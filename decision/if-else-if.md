#if-else-if 

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

### 