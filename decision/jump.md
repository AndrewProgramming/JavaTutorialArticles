#jump

 Java supports three jump statement: 

- break
- continue
- return

. These three statements transfer control to other part of the program.

##Break

In Java, break is majorly used for:

- Terminate a sequence in a switch statement (discussed above).
- To exit a loop.
- Used as a “civilized” form of goto.

**Using break to exit a Loop**

Using break, we can force immediate termination of a loop, bypassing the conditional expression and any remaining code in the body of the loop.
Note: Break, when used inside a set of nested loops, will only break out of the innermost loop.
![img](https://lh3.googleusercontent.com/brPNEPi61NAGYySWbIkvE4O9h0xNh7vl54CxYR_de9uNEG6j82OupHNxtB1lA3jtQCviPYucbzlEeYHbBpI3uXrqNxTzkJ_sReOvJQ483QppkEsfFgeDhr5TSWcOeW5QH54y2GfZRSoLHnGgPE4XUoH7YJoFoP-VfFT-e-VmFTzN0uei9w2VuSdFq_T1Yj1ovudsa2c2TyyjB51dSPzMaJ7WKDAF8YpiJKmh-XhJCY0CZC0SYimVhiJJ6kKv0PwXHssnJNr5V3KebyB6q2zFr-jgr0lsQbzPqlYpBXFmXr6yAcMmPuIvQguZdRKsMROoDmP3ELyG7z1u5cgkG62YIDBTSto9Zc-7AhVM6TY_i518kpoMpLzCqx65DbYAx4cyQ0JJZirIEQ7E3guaGTfKKW1JJ1RH0Iv6c3AhZtDdYR9wE6avmb5vaqmxYifFrObagD37W3wIcNIUj0HrMdZyhR6-MVs-aYHiwiGYtAeGEPLXpSaJZKB24ygeghkIg0-vq9UDn7WcS2qXQbrxkCuoeBxnUOMd-IXnLYaIUjgfoniBN1tVr1zPB1jAEaXITAW7uKL0dA54LYCSo3Cp-xexsaTPwxtg40sno4mdkhSZKZytN_B-b3UG7d08tdshnsk=w699-h407-no)

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

##Continue

Sometimes it is useful to force an early iteration of a loop. That is, you might want to continue running the loop but stop processing the remainder of the code in its body for this particular iteration. This is, in effect, a goto just past the body of the loop, to the loop’s end. The continue statement performs such an action.
![img](https://lh3.googleusercontent.com/5XzWzzGDwwqj-hRXtTMyXvAS_hDkYFbvHvuUjZ7giwSXYQ1uMSpbXIVEMAuWtape0tPFCd0KSZbbkSEMtR4qNE3jnmdFncOfhFyjy_WL4Q7gTwvvEK9yoEg4IuY0u4kdpLavcOOa4HRJAL7Bl9IaZ5TuF7EA113FuIa-0Vj0aDI4vvCUvAtvEJMUkEAwo4qirqzj7sFaDKNQpcapahEPysyLCEKIFhI1RLR_bOHKMVwL03z3ONKnv5aYcG-ptA04iCkOHEeX259Xm7FDR5LQtk-yAfxWbXGpy3F3S8vd1PASfycTQYi12ybj5CZ9ObYOwhdgidCuk_mrQUZiFHSDGTN2Jl7MsLljYTijQ5L0sc1EdcJSgliXFOApfERk1QvQumGs26jhfNCrpNvPie_k0F6yEgNeN9zHnNScxZ7bD7wNrIa14I17qUbrdgulqzrB8qwZLtHiVfSvWQnZ0siIcroDVHo9_yHRvXEIk5TqkJw3Lyb5vPXn-SKLEF_THdIDqBbQozbjw4cEtsJoiK9_xGfU-laJhbeKg6-R_9vQcwQenVJ8MI8e9C70a1ARkpLen8ucyGZuMmNJUALyFI2veaKrsPYcNgL1-ZB3Q_kosFnJcqxVtLzL3U4ZpZ2FZbg=w700-h408-no)

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

##Return

The return statement is used to explicitly return from a method. That is, it causes a program control to transfer back to the caller of the method.

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

