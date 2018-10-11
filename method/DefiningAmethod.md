## Defining a Method

![img](https://lh3.googleusercontent.com/YFGNzvnnLBKnec8ilwmAJG9_5CygjU0qgKcjGtyNplhM1SERzWsFX65xie2fdJRRkNq4r4TOJeolVlC5SCmhUaJ6Iv6yJOWCdvTcvQ94eqIjW5dMYdrnKokBys5bKXO9K4pj39J6lpHl5IhezZxmUlW4MWXKJ-eTfTgeVVMI5JtILHZpXqMvBkcCqcaYz8jubEe0A1QGrVcSDHgHQE2puntU5tbNGoqE5eW8XEWdbfwCdrct8C5na_BF6q66-oZ2u6sGdCo9NMG1jNqF4KTbx8f9NOMBGHSyF014wIjjwHl3V2s01RSyGZ3oKvYSlMFq4syfpzq1nTbkdYiYahDcnnwX66PX4Z2b-90RtZmpDJSwddBd7rVtovqUR9Ctfu8wYtlIVGlrIdwwj3RpzVYNwvbkZhYzHqDL3J0crQvLbuPH3fWByYp6KTE0in6i58_nm92dfufqb6VP1AiP2Lxn_9QrmNV8xQVTBOrYA6oBzYiN4om_pZ0dGKDKtbI3T83WDyLi7LlFGMtlHOXkRjbQ5DLfNd_7jER-mij22ctEba4-unsRsHrUABZtES-mAmSJPscQT3FTneDYs0u4HyxQro-c6jGey-JarR4KXBE_4vAbJJHRZ9yCb8p9iShWs4I=w1240-h506-no)

Here is an example of a typical method declaration:

The only required elements of a method declaration are the method's return type, name, a pair of parentheses, `()`, and a body between braces, `{}`.

More generally, method declarations have six components, in order:

1. Modifiers—such as `public`, `private`, and others you will learn about later.
2. The return type—the data type of the value returned by the method, or `void` if the method does not return a value.
3. The method name—the rules for field names apply to method names as well, but the convention is a little different.
4. The parameter list in parenthesis—a comma-delimited list of input parameters, preceded by their data types, enclosed by parentheses, `()`. If there are no parameters, you must use empty parentheses.
5. An exception list—to be discussed later.
6. The method body, enclosed between braces—the method's code, including the declaration of local variables, goes here.

## Naming a Method

Although a method name can be any legal identifier, code conventions restrict method names. By convention, method names should be a verb in lowercase or a multi-word name that begins with a verb in lowercase, followed by adjectives, nouns, etc. In multi-word names, the first letter of each of the second and following words should be capitalized. Here are some examples:

```java
run
runFast
getBackground
getFinalData
compareTo
setX
isEmpty
```

Typically, a method has a unique name within its class. However, a method might have the same name as other methods due to *method overloading*.

## Overloading Methods

The Java programming language supports *overloading* methods, and Java can distinguish between methods with different *method signatures*. This means that methods within a class can have the same name if they have different parameter lists (there are some qualifications to this that will be discussed in the lesson titled "Interfaces and Inheritance").

Suppose that you have a class that can use calligraphy to draw various types of data (strings, integers, and so on) and that contains a method for drawing each data type. It is cumbersome to use a new name for each method—for example, `drawString`, `drawInteger`, `drawFloat`, and so on. In the Java programming language, you can use the same name for all the drawing methods but pass a different argument list to each method. Thus, the data drawing class might declare four methods named `draw`, each of which has a different parameter list.

```java
public class DataArtist {
    ...
    public void draw(String s) {
        ...
    }
    public void draw(int i) {
        ...
    }
    public void draw(double f) {
        ...
    }
    public void draw(int i, double f) {
        ...
    }
}
```

Overloaded methods are differentiated by the number and the type of the arguments passed into the method. In the code sample, `draw(String s)` and `draw(int i)` are distinct and unique methods because they require different argument types.

You cannot declare more than one method with the same name and the same number and type of arguments, because the compiler cannot tell them apart.

The compiler does not consider return type when differentiating methods, so you cannot declare two methods with the same signature even if they have a different return type.