# The for Statement

![img](https://lh3.googleusercontent.com/Jm4G9KzX3h9HndOZF4wI6jAZQ0GYUgDdFTfffo7fqa3wrBA3rDp4lYXUT-KF7cz3WsSwgBxx8l725TknhdvfW55C5mqsr4Moka5bXjtLnrk7Dtnrl5GTy-G74rMGN9LQafyPd4z1GC5QAQ3Axgj9ShhchSAHQjTpaOQmRcw6bySTs6aINJDZu6DIUeNRttvCmPZYUzLfdRW3XzN49aPj4BGp7Nbsz5XGCaIiz47GWSD3fTijGwCtqB7CzNZNe8KwmbAh6nxF9ixXhmrmJuXFqFoRO4j5-RrA2a-d1AV8Y5_1ZLNmDVLIdXTdIAHi-JcLdR0uGZY4NjP6_Vqr1PlV7IMmwKxuCds5FpcXwQ6mU2ZS9xG0Ey-dcRkrcrahnp3L19gR4lAHyb5zMOVmymTk4xiWElPiDma0I5VwmOTP8h7p_KSvSAZdhGpHUX5FqkBdc064mXJLngONXRMxTR3aHyfRwiwYzgtEixUln04GXNbsuZqB_AhnVL019cy9iIVZ6KqDWE2eXhruBBi2n1qDmUveRYpBu80xv0q7nd_45aADdcQ7Z5jg4aCxlnr-Mk8J4Q7qJiM9hZ0Bmjqpl2gDcfNgG9S1sgN-vRdEkP4p23Djyyo3FjCk_HtqBQw-DdE=w548-h225-no)

##Simple for Loop

The `for` statement provides a compact way to iterate over a range of values. Programmers often refer to it as the "for loop" because of the way in which it repeatedly loops until a particular condition is satisfied. The general form of the `for` statement can be expressed as follows:

```java
for (initialization; termination; increment) {
    statement(s)
}
```

When using this version of the `for` statement, keep in mind that:

- The *initialization* expression initializes the loop; it's executed once, as the loop begins.
- When the *termination* expression evaluates to `false`, the loop terminates.
- The *increment* expression is invoked after each iteration through the loop; it is perfectly acceptable for this expression to increment *or* decrement a value.

The following program, [`ForDemo`](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/examples/ForDemo.java), uses the general form of the `for` statement to print the numbers 1 through 10 to standard output:

```java
class ForDemo {
    public static void main(String[] args){
         for(int i=1; i<11; i++){
              System.out.println("Count is: " + i);
         }
    }
}
```

The output of this program is:

```java
Count is: 1
Count is: 2
Count is: 3
Count is: 4
Count is: 5
Count is: 6
Count is: 7
Count is: 8
Count is: 9
Count is: 10
```

Notice how the code declares a variable within the initialization expression. The scope of this variable extends from its declaration to the end of the block governed by the `for` statement, so it can be used in the termination and increment expressions as well. If the variable that controls a `for` statement is not needed outside of the loop, it's best to declare the variable in the initialization expression. The names `i`, `j`, and `k` are often used to control `for` loops; declaring them within the initialization expression limits their life span and reduces errors.

##An Infinite for loop

The three expressions of the `for` loop are optional; an infinite loop can be created as follows:

```java
// infinite loop
for ( ; ; ) {
    // your code goes here
}
```

##Enhanced for Loop

Since Java 5, we have a second kind of *for* loop called the *enhanced for* *which* makes it easier to iterate over all elements in an array or a collection.

The syntax of the *enhanced for* loop is:

```java
`for``(Type item : items)``  ``statement;`
```

Since this loop is simplified in comparison to the standard for loop, we need to declare only two things when initializing a loop:

1. The handle for an element we’re currently iterating over
2. The source array/collection we’re iterating

Therefore, we can say that: **For each element in items, assign the element to the item variable and run the body of the loop**.

Let’s have a look at the simple example:

```java
`int``[] intArr = { ``0``,``1``,``2``,``3``,``4` `}; ``for` `(``int` `num : intArr) {``    ``System.out.println(``"Enhanced for-each loop: i = "` `+ num);``}`
```

We can use it to iterate over various Java’s data structures:

Given a *List<String> list* object – we can iterate it:

```java
`for` `(String item : list) {``    ``System.out.println(item);``}`
```

We can similarly iterate over a *Set<String> set*:

```java
`for` `(String item : set) {``    ``System.out.println(item);``}`
```

And, given a *Map<String,Integer> map* we can iterate over it as well:

```java
`for` `(Entry<String, Integer> entry : map.entrySet()) {``    ``System.out.println(``      ``"Key: "` `+ entry.getKey() + ``      ``" - "` `+ ``      ``"Value: "` `+ entry.getValue());``}`
```

Let's see an concrete example. consider the following array, which holds the numbers 1 through 10:

```java
int[] numbers = {1,2,3,4,5,6,7,8,9,10};
```

The following program,uses the enhanced `for` to loop through the array:

```java
class EnhancedForDemo {
    public static void main(String[] args){
         int[] numbers = 
             {1,2,3,4,5,6,7,8,9,10};
         for (int item : numbers) {
             System.out.println("Count is: " + item);
         }
    }
}
```

In this example, the variable `item` holds the current value from the numbers array. The output from this program is the same as before:

```java
Count is: 1
Count is: 2
Count is: 3
Count is: 4
Count is: 5
Count is: 6
Count is: 7
Count is: 8
Count is: 9
Count is: 10
```

We recommend using this form of the `for` statement instead of the general form whenever possible.