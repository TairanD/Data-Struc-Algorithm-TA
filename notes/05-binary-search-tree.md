# Binary Search Tree (BST)

## 1 - Definition
A binary search tree is a special type of binary trees. It possesses following characteristics:
1. Each internal node holds a value
2. A _total-order relation_ is defined on those values (a.k.a. those values are comparable)
3. **The left sub-tree of a node contains only values that are less than the nodes value.**
4. **The right sub-tree of a node contains only values that are greater than the nodes value.**

*Note: do you still remember and can distinguish following concepts? If you forget, revise the previous slides!
- tree, binary tree, proper binary tree

## 2 - Example
<div align="center">
<img src="./img/bst.png" width = "600">
</div>

From the image above we can clearly see why _inorder traversal_ will visit nodes in sorted order.

## 3 - BST Interface
Note here I do not use the example in the slides to **simplify** the process and hope make it more understandable to you.
``` javascript
public interface IBST<T> {
    public IPostision
    // Insert a node containing value k
    public void put(k); 
    // Return the value v associated with key k, if k is in the tree (otherwise null).
    public T get(k);
    // Remove the entry with key k from the tree.
    public void remove(k);
}
```

## 4 - Implementation


