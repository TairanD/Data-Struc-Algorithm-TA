<body style="font-family: serif"></body>

# Introduction & Revision 
(_**Completed**_)

## 1 - Why Data Structure & Algorithm

Each line of code we compose and every program we design inherently relies on the understanding and application of these
fundamental concepts. Mastery of diverse data structures and algorithms is not merely a desirable skill but an essential
one for anyone in a software engineering or any programming-related role. A proficient developer must possess the
insight to discern which data structures are optimal for specific tasks. In terms of professional perspective, every
company will ask you questions about this field in the interview.

Again, it is **ESSENTIAL**.

## 2 - Revision

You have learned a lot of data structures and several algorithms last semester, in which some concepts are extremely
important. So, let's give a quick revisit to them.

### 2.1 - Time Complexity & Big O Notation

- Time complexity: Think of it like measuring how fast your computer program works. It's like asking, "How long does it
  take for my code to do its thing?" Imagine your program is a song with a fixed amount of words, then a quick rap will
  have small time complexity, and a slow lyrics will have big time complexity.

This is understandable right? But what about big O notation?

- Big O notation: big O notation is **the mathematical representation** of an algorithm's (or a program's...) time
  complexity. Like how we use hours and minutes quantify time.

Yet, unlike hours and minutes, big O notation captures the relationship between an algorithm's time complexity and its
input size. By incorporating the input size into our mathematical representation (e.g., O(N) or O(N^2)), we accurately
reflect how the program's runtime scales with the size of its data, denoted by N.

Now you can understand why O(1) means constant time. 
The time complexity of this program has no business with its size because there is no N!

Different data structures have different time complexity in the same operations. Thus, it's important to know 
how to quantify time complexity with using O notation, and understand the pros and cons of each type of data structure.

### 2.2 Abstract Data Types (ADT)
You've learned interfaces and classes in the OOP course last semester. An interface defines attributes and behaviors
of classes. Likewise, ADTs define attributes and behaviors of data structures. So, you can see them as interfaces 
describing data structures (like stack ADT below).
```
public interface Stack{
    int size();
    boolean isEmpty():
    int top();
    void push(int o);
    int pop();
}
```
Naturally, ADTs (interfaces) don't care about implementation part at all.

## Understanding the concepts above will prepare you to begin this course! 
I plan to continuously upload contents of DS I (like queue, stack, quick sort, etc.) in the following folder.
- [Data Structure I Revision](./revision)

Yet, it's not an easy task to make knowledge more understandable to you guys. I'll mainly focus on the contents this semester.