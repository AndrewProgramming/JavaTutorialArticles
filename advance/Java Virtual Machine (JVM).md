> Finding more tutorials on [Andrew Programming](http://www.andrew-programming.com)

##Overview

This article describes the Java Virtual Machine (JVM) and its architecture

**JVM** stands for **Java Virtual Machine**. It provides you with environment to execute your compiled programs, called bytecode. There are multiple implementations of JVM from different vendors for variety of platforms. In this article I will explain the main components of JVM, including memory management, class loading and the Garbage collector.

Usually we do not dig deep into the internal mechanics of JVM. If our code works, then we go on without caring much about the internal mechanics… until the day something goes wrong and we need to tweek JVM or fix a memory leak for example.

Java Virtual Machine questions are very popular in job interviews. Interviewers love to ask various questions about JVM to prove your general understanding of the Java platform.

## What is Java Virtual Machine

The Java Virtual Machine is an abstract computing machine that can execute a program written in its machine instruction set, called bytecode.

Like any other virtual machine, the JVM must be implemented on a real computer machine in order to actually run any programs written in the JVM bytecode.

We also need a higher level language like Java and a compiler, so that we create programs quickly in Java and compile it into JVM bytecode. Because writing large programs directly in JVM bytecode is very difficult.

Putting the above together, here is the process of writing and running programs on a JVM:

- Write a program in Java language and save it in .java files. Or we can use other languages (like Jython) that have bytecode compilers.
- Compile .java files into bytecode and save in in .class files.
- Load the .class files into a JVM implemented for your computer,
- The JVM will run your program on your computer.

Here is a simple diagram that illustrates the process of writing and running programs on a JVM:

![JVM Programming Process](http://www.herongyang.com/JVM/JVM-Java-Virtual-Machine-Programming-Process.jpg)

​							 	 **JVM Programming Process**

## Java Virtual Machine Architecture

The Java virtual machine consists of three main areas:

- Class loader subsystem
- Runtime data area
- Execution engine

we will look at each one in greater details

 

![img](https://lh3.googleusercontent.com/T1dHrl3zR8HPAYUDeoM-6oQB0SOiA-Q_RBfpVGosNFo07VAfHa_Itv80cNaGIZV-ig4cTiJ6AzO77oJngD506QCKYHG2jvr4PUQXCnMDh37XPg8JQkTND9kfZC7PH8xhS__0E0yvMPDNZFTNNGhQAzDTAyTq4m6D23j7LXe__3iVnvtVVUX6mWMm68Q5T2pf-Oy-mgIAKgM7ltDPpDCT5ZlQVn1StS6QHA8nBd5XnqRGe4Lw9Qr6i3xHTM1bS9cnY6E265GDGFxsRntroprf_jIwJ0cLTamr2DxRSNJHLDPO-C6mDqRAmNrHjWXah7mR8IN1umJYS0DFo4iMoG7j1LPU38DE0owqrv0qOl9C2CWDfR2YlMXZ3nEUnppPz2cjt7T4cROM-zWZBinQ09ggsRLykcXjGEnl9DeeFqY8PbfoLUCUQK_ke26XqycX1LjWZs-yNv-Tih-EWFDNVtV6RA3_aMq_su39_gNar2VQCtVOJntXZDgdQB0Ed-qUD3lcX24WxTdZ9oiCrs0lgFyaOW0eoL2Fe7ZGAmrOP-OwFulPa7OtIesQsJVhDTWYDEhZZRv2MXYhNJmwQH4fZbz02gWZPUvAH2cIqTQO_r4zQQBuf5-9TyI3NGIT6-Hsux4=w992-h1024-no)



​             								**Java Virtual Machine architecture diagram**

### Class Loader Subsystem

#### Loading

Compiled classes are stored as a .class file. When we try to use a Class, Java ClassLoader loads that class into memory. Classes are introduced into the Java environment when they are referenced by name in a class that is already running. Future attempts at loading classes are done by the class loader, once the first class is running. Running the first class is usually done by declaring and using a static main() method.

There are three types of class loaders:

1. **Bootstrap Class Loader** – It loads JDK internal classes, typically loads rt.jar and other core classes for example java.lang.* package classes
2. **Extensions Class Loader** – It loads classes from the JDK extensions directory, usually lib/ext directory of the JRE.
3. **System Class Loader** –Loads classes from system classpath, that can be set while invoking a program using -cp or -classpath command line options.

#### Linking

Linking a class or interface involves verifying and preparing that class or interface, its direct superclass, its direct superinterfaces, and its element type if necessary.

JVM requires that all of the following properties are maintained:

- A class or interface is completely loaded before it is linked.
- A class or interface is completely verified and prepared before it is initialized.
- Errors detected during linkage are thrown at a point in the program where some action is taken by the program that might, directly or indirectly, require linkage to the class or interface involved in the error.

#### Initialization

Initialization of a class or interface consists of executing its class or interface initialization method or calling the class’s constructor for example.

Because the Java Virtual Machine is multithreaded, initialization of a class or interface requires careful synchronization, since some other thread may be trying to initialize the same class or interface at the same time.

This is the final phase of Class Loading, here all static variables will be assigned with the original values, and the static block will be executed.

### Runtime Data Area

There are five components inside the runtime data area:

#### Method Area

All the class level data will be stored here, including static variables. There is only one method area per JVM, and it is a shared resource.

#### Heap Area

All the Objects and their corresponding instance variables and arrays will be stored here. There is also one Heap Area per JVM. Since the Method and Heap areas share memory for multiple threads, the data stored is not thread safe.

#### Stack Area

For every thread, a separate runtime stack will be created. For every method call, one entry will be made in the stack memory which is called as Stack Frame. All local variables will be created in the stack memory. The stack area is thread safe since it is not a shared resource. The Stack Frame is divided into three sub-entities:

- Local Variable Array – Related to the method how many local variables are involved and the corresponding values will be stored here.
- Operand stack – If any intermediate operation is required to perform, operand stack acts as runtime workspace to perform the operation.
- Frame data – All symbols corresponding to the method is stored here. In the case of any exception, the catch block information will be maintained in the frame data.

#### PC Registers

Each thread will have separate PC Registers, to hold the address of current executing instruction once the instruction is executed the PC register will be updated with the next instruction.

#### Native Method stacks

Native Method Stack holds native method information. For every thread, a separate native method stack will be created.

### Execution Engine

The bytecode which is assigned to the Runtime Data Area will be executed by the Execution Engine. The Execution Engine reads the bytecode and executes it piece by piece.

#### Interpreter

The interpreter interprets the bytecode faster, but executes slowly. The disadvantage of the interpreter is that when one method is called multiple times, every time a new interpretation is required.

#### JIT Compiler

The JIT Compiler neutralizes the disadvantage of the interpreter. The Execution Engine will be using the help of the interpreter in converting byte code, but when it finds repeated code it uses the JIT compiler, which compiles the entire bytecode and changes it to native code. This native code will be used directly for repeated method calls, which improve the performance of the system.

#### Garbage Collector

The Garbage collector (GC) collects and removes unreferenced objects. Garbage Collection can be triggered by calling “System.gc()”, but the execution is not guaranteed. Garbage collection of the JVM collects the objects that are created.

#### Java Native Interface (JNI)

JNI will be interacting with the Native Method Libraries and provides the Native Libraries required for the Execution Engine.

#### Native Method Libraries

It is a collection of the Native Libraries which is required for the Execution Engine.