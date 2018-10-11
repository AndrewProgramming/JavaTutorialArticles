# Introduction

The key benefit of generics is to enable errors to be detected at compile time rather than at runtime.

A generic class or method permits you to specify allowable types of objects that the class or method can work with. If you attempt to use an incompatible object, the compiler will detect that error.

This chapter explains how to define and use generic classes, interfaces, and methods and demonstrates how generics can be used to improve software reliability and readability. 

# Motivations and Benefits

> The motivation for using Java generics is to detect errors at compile time.

Java has allowed you to define generic classes, interfaces, and methods since JDK 1.5. Several interfaces and classes in the Java API were modified using generics. For example, prior to JDK 1.5 the java.lang.The comparable interface was defined as shown in Figure, but since JDK 1.5 it is modified as shown in Figure

![img](https://lh3.googleusercontent.com/3F0nJXmoV9aOTlFP5BHMu0KI8VAaqPuqIojQWbKyozLQM6nXX8OvlLPx5YP11cyNYS3bVHRGmtt5Wm6JOf6ddnKB7y3Vm0tXJTQm0vXKLXHQ8MikZJGNnZ30owDLWp3PBK5-yyxd3bi18KD9ZOwFA7bOwKzIdrRYLfCdtvW_AT8ip5sdKTpc2PAFGUTukjZOOSsvBWtYpaFGtlc0SGge91bs-OaSDVyqYk2_pC8T_JZAzRs5xHYUrYrlZSBU_1ndlDLw3maFR3GIDWZ9o1xlOmQ-SFs7ExTssN375JsXrCKtsmgtRMUwaYmWRermhdGWs3lkX6aNasRwinVfMfRNtHdbH4g61yW1z0MFzheXPTXOEBZqrhAwytA_NMvuCW3e9httUVfHDvrFu-04e4QM8gpiSu4bEJVLx0FsqKl06ZPmMmd9fp1UlZARBJEQgPjWqo66C8KLODGkjN8F7F3avmUqPqYRzmGq370IMQFKXExyI4lqj16v8M3R9stxWQ1KA_V7z_ycoY9FzRdyNvVeS3q2DBV8nsx9S2wlzIC9aq1lVX10g4QKpymbrCC91njl6CRY6Ltm4SylbjdqhgJT-ZSFSEc0ZSf_qKHU3NU8UB6N7BY4-v1UpYkWCCMlz3s=w1120-h196-no)

Here, <T> represents a formal generic type, which can be replaced later with an actual concrete type. Replacing a generic type is called a generic instantiation. By convention, a single capital letter such as E or T is used to denote a formal generic type.

The figure below shows the version of ArrayList before and after JDK 1.5

![img](https://lh3.googleusercontent.com/EN7j_SzZedBP1z4ub3TBLTuOWaM6RakG3_RoLz-9LdgkewkxJscWNYiv77aTVdi5_iz3rl8uwDEfYep0B2J83CMtRbaI0xUMtjyY3eximKvqMW7BiTL_tBYKI3fCBcUzFgYQtELm-WfIx1clnuR0Nk9RAr0VcrHPfjes8I4kWMoeO0ULpFE7J_Cs3LMsZFArRT4c0HdIKuKoKvCUrQi_-WssxbzgNlBcMI85yoTiQs1nXdef0226IKmQmi1OqbB9DTqu1uhXwKr72u4ZN6ezYQwEWnjSLxRQz65B-lynKQT_yg8i7oFPWPO_8JDKqnaIWx96InSQM7LmF03aAt4FQW7IFlfHnVUMz_327ELPh4joHCvig6-akXSXDLL9nHwTICUIFI7Nf70VZQEGlGdyoi6n177b8dzw49syTqUTYNJQ3KbCSbdhzEDkwRK5yBbbrQqHUB5XZrb3J-mgenrNMRx-gUOGR1zB8HiPeRX8Ph44ukqZg00nNqVtB_GfgShug3NcYwLbQyBXLPro-xmon1r9n0adr-uFojTS0_XyDi38JcaWRDO5ktws_lqnp0QtTov3zpbiepLZxdCIsFcg_cXgg7k5fZ16hMWh8_c92dqg7L0jU-uAyp_uj9h7tas=w1382-h616-no)

So why do we need this change?

Let's see an example below by given the ArrayList a specific type "String" we can detect the error in compile time instead of Runtime if we add an Integer to this list.

```java
import java.util.ArrayList;

public class GenericsDemo {

    public static void main(String[] args) {
        ArrayList<String> arrayList = new ArrayList<String>();
        //This works fine because add a String
        arrayList.add("Andrew Programming");
        //This leads an error since add an integer
        // we can detect the error in compile time instead of runtime
        arrayList.add(1);

    }
}
```

What would happen if we don't use generics? Let's see example below as comment demonstrate we cannot detect the error in compile time but in Runtime because lack the help of Generics.

```java
import java.util.ArrayList;

public class BadExample {

    public static void main(String[] args) {
        ArrayList noGenericList = new ArrayList();
        //This ArrayList is supposed to contain String item but infact we add Integer to it
        // which leads to error in Runntime
        noGenericList.add("Andrew Programming");
        noGenericList.add(1);

        for (int i = 0; i < noGenericList.size(); i++) {
            //We want to convent the item in the list to uppercase but there is a Integer in it which will lead error
            String arrayItem = (String) noGenericList.get(i);
            arrayItem.toUpperCase();
        }

    }
}
 
```

```java	
Exception in thread "main" java.lang.ClassCastException: java.base/java.lang.Integer cannot be cast to java.base/java.lang.String
	at BadExample.main(BadExample.java:11)

Process finished with exit code 1
```

