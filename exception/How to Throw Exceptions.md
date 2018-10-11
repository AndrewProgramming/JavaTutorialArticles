# How to Throw Exceptions

Before you can catch an exception, some code somewhere must throw one. Any code can throw an exception: your code, code from a package written by someone else such as the packages that come with the Java platform, or the Java runtime environment. Regardless of what throws the exception, it's always thrown with the `throw` statement.

As you have probably noticed, the Java platform provides numerous exception classes. All the classes are descendants of the `Throwable` class, and all allow programs to differentiate among the various types of exceptions that can occur during the execution of a program.

You can also create your own exception classes to represent problems that can occur within the classes you write. In fact, if you are a package developer, you might have to create your own set of exception classes to allow users to differentiate an error that can occur in your package from errors that occur in the Java platform or other packages.

## The throw Statement

All methods use the `throw` statement to throw an exception. The `throw` statement requires a single argument: a throwable object. Throwable objects are instances of any subclass of the `Throwable` class. Here's an example of a `throw` statement.

```java
throw someThrowableObject;
```

Let's look at the `throw` statement in context. 

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

The `OwnDefinedException` class is a use defined Exception.

```java
package throwExceptionDemo;

public class OwnDefinedException extends RuntimeException {

  public OwnDefinedException(String s) {
    super(s);
  }
}
```

## Throwable Class and Its Subclasses

The objects that inherit from the `Throwable` class include direct descendants (objects that inherit directly from the `Throwable` class) and indirect descendants (objects that inherit from children or grandchildren of the `Throwable` class). The figure below illustrates the class hierarchy of the `Throwable` class and its most significant subclasses. As you can see, `Throwable` has two direct descendants:`Error`and `Exception`.

![img](https://lh3.googleusercontent.com/7T3hp27aQm8e9v10Jf0Mu4JSvGdsB8uNYo9EnD_2rZsQFbAldhbm0NNMHxwjNSc1qbYKdhaZyKWhZ_HyuCyj3tnSzXuk2oCas_Sqllv58qSKH5AdoW6Ilspi1gBU9SXPy6-njfVukYtavg7Kl8mq4dS1LeMdZ9EuTPkjUcBz59vIo4hqNLy89FNJOmmwNAFol2EKfm9NYvsIrZJgoEn3dJF1lXNg9mVDSuY4oeOZcgG92_JIc7m58MYC-Z9LihOvxy9aDGcrM4UhmhTvW1NSe4UGzD9oKQOheMQb2fQhlOPtKuqxoCVS9Es_7T_gS933paQ2O2_8BvqIvelS1KQyDLqXHk2JEStgPIW0LUT2QnkWgDtfavQNg0LzcDmDH0oViPYODommV1Sg_oMZ5NbgLehtHLM3E9FAXRMOhf675OXJ1M3_9wMqmnR84bx53t7XjX0xcr94cJIwyfKWYqQ0pi4-edFUfrSrDhpGnHfhiktlrLE7pPcjlBckYB5_BJ8_4Fyyu2x4BlebrRvHc650D4j6FvZWrDSS5MQ7WDM5yrYPcT2dia3Htw-aqJvJmAnrHFIOcl8ZGgQx1AxHgkhAlBY_TRYulQ-tqOizTnHgxfibpM7n-qfJ5IiLVNHNHsU=w613-h546-no)



​									The Throwable class.

## Error Class

When a dynamic linking failure or other hard failure in the Java virtual machine occurs, the virtual machine throws an `Error`. Simple programs typically do *not* catch or throw `Error`s.

## Exception Class

Most programs throw and catch objects that derive from the `Exception` class. An `Exception` indicates that a problem occurred, but it is not a serious system problem. Most programs you write will throw and catch `Exception`s as opposed to `Error`s.

The Java platform defines the many descendants of the `Exception` class. These descendants indicate various types of exceptions that can occur. For example, `IllegalAccessException` signals that a particular method could not be found, and `NegativeArraySizeException` indicates that a program attempted to create an array with a negative size.

One `Exception` subclass, `RuntimeException`, is reserved for exceptions that indicate incorrect use of an API. An example of a runtime exception is `NullPointerException`, which occurs when a method tries to access a member of an object through a `null` reference. The section Unchecked Exceptions — The Controversy discusses why most applications shouldn't throw runtime exceptions or subclass `RuntimeException`.

##Source code

[Github](https://github.com/AndrewProgramming/JavaTutorial_JavaExceptionDemo/blob/master/README.md)

##Find more tutorials

www.andrew-programming.com