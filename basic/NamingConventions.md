#Naming Conventions

Sticking with the Java naming conventions makes your programs easy to read and avoids errors.

Make sure that you choose descriptive names with straightforward meanings for the variables,constants, classes, and methods in your program. As mentioned earlier, names are case sensitive.

Listed below are the conventions for naming variables, methods, and classes.

- Use lowercase for variables and methods. If a name consists of several words, concatenate them into one, making the first word lowercase and capitalizing the first letter of each subsequent word—for example, the variables `radius` and `area` and the method `print`.

-  Capitalize the first letter of each word in a class name—for example, the class names `ComputeArea` and `System`.

-  Capitalize every letter in a constant, and use underscores between words—for example,the constants **PI** and **MAX_VALUE**.

It is important to follow the naming conventions to make your programs easy to read.

> Do not choose class names that are already used in the Java library. For example, since the System class is defined in Java, you should not name your class `System`.

#Rules of naming convention

| Name           | Convention                                                   |
| -------------- | :----------------------------------------------------------- |
| class name     | should start with uppercase letter and be a noun e.g. String, Color, Button, System, Thread etc. |
| interface name | should start with uppercase letter and be an adjective e.g. Runnable, Remote, ActionListener etc. |
| method name    | should start with lowercase letter and be a verb e.g. actionPerformed(), main(), print(), println() etc. |
| variable name  | should start with lowercase letter e.g. firstName, orderNumber etc. |
| package name   | should be in lowercase letter e.g. java, lang, sql, util etc. |
| constants name | should be in uppercase letter. e.g. RED, YELLOW, MAX_PRIORITY etc. |

#Questions

1. What are the benefits of using constants? Declare an int constant SIZE with value 20.

2. What are the naming conventions for class names, method names, constants, and variables? Which of the following items can be a constant, a method, a variable, or a class according to the Java naming conventions?

​      `MAX_VALUE, Test, read, readDouble`

3. Translate the following algorithm into Java code:

   Step 1: Declare a double variable named miles with initial value 100.

   Step 2: Declare a double constant named KILOMETERS_PER_MILE with value 1.609.

   Step 3: Declare a double variable named kilometers, multiply miles and KILOMETERS_PER_MILE, and assign the result to kilometers.

   Step 4: Display kilometers to the console.

   What is kilometers after Step 4?