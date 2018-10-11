# What is method overloading?

Overloading methods enables you to define the methods with the same name as long as their signatures are different.

#Why do we need Method Overloading ?

If we need to do same kind of the operation with different ways i.e. for different inputs. In the example described below, we are doing the addition operation for different inputs. It is hard to find many different meaningful names for single action.In fact ,we don't need to do so but just giving the method different type of parameters.Java will consider these method are different even though their names are the same.

```java
public int addTwoNumber(int a, int b) {
    return a + b;
}

public float addTwoNumber(float a, float b) {
    return a + b;
}

public double addTwoNumber(double a, double b) {
    return a + b;
}
```

#Different ways of doing overloading methods

Method overloading can be done by three ways.

- The number of parameters in two methods.

  - ```java
    public void sayHi(String name, String words) {
        System.out.println(name + "says " + words);
    }
    
    public void sayHi(String words) {
        System.out.println("says " + words);
    
    }
    ```

- The data types of the parameters of methods.

  - ```java
    public int addTwoNumber(int a, int b) {
        return a + b;
    }
    
    public float addTwoNumber(float a, float b) {
        return a + b;
    }
    
    public double addTwoNumber(double a, double b) {
        return a + b;
    }
    ```

- The Order of the parameters of methods.

  - ```java
    public class ByOrderDemo {
        public void demoMethod(int a, double b) {
    
        }
    
        public void demoMethod(double a, int b) {
    
        }
    }
    ```

# Questioin

What is method overloading? Is it permissible to define two methods that have the same name but different parameter types? Is it permissible to define two methods in a class that have identical method.