# List of Reserved Java Keywords

**Java reserved words** are keywords that are reserved by Java functions or other uses that cannot be used as identifiers (e.g.,variable. If a reserved word was used as a variable you would get an error or unexpected result. The list of reserved words in Java is provided below.

| abstract   | assert       | boolean    | break   | byte      | case      |
| ---------- | ------------ | ---------- | ------- | --------- | --------- |
| catch      | char         | class      | const   | continue  | default   |
| double     | do           | else       | enum    | extends   | false     |
| final      | finally      | float      | for     | goto      | if        |
| implements | import       | instanceof | int     | interface | long      |
| native     | new          | null       | package | private   | protected |
| public     | return       | short      | static  | strictfp  | super     |
| switch     | synchronized | this       | throw   | throws    | transient |
| true       | try          |            |         |           |           |

# What Happens If You Use a Reserved Word?

Let's say you try to create a new class and name it using a reserved word, like this:

```java
 // you can't use finally as it's a reserved word!
class finally {
   public static void main(String[] args) {
      //class code..
   }
}
```

Instead of compiling, the Java program will instead give the following error:

`class or interface expected`

