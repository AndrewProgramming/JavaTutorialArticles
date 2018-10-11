#Examples

##Compute Factorial

```java
public class Factorials {
    public static void main(String[] args) {
        int r = computeFactorials(3);
        System.out.println(r);
    }

    public static int computeFactorials(int n) {
        if (n == 1) {
            return 1;
        } else {
            return n * computeFactorials(n - 1);
        }
    }
}
```

###Invoking factorial(4)  spawns recursive calls to factorial .

![img](https://lh3.googleusercontent.com/uCTXg_-KLo_jbQcMDO144c42WD5n6V5Ehx1at7wZcXiNZX69CmBIJbUgYGlJ7qETLpb6C0v-0FOMZ4Ged9yjSgE4sl-VFlmWCwvrIPsO7eHXtRI32BnSc4blny3M6wB1XWQqP7Tn44RC3GvaQff7Z_RCg0plNPDD6vku_K47a3CHsQOyNvfoYfIxeNfK1XjrrnOl02JB4WuHryz5CaOqQ3Gm03v0jx96NjjAL8qtwG7pJAc5in6GHkmhBCOboWDw-fiirYduRBCpM0mVGxBBN4c1VbtyrFn_GNb31B1hOB_UXuYgb-Eym6-A4wqLGmQ3Ubc_2SHaIaXfUcF09myJNfIsykUQpVnWnX31Ol9B7xBF4bihcuEJMymUNRuEqrC2oEjBWI-PmeuSOvS-ihlgiN6iuK0hG5GYCr2VtqgGL6ypUCKk8EBsgtwWyCwvTDC-1FN9069Dgqq1-3vyJIPEsVfq7nOOVWp9WapokSJdc08HHuWoGoYQOVzufO6lxQoRkwpj62yGUrd0KlIYjoYpFGNL-lhWQQyxL6WvHpaCqnBc0gK4WoufnE83cDLCBC3qTx4m8UXQVj43WCL4yEFD7DZYdTURhwU0JZBXFrNj22RKveFIt1KQT9tveu7ZdkQ=w1230-h680-no)

> Recursive programs can run out of memory, causing a StackOverflowError.

> If you are concerned about your program’s performance, avoid using recursion, because it takes more time and consumes more memory than iteration. In general, recursion can be used to solve the inherent recursive problems such as Tower of Hanoi, recursive directories, and Sierpinski triangles.

![img](https://lh3.googleusercontent.com/bbiUNEpo-80uRg8FiL7PWZFkU8zbde_rWo0js87s4lRvNBfpgxMD6lavNFRfrFPZ0yxJ2P7ruF0_7VzDX6DwK9Q-PI9jFlVjvzKuYrmlbOF7LoIUVeXkj1VZKORoIqFkqnmxyOZVDyawfxL8A43QEXd4Snt-ty3qaPJ4sSh9iW5diVylzyuz9UWVmA_16hBwFKE6a4X0IeZRuPMrsOIVJxIMCYRzFJrfpuA-GJw-XbAcZr1s0c0AM6QfOX_f33_zD9iiFCC0_AS89mJ-YMnMO0p25m2fulQ3GIhw5RtGhdUfmgjuQxSwuS9ASBqQtX-8gU0g4FZmMFFXo-pbqA44TELKdN5PEfYUH8GmQPUR3T8uXT-KxKRCbCGLd13ZVwr9BRwHyu_j7PbjtZ50ArKq3zgYqibdqU_9YK_yOqrB7--LvWYyUBdLrNFBZPW3p_4oDBfLbOKvKL5-CuKwGuxoGOKeof0FioqC2zWEfwKrUc8H5kKEP8_HHHO_XuvugNdDwpgeYgoyxrbjQ_FYVCUKTJi4uiAIJ-NGx-f0i26deVopcWQU7HiozEzmB1l5grVQ4bz-PaCi5xKn7yGcAre6-icqRkc605VGWL_IF7a4Wv-zKOhzyjKdCBBeBobwOwI=w1568-h1098-no)

##Write a recursive mathematical definition for computing 1 +  2 +  3 + c + n  for a positive integer n .

```java
public class plusFactor {
    public static void main(String[] args) {
        System.out.println(computePlusFactor(3));

    }

    public static int computePlusFactor(int n) {
        if (n == 1) {
            return 1;
        } else {
            return n + computePlusFactor(n - 1);
        }
    }
}
```



## Write a recursive mathematical definition for computing $2^n$  for a positive integer n .

```java
public class TwoFactor {
    public static void main(String[] args) {
        System.out.println(computeTwoFactor(4));
    }

    public static int computeTwoFactor(int n) {
        if (n == 0) {
            return 1;
        } else {
            return 2 * computeTwoFactor(n - 1);
        }
    }
}
```

## Write a recursive mathematical definition for computing $x^n$  for a positive integer n and a real number x .

```java
public class XN {
    public static void main(String[] args) {
        System.out.println(computeXN(3, 0));

    }

    public static int computeXN(int x, int n) {
        if (n == 0) {
            return 1;
        }
        if (n == 1) {
            return x;
        }
        return x * computeXN(x, n - 1);
    }
}
```

## Case Study: Computing Fibonacci Numbers

```java
import java.util.HashMap;
import java.util.Map;

public class Fibonacci {
    private static Map<Integer, Integer> map = new HashMap();

    public static void main(String[] args) {
        System.out.println(computeFibonacci(30));

    }

    public static int computeFibonacci(int n) {
        if (map.get(n) != null) {
            return map.get(n);
        }

        if (n == 0) {
            return 0;
        } else if (n == 1) {
            return 1;
        } else {
            int v = computeFibonacci(n - 1) + computeFibonacci(n - 2);
            map.put(n, v);
            return v;
        }
    }
}
```

### Invoking fib(4)  spawns recursive calls to fib .

![img](https://lh3.googleusercontent.com/_wAOISr3193j1e2UcH5Q_mrJKN2HOpzIpCwMJzRNLATPba9VPau_L5YgqRVdB7t3Nl6oH7yLSTBiYuLweovGP_t0ujT4TMN44ZKmItWePy_z5Myosj9aCDQAKAjcbECVo-LOIWmO9LltWhjZJ_Q2q1UDSFi_KdK4BBivpAEHv_3-vAHSQVVgqXfRGZgNtWuHYOlSCIdht09GUUbnCyNWDL7-_nEz5LTpqb9OJpNGxMqjxUGt6giCKmHfwG6ahjeEMeho8vicqUXhONKYBzN1DAcY_zG8gVWXuoZ_ihA2CQAYa3XQA01hWV7KnXki2cbjjeGGiXiTzfo05X3wLrO1-LXZPXZbN3PXn6UdUn_oR2LrGzImpZNFlR4MbUairsmyTZgQ-pVWUyPfooFHdGGOsI4FChoihyT5uEUwUtXMqq59qiiTdkSUXwWRdBByG7FnB-1lirkJgKpeNFXMaXETk1MpD-35ry5jgloJUaGrnPhFDhgzozbYlpLP7w7Eg0SuQBhLqQiLxoB-egJ0GnJzhBnEKOD9CjLgI5GUufvsF5ggeD-VA7OAbVW942CaW4pKbt7dnVLFnwP3nmLDjTKj3nSx8XJdGxMvg1PhwngZBswLcEbgXEAhKgiKj-hlqx4=w1622-h578-no)

## Compute File Size

```java
import java.io.File;

public class GetFileSizeDemo {

    public static void main(String[] args) {

    }

    public static int getFileSie(File file) {
        int fileSize = 0;
        if (file.isDirectory()) {
            System.out.println(file.getAbsolutePath());
            File[] files = file.listFiles();
            for (File fileItem : files) {
                fileSize += getFileSie(fileItem);
            }
        } else {
            fileSize += file.length();
            System.out.println(file.getName());
        }
        return fileSize;
    }
}
```