## Thread Pool

>  A thread pool can be used to execute tasks efficiently.

 In Section before, Creating Tasks and Threads, you learned how to define a task class by implementing

`java.lang.Runnable` , and how to create a thread to run a task like this:

```java
Runnable task = new TaskClass(task);

new Thread(task).start();
```

This approach is convenient for a single task execution, but it is not efficient for a large number of tasks because you have to create a thread for each task. Starting a new thread for each task could limit throughput and cause poor performance. Using a thread pool  is an ideal way to manage the number of tasks executing concurrently. Java provides the Executor  interface for executing tasks in a thread pool and the ExecutorService  interface for managing and controlling tasks. ExecutorService  is a subinterface of Executor , as shown in Figure below