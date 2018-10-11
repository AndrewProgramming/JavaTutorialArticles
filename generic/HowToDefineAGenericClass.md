#How To Define A Generic Class

> A generic type can be defined for a class or interface. A concrete type must be specified when using the class to create an object or using the class or interface to declare a reference variable.

```java
package DefineGenericClassAndInterface;

import java.util.ArrayList;

public class GenericStack<E> {

    ArrayList<E> arrayList = new ArrayList<E>();

    public void push(E e) {
        arrayList.add(e);

    }

    public E pop() {
        E element = arrayList.get(arrayList.size() - 1);
        arrayList.remove(arrayList.size() - 1);
        return element;
    }

    public boolean isEmpty() {
        return arrayList.size() == 0 ? true : false;
    }
}
```

Call it

```java
package DefineGenericClassAndInterface;

public class CallingGenericStack {
    public static void main(String[] args) {
        GenericStack<String> stack = new GenericStack<String>();
        stack.push("Andrew");
        stack.push("Programming");
        stack.push("is great");

        System.out.println(stack.pop());
        System.out.println(stack.isEmpty());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.isEmpty());
    }
}
```

# Questions

- What is the generic definition for java.lang.Comparable in the Java API?

- Since you create an instance of ArrayList of strings using `new ArrayList<String>()`, should the constructor in the ArrayList class be defined as `public ArrayList<E>()`

- Can a generic class have multiple generic parameters?

- How do you declare a generic type in a class?