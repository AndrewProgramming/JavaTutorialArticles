#Relationship in Java

Type of relationship always makes to understand how to reuse the feature from one class to another class. In java programming we have three types of relationship they are.

- Is-A Relationship
- Has-A Relationship
- Uses-A Relationship

### Is-A relationship

In Is-A relationship one class is obtaining the features of another class by using inheritance concept with extends keywords.

In a IS-A relationship there exists logical memory space.

![ Is-A relation](https://www.sitesbay.com/java/images/Relationship-In-Java/Is-A-relation.png)

###Example

```java
package com.andrewProgramming;

class Faculty {

  float salary = 30000;
}

class Science extends Faculty {

  float bonous = 2000;

  public static void main(String args[]) {
    Science obj = new Science();
    System.out.println("Salary is:" + obj.salary);
    System.out.println("Bonous is:" + obj.bonous);
  }
} 
```

Output

```java
Salary is: 30000.0	
Bonous is: 2000.0
```

###Has-A relationship

In Has-A relationship an object of one class is created as data member in another class the relationship between these two classes is Has-A.

In Has-A relationship there existed physical memory space and it is also known as part of or kind of relationship.

![ Has-A relation](https://www.sitesbay.com/java/images/Relationship-In-Java/Has-A-relation.png)

###Example

```java
package com.andrewProgramming;

class Employee {

  float salary = 30000;
}

class Developer extends Employee {

  float bonous = 2000;

  public static void main(String args[]) {
    Employee obj = new Employee();
    System.out.println("Salary is:" + obj.salary);
  }
}  
```

Output

```java
Salary is: 30000.0	
```
