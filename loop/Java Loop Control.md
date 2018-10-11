#Java Loop Control

Loops are used to execute a set of statements repeatedly until a particular condition is satisfied.

## Why need loop

Suppose you have to display "Hello World!" 100 times. Of course, the straightforward solution is that you type `System.out.println("Hello World!")` 100 times but obviously this is not the elegant solution and kind of tedious and error-prone.Java provides a powerful construct called loop to help solve this kind of issue. Using a loop statement, you simply tell the computer to display a string a hundred times without having to code the print statement a hundred times, as follows:

```java
1 int count=100;
2 for(int i=0;i<100;i++){
3     System.out.println("Hello World!")
4 }
```

line 1 define a variable called `count` and initiate it to 100.

line 2  define a variable called `i` and initiate it to 0 and  continues to display "Hello World" on the console until `i` is equal or greater than 100 the loop ended.

See, with just a couple lines of code you solve this problem.

##Three types of loop

![img](https://lh3.googleusercontent.com/r5N4Y24SasbFCsCrxl7eJs2lPiZ43j0Jl7Ujej42VjVyBf6LLWI6fi8QGt1DSlZNZPU75ifUfrLdjCMeIJR8KcvDUkSA-IxiQ1sapeGSlSufXRJ2lQbh895nTE0no33Fp7IoPPDTCE8OnVPgfMzqdCvuw8dfnIZBu1c8a8Kv0AJm6XASLVmqD8hQC6TP7rcJ2zPt-_wD3sXToMa2on17Qy_5yFZ7KLjXv3dMF7Y21sZTMCTR3Zrpil_TWPBToDHjB-KiqFvhfOwx6AS_tzpTdyUzrr0cYG2q4x8vWVXz6qjFt_tQkm9qr21rjthRbuYMbznPGjDHkA5TUrTMaHOt3F-Itgs98so6vCc8Ea2gA1JmwTUy2A_9wUWPiJQIfUtEdj_Tah6bAf-TfG4kxaEOwkloxngzpKws3C8F8p3B73QVu0lMxBIlGxJ04u1p1Kju8NTvW9DdMfcRUSmt1EAEvXUtaRlARzNYRwtB20F1x5svyvxhqelKYUMfmnLXKRytr-75F9hZnuwox8VwUYI7DeVb4CHlNg8uoYWffKW9ulkCUmfmPEMAPnWnV1ZLELbXMaBGVcGqCn2IVawB2w8dfeRpxsSv0VPcOuj93GEFiBeH1b2mQGLv7jtf8LZZuVQ=w664-h523-no)

Java provides three types of loop statements:

- for loop
- while loop
- do...while loop
