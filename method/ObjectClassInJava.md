#Introduction to Object class and toString() method

Every class in Java is descended from the `java.lang.Object` class.

If no inheritance is specified when a class is defined, the superclass of the class is Object by default. For example, the following two class definitions are the same:

```java
public class ClassName {

...

}

is equivalent to

public class ClassName extends Object {

...

}
```

Classes such as String, StringBuilder, Loan, and GeometricObject are implicitly subclasses of Object (as are all the main classes you have seen in this book so far). It is important to be familiar with the methods provided by the Object class so that you can use them in your classes. This section introduces the toString method in the Object class. The signature of the toString() method is:

`public String toString()`

Invoking `toString()` on an object returns a string that describes the object. By default, it returns a string consisting of a class name of which the object is an instance, an at sign (@),and the object’s memory address in hexadecimal. For example, consider the following code for the Loan class defined in Listing 10.2:

```java	
Loan loan = new Loan();
System.out.println(loan.toString());
```

The output for this code displays something like Loan@15037e5. This message is not very helpful or informative. Usually you should override the toString method so that it returns a descriptive string representation of the object. For example, the toString method in the `Object` class was overridden in the GeometricObject class in lines 46–49 in Listing 11.1 as follows:

```java
public String toString() {

return "created on " + dateCreated + "Äncolor: " + color +

" and filled: " + filled;

}
```

# equals method

Like the` toString()` method, the equals(Object) method is another useful method defined in the `Object` class.

 Another method defined in the Object  class that is often used is the equals  method. Its signature is 

```java
public boolean equals(Object o)

```

 This method tests whether two objects are equal. The syntax for invoking it is:

```java	
object1.equals(object2);
```

 The default implementation of the equals  method in the Object  class is:

```java	
public boolean equals(Object obj) {

return (this == obj);

}
```

This implementation checks whether two reference variables point to the same object using the `==  `operator. You should override this method in your custom class to test whether two distinct objects have the same content.The equals  method is overridden in many classes in the Java API, such as `java.lang.String`  and `java.util.Date` , to compare whether the contents of two objects are equal.

You have already used the equals  method to compare two strings in Section 4.4.7, The `String`  Class. The equals  method in the String  class is inherited from the Object  class and is overridden in the String  class to test whether two strings are identical in content.

You can override the equals  method in the Circle  class to compare whether two circles are equal based on their radius as follows:

```java	
public boolean equals(Object o) {
	if (o instanceof Circle)

		return radius == ((Circle)o).radius;

	else

	return this == o;
}


```