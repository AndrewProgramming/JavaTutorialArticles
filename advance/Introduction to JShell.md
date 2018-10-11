# Introduction to JShell

The Java Shell tool (JShell) is an interactive tool for learning the Java programming language and prototyping Java code. JShell is a Read-Evaluate-Print Loop (REPL), which evaluates declarations, statements, and expressions as they are entered and immediately shows the results. The tool is run from the command line.

Topics

- Why Use JShell?
- Starting and Stopping JShell

For reference information for this tool, see `jshell` in Java Platform, Standard Edition Tools Reference.



## Why Use JShell?

Using JShell, you can enter program elements one at a time, immediately see the result, and make adjustments as needed.

Java program development typically involves the following process:

- Write a complete program.
- Compile it and fix any errors.
- Run the program.
- Figure out what is wrong with it.
- Edit it.
- Repeat the process.

JShell helps you try out code and easily explore options as you develop your program. You can test individual statements, try out different variations of a method, and experiment with unfamiliar APIs within the JShell session. JShell doesn’t replace an IDE. As you develop your program, paste code into JShell to try it out, and then paste working code from JShell into your program editor or IDE.



## Starting and Stopping JShell

JShell is included in JDK 9. To start JShell, enter the `jshell` command on the command line.

JDK 9 must be installed on your system. If your path doesn’t include `java-home/jdk-9/bin`, start the tool from within that directory.

The following example shows the command and the response from JShell. Text that you enter is shown in bold:

```java
% jshell
|  Welcome to JShell -- Version 9
|  For an introduction type: /help intro

jshell>
```

The examples in this tutorial use the verbose mode. Verbose mode is recommended as you work through this tutorial so that what you see matches the examples. When you are more familiar with the tool, you might prefer to run in normal or a more concise mode.

To start JShell in verbose mode, use the `-v` option:

```
% jshell -v
```

To exit JShell, enter `/exit`:

```java
jshell> /exit
|  Goodbye
```