#### Introduction

Multithreading enables multiple tasks in a program to be executed concurrently.One of the powerful features of Java is its built-in support for  multithreading—the concurrent running of multiple tasks within a program. In many programming languages, you have to invoke system-dependent procedures and functions to implement multithreading. This chapter introduces the concepts of threads and how multithreading programs can be developed in Java.

#### Thread Concepts

A program may consist of many tasks that can run concurrently. A thread is the flow of execution, from beginning to end, of a task.

A thread  provides the mechanism for running a task. With Java, you can launch multiple

threads from a program concurrently. These threads can be executed simultaneously in multiprocessor

systems, as shown in Figure a

![img](https://lh3.googleusercontent.com/tm9_gG_60pEgtbQqZx7NuoMgU_kCmBbACUd97U9b7K0aPdxwTTDy8XLlvoaIcGtF90cLmcuXvZIYK4xNMJCKs8WcHia6YdnKQDUmfElhOmUb8kJekwziFJRzM9fRakRESLdPHUplYNCBkPF_pNc7M1BHdL3D73SZ029ygBI0ZoxKik5JTYzV38brVujNJmihPbZEz3C9Ai3Wuk0M2BwDXAzMA4XXieVY28UiWIS2zDIXyl2imsbkIuPJFfQub5W1LjafiCR9Bv10CW6moqOlATUPBz5fNWtATFZ30IRyuSif0xe9VJ9E3a_9sgAMQ2ktMyEbpracrvHeJ-vok-3H_Wj06VKe7YQZCitm8IoBoUAkmgjsb4hVkaPnvUghioNHw3F3R0fzhOuDhPXdzSFUWm1yz8vONr1_l5YoToW3FBNOAjqMIOOXMnM6-ObZC3yFU6odI-Yxx6SsveHgssuHryqh3lxytnOjHMvwt1X2z7puQy1zdtR6I9_lYjy3jF8REakYk-KJAM02hJRYq-R6DnaHXSdJqs98Hbs5n1qvR0phdM0au4R-cn7VlmNci9967ndOZHN2rXXQp2CYZhzAWOuSLIYBMexjDz7AXYnu8hvjV6_iQz92mZAZrcgPXGw=w1146-h268-no)

- (a) Here multiple threads are running on multiple CPUs. 
- (b) Here multiple threads share a single CPU.

In single-processor systems, as shown in Figure b, the multiple threads share CPU time, known as time sharing , and the operating system is responsible for scheduling and allocating resources to them. This arrangement is practical because most of the time the CPU is idle. It does nothing, for example, while waiting for the user to enter data.

Multithreading can make your program more responsive and interactive, as well as enhance performance. For example, a good word processor lets you print or save a file while you are typing. In some cases, multithreaded programs run faster than single-threaded programs even on single-processor systems. 