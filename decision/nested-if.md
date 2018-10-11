#nested-if

![img](https://lh3.googleusercontent.com/YNkA-fMG5bLWXoCnLWzHTv7Q6Ux9n57L0BApWj81HeTnjNGKb7G-vVyNPCrHHKOMnVFSkclMFFNOBQ6Ih2fgdCto6iApxJD-4JHGEb0UYQQ7AHuVJs-FtYtVuuUoTzSvz4cpF6wlQuAq8UeAfcyi6Vcv8W6c_ymBf1pB5sdOoNjNdG91me9sPWF-5K5AVmKA3r64J9BcUy6VFngPaCTtO7SW9CcVNb7x-GwHhjq2FJc7vQAn8b0OQnxMcRYXW3THwK0tVg7sWygSBijxKv5Br26NazXZWcz3HwWhBIduWNt1qx79Jyy_AFoQcpR0BcQFjTxNtdIfiRDCQZUBBF4vhMuOxoVk_Y3xf6TCsVIk0xLn6Ysi-A5oGOnGetzYI_gi9QNIfonLanJnj_VmByb4aSJ3NbghC8dSBlZunnwLift4PZ-WrAxz5ZZfmpTB_1jc962LWBB3N8tG3OQ_SQGlEXyi799Tt8xkIDyl8ywzWFPVB7aDYXEpcNI8m2I9T9NKTmbnqGEvt4A0jAplrhRZ5l-uNFBnnQHFdtfLDUsXEs38TLPyVrhV2Aes-R8Ql4AKfF1G004KT-CU7nMlbUMDhf0nfP5vCK6EPXIp1auMhAPu0FA78vQSPQtvG8nlSCw=w577-h503-no)

A nested if is an if statement that is the target of another if or else. Nested if statements means an if statement inside an if statement. Yes, java allows us to nest if statements within if statements. i.e, we can place an if statement inside another if statement.

Syntax:

```java
if (condition1) {
   // Executes when condition1 is true
   if (condition2) {
      // Executes when condition2 is true
   }
}
```

Code below will print `a<b is true`.

```java
 public static void showNestedIf() {
    int a = 10;
    int b = 20;
    if (a == 10) {
      if (a < b) {
        System.out.println("a<b is true");
      } else {
        System.out.println("a<b is false");
      }
    }
  }
```

### 