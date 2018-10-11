#Calling a method

> After define a method you should call it.

## Method type 

In Java there are two type of method:

- static method
- instance method

Different method have different way of calling.

## Calling static method



## Calling a method with return value

Suppose we define a method called `SumTwoInteger(int i,int j)`:

```java	
public static int sum(int i,int j){
    int result = i+ j;
    return result;
}
```

you can call it like this:

```java	
int r = sum(1,2)
```

`r` will be assgined a value 3.

## Calling a method without return value

Suppose we define a method called `diaplyHello()`:

```java	
public static void displayHello(){
    System.out.println("Hello");
}
```

Since the return type is `void` this method will have no return value.

>  In Java ,the reserved keyword `void` means this method will have no return value.

Then you can call it like this:

`dispalyHello()`

and this line of code will display:

`Hello` on you console.

### 







 