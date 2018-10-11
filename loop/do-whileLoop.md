#do-while Loop

![img](https://lh3.googleusercontent.com/YhxDxuFipx5HEivhAaLIjULH3Cn_V6GIU1IbZE8QbiK3ZGSVo4wY2KCDo3vbrl-bnBPobAAwVI8_LckvlLRChTB_VaJGGWSIoPvE0QFvUETLhhSk8BuM2kHRitpsVec7dF3zxruHYWWGSz6CmaoQ9F9-P9oBFcTXHHbBIG_q1RUrnEDAA9w1C-flC9E-_EFB7hcGey1qO95SfE4blG6nV1Mb0zLo29MfdsxmIZ-5a_uh7W_Nsc-fWPfBbUNc0uCv8kgzhcFA2LNFvMih4uCkp7MDyUncUkb4iHJFtIt-KMIHxkvXDauM1UnVr3zCgVdyU7BaDCCeZCCmGykV4R4oYy3tXKHYxpEZt7ExDm-7remv7W_hGQwfyZa0bOW6Mj_q0aU5rxZQaFS6KaPZ78SKykIYsQ6LwntfGWe7E2nCCI1MnGw4XZRsZBWpDAKkstn3bRmFv6jYmAv2vn2k6IVcy_KDIF7RrFR4Rmsi8myc4aAw9oaw0j5-_S3hX5wqicBqmOtGFbQFdqu_miv2u5GIfohuli6xiWRG2zOxt9yE1SC-BAvIvSnAYywgvqWPhzTVZayRNLv42Lg_JaQ6IscEvda1zPNUeWO33nyS1mPqg00uOCu5aUD6u0IWOpn65H0=w270-h304-no)

The Java programming language also provides a `do-while` statement, which can be expressed as follows:

```java
do {
     statement(s)
} while (expression);
```

The difference between `do-while` and `while` is that `do-while` evaluates its expression at the bottom of the loop instead of the top. Therefore, the statements within the `do` block are always executed at least once, as shown in the following `DoWhileDemo` program:

```java
class DoWhileDemo {
    public static void main(String[] args){
        int count = 1;
        do {
            System.out.println("Count is: " + count);
            count++;
        } while (count < 11);
    }
}
```

