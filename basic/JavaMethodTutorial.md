> Finding more Tutorial on [Andrew Programming](https://github.com/AndrewProgramming/JavaTutorial_javaMethodTutorial)

# Methods in Java

A method is a collection of statements that perform some specific task and return result to the caller. A method can perform some specific task without returning anything. Methods allow us to **reuse** the code without retyping the code. In Java, every method must be part of some class which is different from languages like C, C++ and Python.
Methods are **time savers** and help us to **reuse** the code without retyping the code.

**Method Declaration**

In general, method declarations has six components :

- Modifier Defines access type of the method i.e. from where it can be accessed in your application. In Java, there 4 type of the access specifiers.
  - public: accessible in all class in your application.
  - protected: accessible within the class in which it is defined and in its **subclass(es)**
  - private: accessible only within the class in which it is defined.
  - default (declared/defined without using any modifier) : accessible within same class and package within which its class is defined.
- **The return type** : The data type of the value returned by the the method or void if does not return a value.
- **Method Name** : the rules for field names apply to method names as well, but the convention is a little different.
- **Parameter list** : Comma separated list of the input parameters are defined, preceded with their data type, within the enclosed parenthesis. If there are no parameters, you must use empty parentheses ().
- **Exception list** : The exceptions you expect by the method can throw, you can specify these exception(s).
- **Method body** : it is enclosed between braces. The code you need to be executed to perform your intended operations.

[![methods in java](http://cdncontribute.geeksforgeeks.org/wp-content/uploads/methods-in-java.png)](http://cdncontribute.geeksforgeeks.org/wp-content/uploads/methods-in-java.png)

**Calling a method**

The method needs to be called for using its functionality. There can be three situations when a method is called:
A method returns to the code that invoked it when:

- It completes all the statements in the method
- It reaches a return statement
- Throws an exception

```java
package com.andrewProgramming;

// Program to illustrate methods in java

public class MethodDemo {


  //define a method
  private String whoIam() {
    int random = (int) (Math.random() * 2);
    System.out.println("random:" + random);
    String name = null;
    switch (random) {
      case 0:
        name = "kobe";
        break;
      case 1:
        name = "jordan";
        break;

    }
    return name;
  }


  public static void main(String[] args) {

    MethodDemo methodDemo = new MethodDemo();

    //calling the method and print it
    System.out.println(methodDemo.whoIam());

  }
}
```

## Source code

[Github](https://github.com/AndrewProgramming/JavaTutorial_javaMethodTutorial)