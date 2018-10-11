##### Thread Class

>  The Thread class contains the constructors for creating threads for tasks and the methods for controlling threads.

Picture below shows the `Thread` class.As you may see here this class provides serveal useful methods manipulating the thread.

![img](https://lh3.googleusercontent.com/XWPhT4iaZH_KIw3mFqk30uddBuyJ3xaRMHa6_UeCCW0hl7i5VDwpXxfNpGVYFwkt-YoL_JwzuQDWblMY_13mDul3-_b7UDfKVhLDU6ylT2lkJ3Yb6Ab9AkfgmD8YNOgmfTp86Et6UCDyKx8Ag9VhJeFKcqoCOlpDzKM1Vp67aBpYBrBPzcDD6ey-b8Cis6PfmGl5lSaKHgxTl36fOxdr0z6ygFRFnUuYCn3TUT0t6BDa1K4rbkrtX6mDJ4uC9V27VxJbHGixqbgPcfU6AYGD5S3m5optsKTpOn54BQKxY0PxfQ0rgl0yh-qNXnmvpdm-zY5Tusslw1fsbwZ9tw71CcPZboxzQfPoe_omkyHqaeOAYbVko2AgYrR2mY_dA6dTaVdwtF3ncy1nf159KMSrx6ZpWukGIlpMAjfoIgBeNeIlPKNOVV-eCPfxJvBfKG4R2M397O3xPaoYvZEjSgPhpE8gAw8LfYWqesJ8GH9EMmop1L9xSkvNZ9TtMs5Efh7t2gWtJ1Nqs5pxURb-fdfG3Kv3t84eq0auYRD1hBH9nRyjKYdSPp16Njsuq8IXfiA_rAY30Ztjflx3hGlVzhl3paRIVFJgsyGQ_mg8fF8stLOBNsqmDNpxUycFeKTZIuM=w1454-h622-no)

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

##### `yield()`  method to temporarily release time for other threads

```java
package com.yieldMethodDemo;

public class YieldMethodDemo {

  public static void main(String[] args) {
    BuildThread buildThread = new BuildThread();
    DestroyThread destroyThread = new DestroyThread();
    buildThread.start();
    destroyThread.start();

  }

  static class BuildThread extends Thread {

    public void run() {
      for (int i = 0; i < 50; i++) {
        System.out.println("Build");
        if (i % 2 == 0) {
          Thread.yield();
        }

      }
    }
  }

  static class DestroyThread extends Thread {

    public void run() {
      for (int i = 0; i < 50; i++) {
        System.out.println("Destory");
      }
    }
  }
}
```

##### `join()`  method demo

In `CountingOne ` class's `run()` method once `i==5` then the countingOne thread will stop to wait the countingTwo thread to finish executing.

```java
package com.ThreadJoinMethodDemo;

public class ThreadJoinMethodDemo {

  public static void main(String[] args) {
    CountingOne countingOne = new CountingOne();
    countingOne.start();
  }

  static class CountingOne extends Thread {

    public void run() {
      CountingTwo countingTwo = new CountingTwo();
      countingTwo.start();

      try {
        for (int i = 0; i < 10; i++) {
          if (i == 5) {
            countingTwo.join();
          }
          System.out.println(i);
        }
      } catch (InterruptedException e) {
        System.out.println(e);
      }
    }
  }

  static class CountingTwo extends Thread {

    public void run() {
      for (int i = 10; i < 20; i++) {
        System.out.println(i);
      }
    }
  }

}
```

output:

```java
0
1
2
3
4
10
11
12
13
14
15
16
17
18
19
5
6
7
8
9
```

