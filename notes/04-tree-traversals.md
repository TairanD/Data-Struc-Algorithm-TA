# Tree Traversal
(_**Updating**_)

1. [Definition](#1)
2. [Recursion](#2)

## 1 - Definition <a name="1"></a>
- The act of travelling through a tree visiting nodes is known as a **traversal**.
    - where 'visiting' means we **perform some process to nodes**. For example:
      - Find a particular value in the tree.
      - Print the object stored in the node.
      - ......

## 2 - Recursion (_Important!_) <a name="2"></a>
HAHA! Here it comes - **recursion**, one of the biggest troubles for beginners. In this section, let's solve it once for all.

- Recursion: the process in which a function calls **itself**.

Very simple definition right? I would like to illustrate the mechanism of a recursive function:
1. When a recursive function is firstly executed, our computer creates a new data structure (called stack frame) to store 
all the information of the function, including parameters, addresses, etc. 
2. When a recursive function calls itself, all the information will be stored in the current stack frame, and some will be
passed to the next new stack frame (generated due to the recursive execution).
3. Will a recursive function calls itself, and calls itself, and calls itself ...... Forever? Ofcourse not. We certainly 
want it to stop at some point, which is why we need to set up a **_base_** inside our recursive function. 
   - A base indicates the terminal of the current stack frame. When a recursive call reaches a base case, it does not make further recursive calls but starts returning.

*But what happen to the previous functions? - Their information (local variables) is stored in their own stack frames, and
they are **_waiting_** the completion of the currently executing function call. 

4. Once a recursive call reaches a base case or completes its computation, the program starts performing return operations. This involves 
    - popping the corresponding stack frame from the call stack
    - returning control to its caller (the one calling it), and the caller resumes running
5. During the execution of a recursive function, each recursive call returns a result. These results may be passed, 
modified, or combined as part of the recursive process to compute the final result.

## 3 - Tree Traversal
I'm going to introduce three types of tree traversals. 

Which type to use depends on what the tree represents.
### 3.1 - Preorder Traversal
Below is the pseudocode of the preorder traversal, which means visits a node **before** it 
recursively visits its subtrees (left first, then right).

Preorder traversal can be used with any tree type.
```
Algorithm preorder(T,v):
    perform the "visit" action for node v
    
    if v has a left child leftChild in T then
        preorder(T,leftChild)
    
    if v has a right child rightChild in T then
        preorder(T,right)
```

### 3.2 - Inorder Traversal
Below is the pseudocode of the inorder traversal, which means visiting a node
- **after recursively visiting its left subtree**
- **before recursively visiting its right subtree**

Inorder traversal only makes sense for binary trees.
```
Algorithm preorder(T,v):
    if v has a left child leftChild in T then
        preorder(T,leftChild)
        
    perform the "visit" action for node v
    
    if v has a right child rightChild in T then
        preorder(T,right)
```

### 3.3 - Postorder Traversal
Below is the pseudocode of the postorder traversal, which means visits a node **after** recursively 
visiting all its child subtrees (left first, then right).

Postorder traversal can be used with any tree type.
```
Algorithm postorder(T,v):
    if v has a left child leftChild in T then
        preorder(T,leftChild)
    
    if v has a right child rightChild in T then
        preorder(T,right)
        
    perform the "visit" action for node v
```

### 3.4 Which traversal to choose?
It depends on what kind of data your tree represents.
- Postorder: 
  - freeing memory in a tree (deleting the tree one node at a time)
    - we want to delete child nodes before deleting parent nodes because we do not want to lose reference of child notes.
  - calculating the size of a directory/folder (when a filesystem is represented as a tree structure)
    - we need to find out all the sizes of subdirectories, and sum them.
- Inorder (remember, inorder is only suitable for binary tree):
  - so it is very useful when we're dealing with a binary search tree (introduced in the next chapter), where we can visit the values stored in the tree in sorted 
order.
- Preorder: 
  - copy the structure of a tree
    - to create a tree, we usually create parent nodes first, and add children to them. Therefore, preorder allows us to copy the parents before adding their children.
  - present the table of a document's/article's contents
    - we want the biggest title appears first. Take this file as an example, I want the 'Tree Traversal' created firstly.