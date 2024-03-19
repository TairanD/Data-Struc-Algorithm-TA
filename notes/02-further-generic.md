# Generics
In the lab course last week, I found out a lot of you were still confused about the practices
of **Generics**. Let's talk about it a little more.
## 1 - Conceptual Introduction
- [See this note](02-trees.md), in the _Quick Revision: generics_ section

## 2 - How do we create and implement Generics Classes

### 2.1 - Generic Class
To create a generic class, we need to declare one or more type parameters behind our class name.
```java 
public class Box<T> {
    private T content;

    public T getContent() {
        return content;
    }

    public void setContent(T content) {
        this.content = content;
    }
}
```
### 2.2 - Generic Method
To create a generic method, we need to declare one or more type parameters before declaration of the method's returning
type.
```java
public static <T> T getLastElement(T[] array) {
    if (array == null || array.length == 0) {
        return null;
    }
    return array[array.length - 1];
}
```
In this example, we declare T as the type parameter & T as the method's returning type.
### 2.3 - Generic Interface
Similar to generic class, to create a generic interface,
we need to declare one or more type parameters behind our interface name
```java
public interface List<T> {
    void add(T element);
    T get(int index);
}
```

### 2.4 - Generic Inheritance
A generic class can extend another generic class and pass type parameters (the type parameters of the parent class must be passed to the subclass). For example:
```java
public class MyBox<T> extends FatherBox<T> {
    // Implement specific methods
}
```
In this example, `MyBox<T>` is a generic class that extends another generic class `FatherBox<T>`. The type 
parameter `T` from BaseClass is passed down to `MyBox<T>`, allowing the usage of `T` within `MyBox<T>`.