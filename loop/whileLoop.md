# The while Statements

![img](https://lh3.googleusercontent.com/khzgQt7tPmNMxF-sw8hobSaYzOyIx7KjLA0cByLheyrQZensdEKYRX3-xgKkcobtfufDUl-bPO2Uuvdm-lEDFFPd9iwCTsmS9PGeKUWAWl1o3dvmCzR6_TU7PWG0A9ewdgw44BKQ5ddHymvzBRUjQ7mfKGkAs_mEY_k35RKTxFbqEL9Su4t9e5-zqp-JLoRDm-_yfeS1cMpvG8kCfXQehz0AG4BtmESZDEAmfB9gXWfqK2tkrT1IOsqQ0qI_aTiBkRQc8t4xsn_nTIKAsZcW7i9d9XtEh-3fNQm0RD334NtQwj1s8adAr5SjO6RbqAzejQi7_JdiigT9wJEg-O97dr8YzWRFWtPcaZD1c4Lyrpg3LSI27B7YSkdoC-kzJYo9wjiWYtx70M8Ku722EpzDVW9DfGKkaYU9E3sGpzFjVEvPrU6lOZsbfIJlQp8WeZmm98ARNWpOjFDW4Ge4Wo5pSKhTqbnGsfYowRaWpf28NS74cza0FrOM4xKbTiRSqbKqTjq8hgn4i9yS0xEKqtDAGSlJzdzeqgtL-IVIw31z87yUojLfMGNgOHpeGRruA3NePfTNMaI7cyPXNPBy3H5pxvLKiUdocDIkUtf8AFRhmdhL9ePhrhuNorTDd7S05oY=w263-h404-no)

##Syntax

The `while` statement continually executes a block of statements while a particular condition is `true`. Its syntax can be expressed as:

```java
while (expression) {
     statement(s)
}
```

The `while` statement evaluates *expression*, which must return a `boolean` value. If the expression evaluates to `true`, the `while` statement executes the *statement*(s) in the `while`block. The `while` statement continues testing the expression and executing its block until the expression evaluates to `false`.

##Example

 Using the `while` statement to print the values from 1 through 10 can be accomplished as in the following `WhileDemo`program:

```java
class WhileDemo {
    public static void main(String[] args){
        int count = 1;
        while (count < 11) {
            System.out.println("Count is: " + count);
            count++;
        }
    }
}
```

##Define An Infinite Loop Using While Loop

You can implement an infinite loop using the `while` statement as follows:

```java
while (true){
    // your code goes here
}
```