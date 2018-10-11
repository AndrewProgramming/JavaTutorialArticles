# Throws & Throw Keyword

`Throws` and `Throw` are the most commonly used  two keyword in Java but unfortunately they sometimes confuse the beginner a lot .Now let me explain them one by one.

##Declaring Exceptions By Using `throws`

In Java, the statement currently being executed belongs to a method. The Java interpreter invokes the main method to start executing a program. Every method must state the types of checked exceptions it might throw. This is known as declaring exceptions. Because system errors and runtime errors can happen to any code, Java does not require that you declare Error and RuntimeException (unchecked exceptions) explicitly in the method. However,all other exceptions thrown by the method must be explicitly declared in the method header so that the caller of the method is informed of the exception.To declare an exception in a method, use the throws keyword in the method header, as in this example:

`public void myMethod() throws IOException`

The `throws` keyword indicates that myMethod might throw an `IOException`. If the method

might throw multiple exceptions, add a list of the exceptions, separated by commas, after throws:

`public void myMethod() throws Exception1, Exception2, ..., ExceptionN`

> `throws` can only apply to checked exception

## Throwing Exceptions By Using `throw`

A program that detects an error can create an instance of an appropriate exception type and throw it. This is known as throwing an exception .

Look at the code sample below i define my own `Exception` called `OwnDefinedException`.

In the `main` method of `ThrowExceptionDemo` i using the keyword `throw` to mannly throw the exception that defined  by myself and this exception will be catch by the `cacth` block.

```java
package throwExceptionDemo;

public class ThrowExceptionDemo {

  public static void main(String[] args) {
    try {
      // Throw an object of user defined exception
      throw new OwnDefinedException("OwnDefinedException occurs");
    } catch (OwnDefinedException ex) {
      // Print the message from OwnDefinedException object
      System.out.println(ex.getMessage());
    }
  }

}
```

```java
package throwExceptionDemo;

public class OwnDefinedException extends RuntimeException {

  public OwnDefinedException(String s) {
    super(s);
  }
}
```

The output

**OwnDefinedException occurs**

## `Throw` vs `Throws` in java

There are many differences between throw and throws keywords. A list of differences between throw and throws are given below:

| No.  | throw                                                        | throws                                                       |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1)   | Java throw keyword is used to explicitly throw an exception. | Java throws keyword is used to declare an exception.         |
| 2)   | Checked exception cannot be propagated using throw only.     | Checked exception can be propagated with throws.             |
| 3)   | Throw is followed by an instance.                            | Throws is followed by class.                                 |
| 4)   | Throw is used within the method.                             | Throws is used with the method signature.                    |
| 5)   | You cannot throw multiple exceptions.                        | You can declare multiple exceptions e.g. public void method()throws IOException,SQLException. |