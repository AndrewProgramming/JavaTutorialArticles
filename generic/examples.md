# A wildcard generic type has three forms  

- ?
- ? extends T 
- ? super T ,

where T  is a generic type.

# Examples

###  unbounded wildcard example

Example shows an example of using the `? ` wildcard in the print  method that prints

objects in a stack and empties the stack.` <?>`  is a wildcard that represents any object type. It

is equivalent to `<? extends Object>` . What happens if you replace GenericStack`<?>`

 with GenericStack`<Object>` ? It would be wrong to invoke print(intStack) ,

because intStack  is not an instance of GenericStack`<Object>` . Please note that

GenericStack`<Integer>`  is not a subtype of GenericStack`<Object>` , even though

Integer  is a subtype of Object .

```java
import DefineGenericClassAndInterface.GenericStack;

public class AnyWildCardDemo {

    public static void main(String[] args) {
        GenericStack<Integer> intStack = new GenericStack();
        intStack.push(1); // 1 is autoboxed into new Integer(1)
        intStack.push(2);
        intStack.push(-2);

        print(intStack);
    }

    /**
     * Prints objects and empties the stack
     */
    public static void print(GenericStack<?> stack) {
        while (!stack.isEmpty()) {
            System.out.print(stack.pop() + " ");
        }
    }
}
```

If we change `print` method to  below will cause an error.

```java
 public static void print(GenericStack<Object> stack) {
        while (!stack.isEmpty()) {
            System.out.print(stack.pop() + " ");
        }
 }
```

```java
Exception in thread "main" java.lang.ClassCastException: java.base/java.lang.Integer cannot be cast to java.base/java.lang.String
	at BadExample.main(BadExample.java:14)

Process finished with exit code 1
```

###  lower-bounded wildcard example

```java
package superwildcarddemo;

import DefineGenericClassAndInterface.GenericStack;

public class SuperWildCardDemo {
    public static void main(String[] args) {
        GenericStack<String> stack1 = new GenericStack();
        GenericStack<Object> stack2 = new GenericStack();
        stack2.push("Java");
        stack2.push(2);
        stack1.push("Sun");
        add(stack1, stack2);
    }

    public static <T> void add(GenericStack<T> stack1, GenericStack<? super T> stack2) {
        while (!stack1.isEmpty())
            stack2.push(stack1.pop());
    }

    //If we change GenericStack<? super T> to GenericStack<T> will cause an error
//    public static <T> void add(GenericStack<T> stack1, GenericStack<T> stack2) {
//        while (!stack1.isEmpty())
//            stack2.push(stack1.pop());
//    }
}
```

### bound wildcard example

```java
package boundWildcard;

import DefineGenericClassAndInterface.GenericStack;

public class BoundWildCardDemo {
    public static void main(String[] args) {
        GenericStack<String> stack1 = new GenericStack();
        GenericStack<Object> stack2 = new GenericStack();
        stack2.push("Java");
        stack2.push(2);
        stack1.push("Sun");
        add(stack1, stack2);
        diaplyStackElement(stack2);
    }

    public static <T> void add(GenericStack<? extends T> stack1, GenericStack<T> stack2) {
        while (!stack1.isEmpty())
            stack2.push(stack1.pop());
    }

    public static <T> void diaplyStackElement(GenericStack<T> stack) {
        while (!stack.isEmpty()) {
            System.out.println(stack.pop());
        }
    }
}
```

