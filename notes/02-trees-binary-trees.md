<body style="font-family: serif"></body>

# Trees
(_**Updating**_)

## 1 - Definition
- A tree is an Abstract Data Type (ADT) that stores data **hierarchically** in **nodes**. Look at the example tree below, it looks like a
family tree. In fact, they are similar. Our tree ADTs also use a lot of terminology from family trees.
<div align="center">
<img src="img/tree.png" width = "600">
</div>

- Formal Definition: a tree is a hierarchical ADT where data is related in terms of parent-child relationships.

## 2 - Why Trees?
In the [introduction](./01-intro.md) I emphasized the crucial role of learning data structures for developers, and now, 
you can tell why. Tree data structure can make lots of algorithms much faster relying on its special structure. Ofcourse it also
has disadvantages. Their utility is highly task-dependent, proving immensely advantageous for certain applications (like searching) while
potentially less suitable for others (like finding). We will delve into these aspects shortly.


## 3 - Terminology
- Root: the only node with no parent.
- Siblings: nodes that have the same parent.
- Internal Nodes: any node that has one or more children.
- External Nodes: any node that has no child.
- Ancestor of node _n_: any node above _n_.
  - and ***_n_ itself !!***
- Descendent of any node below _n_.
  - and ***_n_ itself !!!!***
- Edge: a pair of 'father-son' nodes (parent node, child node).
- Path: a sequence of node **from above to below**, the reverse order is NOT a path.
- Subtree: a subtree of tree T at node _v_ is the tree consisting of _v_ and all nodes below _v_ (figure showed below).

<div align="center">
<img src="img/subtree.png" width = "300">
</div>

## 4 - Tree's Properties (this part will definitely appear in your test :)
For a node _n_:
- Depth (level) of _n_: the number of nodes above v (v's ancestors excluding v itself). E.g. the depth of a root is zero.
- Degree of _n_: the number of children of _n_. E.g. the degree of an external node is zero.
- Height of a tree T: the maximum depth of an external node of T.
- Height of _n_: 
  - if _n_ is an external node, its height = 0
  - elif _n_ is an internal node, its height = 1 + the maximum height of _n_'s child
  - Note: Height of the tree = height of the root node
  - Also, the height of _n_ is the deepest path's amount of node (not include itself).

## 4 - Define a Tree ADT: ITree
### 4.1 - IPosition (Java)
- Naming convention: all interfaces starts with a capital "I", separating interfaces from classes
- Position: a **Position** is an abstraction for storing an element within a data structure. Consider nodes in the tree as one specific form 
of **Position**.
```
public interface IPosition<T> {
 public T element();
}
```
You may notice the wired `<T>`, which is included in your last semester's OOP course. Yet, I believe after one vocation 
there is nothing left in your head. 
Based on the importance of this concept and its utility in your future labs and assignments,
let's quickly review the concept of generics (泛型) 

#### * Quick Revision: generics
- Why generics? - Because we want data structures compatible to multiple types of data.
- What's generics? - A technique allowing us to replace actual types (like String) with **type parameter** 
  - Type parameter: one or more symbols wrapped by `<>` , in the above case, `T`.
- How generics achieves our expectation? - By specify type parameter behind class name when we create a variable,
the type parameter will become the specified type. Take our familiar ArrayList<E> as an example. We only need to define ArrayList for once, 
and it is compatible to multiple types (String, Integer, Person) of data.
  ```
  ArrayList<String> = strList;
  ArrayList<Integer> = intList;
  ArrayList<Person> = personList;
  ```

So, using generic, we can define our ITree, where T is a generic type. It refers to the types of elements that will be 
stored in this tree:
``` 
public interface ITree<T> {
 public IPosition<T> root();
 public IPosition<T> parent(IPosition<T> n);
 public Iterator<IPosition<T>> children(IPosition<T> n);
 public boolean isInternal(IPosition<T> n);
 public boolean isExternal(IPosition<T> n);
 public boolean isRoot(IPosition<T> n);
 public int size();
 public boolean isEmpty();
 public Iterator<T> iterator();
 public Iterator<IPosition<T>> nodes();
 public T replace(IPosition<T> n, T e);
}
```

### 4.2 - Iterator (Java)
Iterator is important and very common-used in your future coding projects. It is a Java build-in interface with the aim to
traverse a sequence of element. 
- `public boolean hasNext();`: an Iterator method that returns a boolean value
  - true if and only if (iff) there is another element available.
  - false iff there is not
- `public T next();`: an Iterator method that returns the next element in the sequence. When you firstly call this method,
it will return the first element as the 'next element'.



# Binary Trees

## 1 - Definition

## 2 - Binary Trees ADT

## 3 - Implementation
