#### Multithreading

**Multithreading** is a Java feature that allows concurrent execution of two or more parts of a program for maximum utilization of CPU. Each part of such program is called a thread. So, threads are light-weight processes within a process.Java provides exceptionally good support for creating and running threads and for locking resources to prevent conflicts.

Threads can be created by using two mechanisms :

1. Extending the `Thread` class
2. Implementing the `Runnable` Interface

##### Thread creation by extending the Thread class

We create a class that extends the **java.lang.Thread** class. This class overrides the `run()` method available in the Thread class. A thread begins its life inside `run()` method. We create an object of our new class and call `start()` method to start the execution of a thread. `Start()` invokes the `run()` method on the Thread object.

Code below shows how to define a class extends Thread class to achive multithreading.

```java
  // Java code for thread creation by extending
// the Thread class
  static class MultithreadingDemo extends Thread {

    public void run() {
      try {
        // Displaying the thread that is running
        System.out.println("Thread " +
            Thread.currentThread().getId() +
            " is running");

      } catch (Exception e) {
        // Throwing an exception
        System.out.println("Exception is caught");
      }
    }
  }
```

Then create two threads:

```java
Thread threadOne = new MultithreadingDemo();
Thread threadTwo = new MultithreadingDemo();

threadOne.start();
threadTwo.start();
```

output:

```java
Thread 11 is running
Thread 12 is running
```

#### Thread creation by Implementing `Runnable` interface

```java
  // Java code for thread creation by implementing
// the Runnable Interface
  static class MultithreadingRunnableDemo implements Runnable {

    public void run() {
      try {
        // Displaying the thread that is running
        System.out.println("Thread " +
            Thread.currentThread().getId() +
            " is running");

      } catch (Exception e) {
        // Throwing an exception
        System.out.println("Exception is caught");
      }
    }
  }
```

Then

```java
Runnable threadThree = new MultithreadingRunnableDemo();
Runnable threadFour = new MultithreadingRunnableDemo();

Thread threadObjectOne = new Thread(threadThree);
Thread threadObjectTwo = new Thread(threadFour);

threadObjectOne.start();
threadObjectTwo.start();
```

Output:

```java
Thread 13 is running
Thread 14 is running	
```

#### Thread Class vs Runnable Interface

1. If we extend the Thread class, our class cannot extend any other class because Java doesn’t support multiple inheritance. But, if we implement the Runnable interface, our class can still extend other base classes.
2. We can achieve basic functionality of a thread by extending Thread class because it provides some inbuilt methods like yield(), interrupt() etc. that are not available in Runnable interface.