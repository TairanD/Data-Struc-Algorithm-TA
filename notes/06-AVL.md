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

#### The following parts will be quite tedious, but it's highly possible to appear in your assignment.

## 3 - Insertion

## 4 - Removal