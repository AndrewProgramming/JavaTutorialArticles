## Overview

This tutorial shows how to use Java Relational Operators.

## The Relational Operators

There are following relational operators supported by Java language.

Assume variable A holds 10 and variable B holds 20, then −

| Operator                      | Description                                                  | Example               |
| ----------------------------- | ------------------------------------------------------------ | --------------------- |
| == (equal to)                 | Checks if the values of two operands are equal or not, if yes then condition becomes true. | (A == B) is not true. |
| != (not equal to)             | Checks if the values of two operands are equal or not, if values are not equal then condition becomes true. | (A != B) is true.     |
| > (greater than)              | Checks if the value of left operand is greater than the value of right operand, if yes then condition becomes true. | (A > B) is not true.  |
| < (less than)                 | Checks if the value of left operand is less than the value of right operand, if yes then condition becomes true. | (A < B) is true.      |
| >= (greater than or equal to) | Checks if the value of left operand is greater than or equal to the value of right operand, if yes then condition becomes true. | (A >= B) is not true. |
| <= (less than or equal to)    | Checks if the value of left operand is less than or equal to the value of right operand, if yes then condition becomes true. | (A <= B) is true.     |

##Demo

```java
public class JavaRelationalOperatorsDemo {

  public static void main(String[] args) {

    int a = 10;
    int b = 20;

    System.out.println(a == b);
    System.out.println(a != b);
    System.out.println(a > b);
    System.out.println(a < b);
    System.out.println(a >= b);
    System.out.println(a <= b);

  }
}
```

##Result

![image-20180914195205203](/Users/andrew/Desktop/tutorials/java/pics/image-20180914195205203.png)

## Source code 

[Github](https://github.com/AndrewProgramming/JavaTutorial_RelationalOperators)