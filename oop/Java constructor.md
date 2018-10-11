> Finding more tutorials on [Andrew Programming](http://www.andrew-programming.com)

##Overview

In [class-based](https://en.wikipedia.org/wiki/Class-based_programming) [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming), a **constructor** (abbreviation: **ctor**) is a special type of [subroutine](https://en.wikipedia.org/wiki/Subroutine) called to [create an object](https://en.wikipedia.org/wiki/Object_creation). It prepares the new object for use, often accepting [arguments](https://en.wikipedia.org/wiki/Parameter_(computer_programming)) that the constructor uses to set required [member variables](https://en.wikipedia.org/wiki/Member_variable).

### Java

In [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), constructors differ from other methods in that:

- Constructors never have an explicit return type.
- Constructors cannot be directly invoked (the keyword “`new`” invokes them).
- Constructors cannot be *synchronized*, *final*, *abstract*, *native*, or *static*.
- it should not contain modifiers

Java constructors perform the following tasks in the following order:

1. Call the default constructor of the superclass if no constructor is defined.
2. Initialize member variables to the specified values.
3. Executes the body of the constructor.

Java permit users to call one constructor in another constructor using `this()` keyword. But `this()` must be first statement.

##There are two types of constructors:

- Default constructor (no-arg constructor)
- Parameterized constructor

A constructor having no parameter is known as default constructor and no-arg constructor.

###Default constructor

The structure of a default constructor is like this:

```java
class Demo{
public Demo(){
   System.out.println("This is a default constructor");
  }
}
```

The syntax of default constructor:

Syntax:

```java
<class_name>(){

}
```

###Parameterized Constructor

A constructor having an argument list is known as a parameterized constructor. Parameterized constructors are used to supply dissimilar values to the distinct objects.

The structure of a parameterized constructor in Java is:

```java
class Demo
{
 public Demo(int num, String str)
  {
   System.out.println("This is a parameterized constructor");
  }
}
```

## Example

```java
package com.andrewProgramming;

public class Person {

  private String id;
  private String name;
  private String gender;

  /* This is default constructor */
  public Person() {
  }


  /* This is parameterized constructor */
  public Person(String id, String name, String gender) {
    this.id = id;
    this.name = name;
    this.gender = gender;
  }

  public static void main(String[] args) {
    //This will call default constructor
    Person andrew = new Person();

    //This is will call parameterized constructor
    Person kobe = new Person("1", "Kobe Bryant", "male");
  }
}
```

## Source code

### [Github](https://github.com/AndrewProgramming/JavaTutorial_JavaConstructor)

