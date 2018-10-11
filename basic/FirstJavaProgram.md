## Overview

This toturial will create your very first Java program with some basic explanation to help you better understand.

## Prerequest

- JDK 1.8
- Any Text Editor

## Steps

1. Writing a program and save it as `HelloWorld.java` by using any text editor you like.
2. Using `javac` command compile this java file to class file.
3. Using `java` command to run the program and checkout the result

##Workflow

![img](https://lh3.googleusercontent.com/W2p_Ub-NoWGcgLuo82r3XDsu2PDlEMp2TJlC2yY8TaQ2o6og-u3Z8jj2mW05mSnswGCKHElwwI3S8nQMWDjQTEFjZSDH4KkRh5VSzA9pc_1hC4F1CWlR7y0RFwX8vupiG8QTRXAy28HBRy6YP2NaV0TfPvAptuSnW05axjdBsy2gPygWSeJ2WjqYQThk_epvMd8r0Gnf8qDq4bEAO4kfmWBCuMWHSZjPZUfUQPTcDm4_qWyAm2OhqxtZlJXpTDUN78mCNUiuL9SItxyo-swWZf6nVt1suz7qACqK9wZTHpMNiBa0hLLNdcVhr7JPjGu1HZYXxy4N9IrudncQpUxgm3Q1GC0T5qAMziudu8JhMT_HhCVc6RRQ-2BnSb-l0Um8bcbZPVJR0z41THwCbTa3fb28DqPIaSCdDsDV1-0xcUnZm3ICqGmxPlDunsOG7qcLRJaHkGmpxkVquVtHIM5UQImTx0YsFUCK21rcBLeP-3iJR-2X-mgVK2RYGJAwnYDKhlW0BoURIuzrjWGvjAqib2RcZ_8JtYKExzRZ0tJ0p8-Eqti-AXXW1a5Gjojekp5vMYKJ9zYXP3t7GwRuiEnuTFCT-iyGbLwSHfuxAk5YF6CEIZDgbNGxtk98DXFC4cI=w1416-h962-no)

## Component

#### HelloWorld.java

```java
1 public class Welcome{
2     public static void main(String[] args) {
3        //Display Hello World! on the console
4         System.out.println("Welcome to Java!");
5     }
6 }
```

> don't type line number in your program since i put here for line numbers are for reference purposes only

Each source file can contain one public class. The source file's name has to be the name of that class. By convention, the source file uses a **.java** filename extension (a tail end of a file name that marks the file as being of a particular type of file.)

Line 1 defines a class. Every Java program must have at least one class. Each class has a name. By convention, class names start with an uppercase letter. In this example, the class name is `HelloWorld`.

Line 2 defines the `main` method. The main  method is the entry point where the program begins execution.

Line 3 is a comment  that documents what the program is and how it is constructed.Comments help programmer better understand what the code is really doing. They are not programming statements and thus are ignored by the compiler.For more details about comment in java please refer this [link](http://www.andrew-programming.com/2018/09/26/comments-in-java-code/).

A pair of curly braces in a program forms a block  that groups the program’s components.In Java, each block begins with an opening brace **({ ) and ends with a closing brace (} )**. Every class has a class block  that groups the data and methods of the class. Similarly, every method has a method block  that groups the statements in the method.

You have seen several special characters (e.g., { } , // , ; ) in the program. They are used in almost every program. Table 1.2 summarizes their uses.

####Tables Special Character

| Character | Name                                                         | Description                                      |
| --------- | ------------------------------------------------------------ | ------------------------------------------------ |
| {}        | Opening and closing braces                                   | Denote a block to enclose statements.            |
| ()        | engine to be used for processing templates. Handlebars is the default. | Used with methods.                               |
| []        | extension to be used for dest files.                         | Denote an array.                                 |
| //        | Double slashes                                               | Precede a comment line.                          |
| " "       | Opening and closing quotation marks                          | Enclose a string (i.e., sequence of characters). |
| ;         | Semicolon                                                    | Mark the end of a statement.                     |

 #### Using `Javac` complie source file into java bytecode file	

 A Java compiler translates a Java source file into a Java bytecode file. The following command compiles `Welcome.java`:

> `javac Welcome.java`

The Java language is a high-level language, but Java bytecode is a low-level language. The bytecode  is similar to machine instructions but is architecture neutral and can run on any platform that has a [Java Virtual Machine (JVM)](http://www.andrew-programming.com/2018/09/11/java-virtual-machine-jvm-difference-jdk-jre-jvm-core-java/)

Rather than a physical machine, the virtual machine is a program that interprets Java bytecode. This is one of Java’s primary advantages: Java bytecode can run on a variety of hardware platforms and operating systems.  Java source code is compiled into Java bytecode and Java bytecode is interpreted by the JVM. Your Java code may use the code in the Java library. The JVM executes your code along with the code in the library. To execute a Java program is to run the program’s bytecode. You can execute the bytecode on any platform with a JVM, which is an interpreter. It translates the individual instructions in the bytecode into the target machine language code one at a time rather than the whole program as a single unit. Each step is executed immediately after it is translated.

![img](https://lh3.googleusercontent.com/zMRWpRXux1VKkEHvB5kG1cTPMH8n2KVZGu2iibm47kgvIC0FaZW7UQ11bliwqlytiyVXDzPQM0PKa-71rTiw-Wr4bxFHtzaexQYu4uSoW3Co5dbGz9RknQzQ3iitRoucul703j3kHxrE7yJrhwxyslkIsVsg2uoKtalEsRMIeEmuudkvdPVEUhj-myOmmdsRHxkuu_0JsPFUK5WHdgOqCsZk7NT_lWsVD1dBbUzcVJKaDNcdXgpnN_azvyKvAdrmJRIZbpBjYcGoj8u-y7NmB7TcVm73_L1sbPJh67XBnyNwPftVmbRMT_1hubd5DR9PtWENCm5jPwM8h8l2iwNa_uDdKeCFkOI69H7NT4VVlfk1suwIW8BL0SB0uzFnP9RqHP-Pan8u0lmnvgxD0w1EJRpaSThzEIrkZB5RLQiOZqO2DzTH9fYCnu8QaanTGrkIB2og6UY5_9BRpVvLzvilYXTI1trqywBBng1Yx0pqysTzdkP13opL4LfH1oYET9HgmqlJl8mpAqB7clEjd9jFL3BNCFxhLSxaW5q7Ky4fWhdeRc-z14Zoe6YYNHDYikgmFLS8gE8YNa8G1xy3pOSekFucCcmzOIm4Zn0JGG8aCrB2O-Ng50yeAwLQY2rklac=w1588-h490-no)

Picture below shows how to using the `javac` and `java` command to compile and run the program.

> Do not use the extension .class in the command line when executing the program.
>
> Use java ClassName to run the program. If you use java ClassName.class in the command line, the system will attempt to fetch ClassName.class.class.

![img](https://lh3.googleusercontent.com/ildJKEuFrBGRfHKWlKJd8QWHxVRFGuKzco3Izjxpk3sp1YcU4zBpCMpwJg3fMV-LaoSaaIVch6oWo2HHfwxUyvm7Oyvt7-bWlq1VdtCsEyPpkdw74mnXc39cqnoAtIRp6xwbiataUlL0CYW6uNtGj1OOzrQT2vJ8k0ZDKkapF6kLE-DpPfkd_lJ-XZXEjOX3xWzjcKAyxIU2hMuTzOl5sivZkKAiQmSiFRBy2wx_HkVxg6MrPNO4esM6_Mga9cO-FpLov4W7_NrcTRPdFk4mhZgU2SansUFl5KWsiNxLfQnGxU6h-crUA3mJDxOYGuKIQMe_WQ2Ro36lkay_8ylhTkQpf-cPZKmAtm6U9DTeQV8ULjEASBfW_-OLihd4xr2hTEzs1-LBCzQ5MJ7_7IuBHMiCis9Yf7ZNYLJFwU603Djp-AMIa3vAvbCVh0hkhftmmZ-3f7-_5iCg-pBz6i59PKdDTw_kO_RzhtPRw1-FuQ6wsxc7nrOVPVTpxy2oUHkfVmOxzYX5wgaLUKkHJOVOpbUXngU7U4nAjbm8zJ2QIwFKMlB41JXd4Y6Ag8rkVdjuhIOQKWmQYmbIDj28FyW1qrpV39F4oSDQvoPpsDLH7GyEfnGPYNwhabN0u-ktrsM=w914-h314-no)

## Questions

1. What is the Java source filename extension, and what is the Java bytecode filename extension?
2. What are the input and output of a Java compiler?
3. What is the command to compile a Java program?
4. What is the command to run a Java program?
5. What is the JVM?
6. Can Java run on any machine? What is needed to run Java on a computer?