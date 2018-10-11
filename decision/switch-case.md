#switch-case

![img](https://lh3.googleusercontent.com/_BiRG_YxzLtfQ-MLlv6dLY-qYdaC3F7Z0YuGXWt8uLHUrbaO9XFtSvpB8s4rbJgAGlH3mEjOZXMzjBv-9ef3AXaxiEX5q9cet2pXMbphKMb59UlWB9EOtmlX2U2Jmz7Lh5XarpV1DXSgx5Uhoe367eyHN7afbusP3fTQfQMG-NUNqTAukCq17nb_kHdvzbCLJX8Ey4-ZWWTHbSGgTM3yPOMu8rUkcWpiTvNm4383QuDQRBFFgnlkF3IsEIOBh-pP0Sls98m1i5gJg0RVHWUj0jYAnOV8cSYJMORft_6TEXEuq8VbUU7VGK6uULg6cSLcTZml5mDNe_cmKX100BEQww-nbLizSIGoe6r0m7cnvRoBSHRYoR3TkwvZgS2jgmJv93eWFVbKgjwvWWCNjqNrcPNQf4upUnpVlR6ieiHzsfrgrgC-nFgAfOGQIlsQuKQBtn9xXVyHQRvRRXp4GbhiUx70AFLaCyBMzFptrwv_iyN0mTmVPpIFs4w5RmH9Cw8Hq5-wifFOWB8CHWhGXpDHZlM4E_ZOwNZJNpAnafbK-L5HvHiJcO_4xuCOQ4Y0aF8yb0HTBU-1fsVJAfNBZP2YmnTn3wnrVGXwQ10kQ112YzRy3nZuRK0gFh9AbTAmMjw=w702-h971-no)

The switch statement is a multiway branch statement. It provides an easy way to dispatch execution to different parts of code based on the value of the expression.

Syntax:

```java
switch (expression){
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
  .
  .
  case valueN:
    statementN;
    break;
  default:
    statementDefault;
}
```

- Expression can be of type byte, short, int char or an enumeration. Beginning with JDK7, *expression* can also be of type String.
- Dulplicate case values are not allowed.
- The default statement is optional.
- The break statement is used inside the switch to terminate a statement sequence.
- The break statement is optional. If omitted, execution will continue on into the next case.

Code below will print `Switch demo a==20`.

```java
public static void showSwitch() {
  int a = 20;
  switch (a) {
    case 1:
      System.out.println("a==1");
      break;
    case 2:
      System.out.println("a==2");
      break;
    case 3:
      System.out.println("a==3");
      break;
    default:
      System.out.println("Switch demo a==20");
  }
}
```

