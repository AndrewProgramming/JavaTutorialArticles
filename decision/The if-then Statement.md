## The `if-then` Statement

The `if-then` statement is the most basic of all the control flow statements. It tells your program to execute a certain section of code *only if* a particular test evaluates to `true`. 

![img](https://lh3.googleusercontent.com/Y0DWloZri0JQ22Nb0eaQnTqoHTm8scwTWFZHWIYJ5X2eMECQUzuq9tIFhuVW2zaAuSMT4WFzRSGIQYFpakRso-IzfOThw_Ml3gTuaPbbhucX6yjXuF9hWXP01o1mO3f9aa1YphCV47sjaEBlt_bHo9D9lJ6J-KmzX2pEvcO4d9wES3_ff5Ib6ziKYtUyazRqIytJk3cIBCMH29RKpsMMGxelB66x5fuWeYeSzcprXxieAmJxZ_IdeqLk6dPY7BGaBQv1pX2Kjti5xJYjvT_zsv6V739PcQV6ANAS17ndRPtpMQVHHvZkt-59P9WD7J-WTqu8I44LfKGf_TYZ1jYG3QXKNLsByfaf6SmTzyyPuMi4f8VEwca_xRrCfUjsTtx4H3XmnPPbB5dRDKpRT4DVeF9meF9tdkUz9dbXOoynM1Ib-_McnhX-31oJoeMqQ4TGazFFHit1sxIehhsLH265WOTrJpGnqDY5-YWTdDYBc2rOpkhXxJD3ayCfCWntRBSnF7_4fDgiQTIfeZ2NHHre6dbrMi4WqhQpf0fMau9kfdtDZZr2cMDqxt0w6pZUL4q1ylAEIz8zebYJfmgYMK38uGtWOUhJOtHvfVv-VEapTVMaf-ZMIkJxPAC4OcADHsI=w265-h339-no)

This logic is really simple. if the condition return `true` then execute the code block.

```java
if(condition){
    //statement to execute if condition is true
}
```

Look at the example below since `a<b` is true then the code inside the curly braces will be executed.

```java
 public static void showIf() {
    int a = 10;
    int b = 20;
    if (a < b) {
      System.out.println("a<b is true");
    }
  }
```

The output is:

`a<b is true`

