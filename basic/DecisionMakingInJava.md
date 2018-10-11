#Decision Making in Java

Decision Making in programming is similar to decision making in real life. In programming also we face some situations where we want a certain block of code to be executed when some condition is fulfilled.
A programming language uses control statements to control the flow of execution of program based on certain conditions. These  are used to cause the flow of execution to advance and branch based on changes to the state of a program.

##Java’s Selection statements:

- if
- if-else
- nested-if
- if-else-if
- switch-case
- jump - break, continue,return

###if condition

![Decision Making](/Users/andrew/Desktop/decision_making.png)

This logic is really simple. if the condition return `true` then execute the code block.

```java
if(condition){
    //statement to execute if condition is true
}
```

Look at the example below since `a<b` is true then the code inside the curly braces will be executed.

```java
 public static void showIf() {
    int a = 10;
    int b = 20;
    if (a < b) {
      System.out.println("a<b is true");
    }
  }
```

The output is:

`a<b is true`

###if-else condition

The if statement alone tells us that if a condition is true it will execute a block of statements and if the condition is false it won’t. But what if we want to do something else if the condition is false. Here comes the else statement. We can use the else statement with if statement to execute a block of code when the condition is false.

```java
if (condition)
{
    // Executes this block if
    // condition is true
}
else
{
    // Executes this block if
    // condition is false
}
```

The output below will be `a<b is false` since `a<b` is false.

```java
public static void showIfElse() {
  int a = 100;
  int b = 20;
  if (a < b) {
    System.out.println("a<b is true");
  } else {
    System.out.println("a<b is false");
  }
}
```

###nested-if

nested-if:

 A nested if is an if statement that is the target of another if or else. Nested if statements means an if statement inside an if statement. Yes, java allows us to nest if statements within if statements. i.e, we can place an if statement inside another if statement.

Syntax:

```java
if (condition1) 
{
   // Executes when condition1 is true
   if (condition2) 
   {
      // Executes when condition2 is true
   }
}
```

Code below will print `a<b is true`.

```java
 public static void showNestedIf() {
    int a = 10;
    int b = 20;
    if (a == 10) {
      if (a < b) {
        System.out.println("a<b is true");
      } else {
        System.out.println("a<b is false");
      }
    }
  }
```

###if-else-if 

Here, a user can decide among multiple options.The if statements are executed from the top down. As soon as one of the conditions controlling the if is true, the statement associated with that if is executed, and the rest of the ladder is bypassed. If none of the conditions is true, then the final else statement will be executed.

```java
if (condition)
    statement;
else if (condition)
    statement;
.
.
else
    statement;
```

Code below will print `a==10`

```java
public static void showIfElseIf() {
  int a = 10;
  if (a == 1) {
    System.out.println("a==1");
  } else if (a == 2) {
    System.out.println("a==2");
  } else if (a == 3) {
    System.out.println("a==3");
  } else {
    System.out.println("a==10");
  }
}
```

###switch-case

The switch statement is a multiway branch statement. It provides an easy way to dispatch execution to different parts of code based on the value of the expression.

Syntax:

```java
switch (expression)
{
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
  .
  .
  case valueN:
    statementN;
    break;
  default:
    statementDefault;
}
```

- Expression can be of type byte, short, int char or an enumeration. Beginning with JDK7, *expression* can also be of type String.
- Dulplicate case values are not allowed.
- The default statement is optional.
- The break statement is used inside the switch to terminate a statement sequence.
- The break statement is optional. If omitted, execution will continue on into the next case.

Code below will print `Switch demo a==20`.

```java
public static void showSwitch() {
  int a = 20;
  switch (a) {
    case 1:
      System.out.println("a==1");
      break;
    case 2:
      System.out.println("a==2");
      break;
    case 3:
      System.out.println("a==3");
      break;
    default:
      System.out.println("Switch demo a==20");
  }
}
```

###jump

 Java supports three jump statement: 

* break
* continue
* return

. These three statements transfer control to other part of the program.

####Break

In Java, break is majorly used for:

- Terminate a sequence in a switch statement (discussed above).
- To exit a loop.
- Used as a “civilized” form of goto.

**Using break to exit a Loop**

Using break, we can force immediate termination of a loop, bypassing the conditional expression and any remaining code in the body of the loop.
Note: Break, when used inside a set of nested loops, will only break out of the innermost loop.
![using-break-to-exit-a-loop-in-java](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/exit.png)

Code below won't loop 100 times since `a==10` will break the loop and print `Since a==10 then break the loop`.

```java
public static void showJumpBreak() {
  int a = 10;
  for (int i = 0; i < 100; i++) {
    if (a == 10) {
      System.out.println("Since a==10 then break the loop");
      break;
    }
  }
}
```

####Continue

Sometimes it is useful to force an early iteration of a loop. That is, you might want to continue running the loop but stop processing the remainder of the code in its body for this particular iteration. This is, in effect, a goto just past the body of the loop, to the loop’s end. The continue statement performs such an action.
![continue-in-java](https://contribute.geeksforgeeks.org/wp-content/uploads/continue-1.png)

Code below print odd number. Since we just wanna odd number so if the number is not odd then we don't need to run the rest of the code then we just leave this loop and enter the next one.

It will print `1 3 5 7 9`.

```java
public static void showJumpContinue() {
  int a = 10;
  for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) {
      continue;
    }
    // If number is odd, print it
    System.out.print(i + " ");
  }
}
```

**Return:**The return statement is used to explicitly return from a method. That is, it causes a program control to transfer back to the caller of the method.

Code below shows the `return` keyword usage since `if` statement will be executed so the code 

`    System.out.println("This won't execute.");`  will not executed.

```java
 public static void showJumpReturn() {
    boolean t = true;
    System.out.println("Before the return.");

    if (t) {
      return;
    }
    // Compiler will bypass every statement
    // after return
    System.out.println("This won't execute.");
  }
```

#Source code

[Github](https://github.com/AndrewProgramming/JavaTutorial_JavaDecisionMakingTuotrial/tree/master)