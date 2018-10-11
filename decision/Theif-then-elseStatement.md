#The `if-then-else` Statement

![img](https://lh3.googleusercontent.com/Br-_Wr-oaCCaOc2QbENlfB-1XfO9bUFz9V3E04wsNxAhM-c6vAsuQmPs6sRDGa94pjOtl3_hYMdsqXvOqDdTGCWZf_0tEM1qXi7u7BROTLNo0-m5ItO2O9RU-rLRi4uTeJOCBe8sO8WsfE-KY7lItCn1JAxmNJY2Tpd3QMWGvmh-mezchK4poy4C1Ch0OvWckAJ2-gqeigi31OWbBHeXgsIt_qTTioFA8DhyXyO-F2vZp6ddd0SdIML4bGgh3RE-T4Iq1fWFVnTvGQkvdJIcyc2c5NbY20GjZ-mzev-f-MnyG0R7m-9fL8ReY5vJcgXe9WgGeVkvX1beAXaBMXLQ2Zt68ipg4jmLccnKe9kRk2vd95cFm9iAcsXbaSUIA6bTt7Z74XXlBG7OsG6P0z2APiYTBMfgeAiXvZ5xevEJj4L3LT6L2iv0X9UR_Ino0HnzEFM6vqYMlnFU9KlX6cViT1U9Mxg1tYi4DXpgxO1NP1EQl3aiuO95-cxJbbp_dgY3F1a_Ro8sDoKhAgAkiJRNe7kDUvQvK92JZm9KT3AnuRfya77H3Jts_VS-OI8uk3Lrn_460w3RBJ5PqLmuWkNvtzaQuEw5RwwWZ5YhqJTd3oBblvGw2u6cz_c02u0e_GE=w251-h321-no)

The if statement alone tells us that if a condition is true it will execute a block of statements and if the condition is false it won’t. But what if we want to do something else if the condition is false. Here comes the else statement. We can use the else statement with if statement to execute a block of code when the condition is false.

```java
if (condition){
    // Executes this block if
    // condition is true
}else{
    // Executes this block if
    // condition is false
}
```

The output below will be `a<b is false` since `a<b` is false.

```java
public static void showIfElse() {
  int a = 100;
  int b = 20;
  if (a < b) {
    System.out.println("a<b is true");
  } else {
    System.out.println("a<b is false");
  }
}
```