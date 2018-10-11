## Final keyword in java

It is used to make a variable as a constant, Restrict method overriding, Restrict inheritance. It is used at variable level, method level and class level. In java language final keyword can be used in following way.

- Final Keyword at Variable Level
- Final Keyword at Method Level
- Final Keyword at Class Level

## Final at variable level

Final keyword is used to make a variable as a constant. This is similar to const in other language. A variable declared with the final keyword cannot be modified by the program after initialization. This is useful to universal constants, such as "PI".

## Final Keyword in java Example

```java
package com.andrewProgramming;

public class Circle {

  public static final double PI = 3.14159;

  public static void main(String[] args) {
    System.out.println(PI);
  }
}
```

## Final Keyword at method level

It makes a method final, meaning that sub classes can not override this method. The compiler checks and gives an error if you try to override the method.

When we want to restrict overriding, then make a method as a final.

## Example

```java
public class A {

  public void fun1() {
    .......
  }

  public final void fun2() {
    .......
  }

}

class B extends A {

  public void fun1() {
    .......
  }

  public void fun2() {
    // it gives an error because we can not override final method
  }
}
```

### Example of final keyword at method level

## Example

```java
class Employee {

  final void disp() {
    System.out.println("Hello Good Morning");
  }
}

class Developer extends Employee {

  void disp() {
    System.out.println("How are you ?");
  }
}

class FinalDemo {

  public static void main(String args[]) {
    Developer obj = new Developer();
    obj.disp();
  }
} 
```

## Output

```java
It gives an error
```

## Final Keyword at Class Level

It makes a class final, meaning that the class can not be inheriting by other classes. When we want to restrict inheritance then make class as a final.

## Example

```java
public final class A {
    ......
    ......
}

public class B extends A {
// it gives an error, because we can not inherit final class
}
```

### Example of final keyword at class level

## Example

```java
package com.andrewProgramming;

final class Employee {

  int salary = 10000;
}

class Developer extends Employee {

  void show() {
    System.out.println("Hello Good Morning");
  }
}

class FinalDemo {

  public static void main(String args[]) {
    Developer obj = new Developer();
    Developer obj = new Developer();
    obj.show();
  }
}
```

## Output

```java
Output:
It gives an error
```