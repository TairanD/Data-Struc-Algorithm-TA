# AVL Tree
(_**Updating**_)

## 1 - Motivation
In the last chapter, I introduced that the time performance of find method is best, `O(log n)`, when the binary search tree is balanced. 

So, why don't we create a class that's automatically balanced? - This is the motivation of the AVL tree. 

## 2 - Definition
AVL trees are **self-balancing** binary search tree, which means AVL trees satisfy the following property:
- height-balance property: for every internal node _v_ in tree T, **the heights of the children of _v_ can differ by at most 1**.

Remember our objective is:
- Creating a class, with which other programmers do not need to worry about the undesirable time performance caused
by bad tree structure when they operate the tree (add, delete nodes), as the class is **self-balancing**.

Therefore, it's our responsibility to balance the tree inside the class. Let's see what should we do.

#### The following parts will be quite tedious, but it's necessary to complete your assignment.

## 3 - Insertion: put(k, v)
### 3.1 - Begin with Expansion and Property Check
Remember, AVL trees are self-balancing binary search tree, which means we can insert a new node just like a binary
search tree (by comparing keys). The expected performance of this operation is O(log n).

**Notice here!** As I said above, the key difference between AVL trees and common BSTs is that after insertion, we need
to check if the height-balance property still holds:
- we need to search upwards begin from the newly inserted node
- for each node we visit, we check if whether its height-balance property holds by **compare the height** of its children
  - if the difference in height between the two children is greater than 1, the tree becomes unbalanced! For example, after we
inserted a node with key 54, the tree becomes unbalance:
  <div align="center">
    <img src="img/unbalanced-avl.png" width = "400">
  </div>
### 3.2 - How to make unbalanced tree balanced again? - restructure
Since we need to restore the height-balance property of the AVL tree, we need to **restructure** it.

Let's label the crucial nodes in this restructuring process:
1. _z_: the first unbalanced node encountered while travelling up the tree from the newly expanded node.
2. _y_: the child of _z_ with larger height
3. _x_: the child of _y_ with larger height
  <div align="center">
    <img src="img/labelled-avl.png" width = "300">
  </div>

#### Two Cases of restructure


## 4 - Removal