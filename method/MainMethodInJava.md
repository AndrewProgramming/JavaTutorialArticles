`public static void main(String[] args)` is the most important [Java method](https://www.journaldev.com/22385/java-method). When you start learning java programming, this is the first method you encounter. Remember the first [Java Hello World program](https://www.journaldev.com/481/java-hello-world-program) you wrote that runs and prints “Hello World”?

##Table of Contents

public static void main(String[] args)

- public
- static
- void
- main
- String[\] args
- Java main method command line arguments in Eclipse

## public static void main(String[] args)

Java main method is the entry point of any java program. Its syntax is always `public static void main(String[] args)`. You can only change the name of String array argument, for example you can change `args` to `myStringArgs`.

Also String array argument can be written as `String... args` or `String args[]`.

[![public static void main string args, java main method](https://cdn.journaldev.com/wp-content/uploads/2016/08/public-static-void-main-string-args.png)](https://cdn.journaldev.com/wp-content/uploads/2016/08/public-static-void-main-string-args.png)

Let’s look at the java main method closely and try to understand each of its parts.

### public

This is the access modifier of the main method. It has to be `public` so that java runtime can execute this method. Remember that if you make any method non-public then it’s not allowed to be executed by any program, there are some access restrictions applied. So it means that the main method has to be public. Let’s see what happens if we define the main method as non-public.



```
public class Test {

static void main(String[] args){

	System.out.println("Hello World");
	
}
}
$ javac Test.java 
$ java Test
Error: Main method not found in class Test, please define the main method as:
   public static void main(String[] args)
or a JavaFX application class must extend javafx.application.Application
$
```

### static

When java runtime starts, there is no object of the class present. That’s why the main method has to be static so that JVM can load the class into memory and call the main method. If the main method won’t be static, JVM would not be able to call it because there is no object of the class is present. Let’s see what happens when we remove static from java main method.

```
public class Test {

public void main(String[] args){

	System.out.println("Hello World");
	
}
}
$ javac Test.java 
$ java Test
Error: Main method is not static in class Test, please define the main method as:
   public static void main(String[] args)
$
```

### void

Java programming mandates that every method provide the return type. Java main method doesn’t return anything, that’s why it’s return type is `void`. This has been done to keep things simple because once the main method is finished executing, java program terminates. So there is no point in returning anything, there is nothing that can be done for the returned object by JVM. If we try to return something from the main method, it will give compilation error as an unexpected return value. For example, if we have the main method like below.

```java
public class Test {

public static void main(String[] args){
	
	return 0;
}
}
```

We get below error when above program is compiled.



```java
$ javac Test.java 
Test.java:5: error: incompatible types: unexpected return value
	return 0;
	       ^
1 error
$
```

### main

This is the name of java main method. It’s fixed and when we start a java program, it looks for the main method. For example, if we have a class like below.

```java
public class Test {

public static void mymain(String[] args){

	System.out.println("Hello World");
 }
}
```

And we try to run this program, it will throw an error that the main method is not found.

```java
$ javac Test.java 
$ java Test
Error: Main method not found in class Test, please define the main method as:
   public static void main(String[] args)
or a JavaFX application class must extend javafx.application.Application
$ 
```

### String[] args

Java main method accepts a single argument of type String array. This is also called  java command line arguments. Let’s have a look at the example of using java command line arguments.

```java
public class Test {

public static void main(String[] args){

    for(String s : args){
	   System.out.println(s);
    }
   }
}
```

Above is a simple program where we are printing the command line arguments. Let’s see how to pass command line arguments when executing above program.

```
$ javac Test.java 
$ java Test 1 2 3
1
2
3
$ java Test "Hello World" "Pankaj Kumar"
Hello World
Pankaj Kumar
$ java Test
$ 
```

### Java main method command line arguments in Eclipse

Below images show how to pass command line arguments when you are executing a java program in Eclipse.

[![java main method eclipse run configurations](https://cdn.journaldev.com/wp-content/uploads/2016/08/java-main-method-eclipse-run-configurations.png)](https://cdn.journaldev.com/wp-content/uploads/2016/08/java-main-method-eclipse-run-configurations.png)

[![java main method command line arguments eclipse](https://cdn.journaldev.com/wp-content/uploads/2016/08/java-main-method-command-line-arguments-eclipse.png)](https://cdn.journaldev.com/wp-content/uploads/2016/08/java-main-method-command-line-arguments-eclipse.png)

[![java main method executing eclipse](https://cdn.journaldev.com/wp-content/uploads/2016/08/java-main-method-executing-eclipse.png)](https://cdn.journaldev.com/wp-content/uploads/2016/08/java-main-method-executing-eclipse.png)

That’s all for `public static void main(String[] args)`, java main method.