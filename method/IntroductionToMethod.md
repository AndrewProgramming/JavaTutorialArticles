# Method

> Methods can be used to define reusable code and organize and simplify coding.

![img](https://lh3.googleusercontent.com/0fymDuekiDEcBo6qxg7qDN7pED0sStH3uXlo8uTPurqTTFxd_oMi0AYG7Ff1C_DKvFgSNFyLXUIlxP74RSW1rsIuz1tmfOvKUknxBUlccH222WStnqb4necD53qmffy_1oJAGq5nQEnNArb0-LZE9V_z6-MXjcia8Ei41nBLyPFwmo0S--NltaNIpCpKngBaEMsuPDns-O20HDuRUz-tpn2E1sUHRZfttpgbbvSllD7r6CrHmCjm3Fpw42RDkAjYM4n5fT6Qvvc9mi4_CFxYI0rpHQfW-xHunZGRMWDgLARmW0A7_WYKyzKUP9CRDpHV01gXis-8U7JJtoAXHgZARz4uC0Tok2Ul6bRgHfFz40UMn7DWqmp3d05Vz7LQXlKCCsgtVAqVcaXmIpZKJUsl-k_b5u-iuhDm8fG38aW7tB3Mt1161dvp8Ph6NSRJcazznDnpPMJiO3zrcs7anJkKZFvn3c5OPeSZvEfJHqs99CHetHYEqXL15uzqhlVJZBV0FRv5C4VH3ACT5nrLpxVseciYkNSYviJXmgko_Iyr2D3RjnMRYjEGdVUtwCBE8gIsgxmvgwvtrizAf2f4OWoKD6GTzn-6ESi-NH0RlOEfHQdYjegodQD4jW0oK9KFqOM=s1080-no)

## Why need a method?

Suppose that you need to find the sum of integers from 1 to 10, from 20 to 37, and from 35 to 49, respectively.

You may write the code as follows:

```
int sum = 0;
for (int i = 1; i <= 10; i++){
    sum += i;
    System.out.println("Sum from 1 to 10 is " + sum);
}


sum = 0;
for (int i = 20; i <= 37; i++){
    sum += i;
    System.out.println("Sum from 20 to 37 is " + sum);
}


sum = 0;
for (int i = 35; i <= 49; i++){
    sum += i;
    System.out.println("Sum from 35 to 49 is " + sum);
}
```

Wouldn’t it be nice if we could write the common code once and reuse it? We can do so by defining a method and invoking it.

Think about the code below:

```
public void sumNumber(int i,int j){
    int sum =0;
    for(int counter=i;counter<=j;counter++){
        sum=sum+counter;
    }
    return sum;
}
```

Now all you need to do is calling this method three times:

```
sumNumber(1,10);
sumNumber(20,37);
sumNumber(35,49);
```

See, with just a couple lines of code we achieve the same goal.

That's the magic of Method！

## What are the advantages of using methods?

- The main advantage is code reusability. You can write a method once, and use it multiple times. You do not have to rewrite the entire code each time. Think of it as, "write once, reuse multiple times."

- Methods make the code more readable and easier to debug. For example, the `getSalaryInformation()`method is so readable, that we can know what this method will be doing than actually reading the lines of code that make this method.

## Types of Java methods

Depending on whether a method is defined by the user, or available in the standard library, there are two types of methods:

- Standard Library Methods
- User-defined Methods

The standard library methods are built-in methods in Java that are readily available for use. These standard libraries come along with the Java Class Library (JCL) in a Java archive (*.jar) file with JVM and JRE.

For example,

- `print()` is a method of.`java.io.PrintSteam` The prints`print("...")` the string inside quotation marks.
- `sqrt()` is a method of the `Math`class. It returns the square root of a number.

Here's a working example:

```
public class Numbers {
    public static void main(String[] args) {
        System.out.print("Square root of 4 is: " + Math.sqrt(4));
    }
}
```

When you run the program, the output will be:

```
Square root of 4 is: 2.0
```

------

## User-defined Method

You can also define methods inside a class as per your wish. Such methods are called user-defined methods. We will talk about it in the later chapter.