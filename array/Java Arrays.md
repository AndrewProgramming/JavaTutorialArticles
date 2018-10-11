##Introduction To Array

An array is used to store a collection of data, but often we find it more useful to think of an

array as a collection of variables of the same type. Instead of declaring individual variables,

such as number0 , number1 , . . . , and number99 , you declare one array variable such as

numbers  and use numbers[0] , numbers[1] , . . . , and numbers[99]  to represent individual

variables. This section introduces how to declare array variables, create arrays, and

process arrays using indexes.

![img](https://lh3.googleusercontent.com/Z0wJWQNWKmaJlOrupTydEl-djuBioipCmInCb2hbUUxGpiUEWUsxpC5YyGZ57YuFdo3u9o1sk9AxXwtwW6LfzeAGiKP4TwNWQzUqwGiSndw4hi1Z1Cu4P_hWVmUoo4HhPCAByrpWOkPB1nDma-5JZLumHa7TJAzhGr1sPwEAmJqYIpgz4FPM7zH0F1J2lv0T3dlvQrkRUET5wiJK3rce_REZ_mQTKu-7RCJ-M6pkqxfFFdclYSmPSspP8gxf7YqBvSHIPpkiYWdJg96FDNlx8fa8ZwI0siW8NTM6xE3G5BiHkz7DEXPYgyurnAp--_5n4-GL-30RBOzt5qQYTy2-VmlAxAK4Zx5wui4UEcqw9SyvU6Zrhd2QRAaotx1B47DVG_UjneOm6d9YFvS5dTwHyDJ4wvt_FuE39WmU9Ylw_hOVSBqSJ-PWuR5MZJE_Pnm7DdMwt5YnHa7j2aj1RCyl5A4hEvFd_Sf2U1mR19rirFiptDLk37GQmpQ1GZFygW-4P87sSZTLREkdFv7ATuHY_F3gvQK9d0b7WYgKrOldTa8vwmO3DSswkIwGCWRv3OQ1FIfM68M4iMl7blktQMHl4uK2NA3jm4DJIoRZSGObO8LW3MNpsn3Rmu6jsVGoqw8=w335-h124-no)

##Declaring Array Variables

To use an array in a program, you must declare a variable to reference the array and specify

the array’s element type. Here is the syntax for declaring an array variable:

`elementType[] arrayRefVar;`

The elementType can be any data type, and all elements in the array will have the same

data type. For example, the following code declares a variable myList that references an

array of double elements.

`double[] myList;`

## Creating Arrays

Unlike declarations for primitive data type variables, the declaration of an array variable does not allocate any space in memory for the array. It creates only a storage location for the reference to an array. If a variable does not contain a reference to an array, the value of the variable is null . You cannot assign elements to an array unless it has already been created.

You can create an array by using the `new`  operator and assign its

reference to the variable with the following syntax:

`arrayRefVar = new elementType[arraySize];`

Declaring an array variable, creating an array, and assigning the reference of the array to

the variable can be combined in one statement as:

`elementType[] arrayRefVar = new elementType[arraySize];`

or

`elementType arrayRefVar[] = new elementType[arraySize];`

`double[] myList = new double[10];`

This statement declares an array variable, `myList`, creates an array of ten elements of

double type, and assigns its reference to `myList`. To assign values to the elements, use

the syntax:

`arrayRefVar[index] = value;`

For example, the following code initializes the array.

```java
myList[0] = 5.6;
myList[1] = 4.5;
myList[2] = 3.3;
myList[3] = 13.2;
myList[4] = 4.0;
myList[5] = 34.33;
myList[6] = 34.0;
myList[7] = 45.45;
myList[8] = 99.993;
myList[9] = 11123;
```

 The array myList  has ten elements of double  type and int  indices from 0  to 9 .

![img](https://lh3.googleusercontent.com/czocrc0GfpTPKLYs70Rs0CnqGesuJA5-B3FBbfgM5dl2cU7VRfTKUtbrnDrUeR91r4cBUT92hFR_ma4kOO3TPyFkPkpfl2VGsgRC4kvvw6qKmcc7rYI5ADbItKpUlv6mRr8zpHYkaJSkq3W50lyN4hJpWUv5uNw4Om2gzGewFdwWPAk12D1E8v3UZrIdQUuib9ndIBdPsNsoPLldzw_h5S6R1pHfMtDGKOjtgml2-kLJcaMwElsgs8QKlYYNUJ7va-YuBvnoO7OxOjTTaovhj9-wcxwHswWi_1qHRf0iUqWHIjqByWNoV8KREly3LiGSZBJRfpALEm90iEf9H2Q0rbOF6LKLAMBTGmzneHHOPotcm0sn0D51aP51ia8FaP8gDiHEkUNTnL4o1hm3F4Fs0sDRBjvMbOj_rDRKuWXCZk5L4hc9K8-q-445QFirvdYHhhdtwMn7zdmUlS0LZAomxxdttVnpzdFswuSxbaDBU0G2wG5bw8RHCGdUCpJe3AHDvqlIt2rwR1Wm7zQQ_3Toc8-lwUUYcyae1ZzK2rUu_feNf6gGl2EIHX7uiBTZUX2JLqAXsuRHapJ8cx7a94E_QnMmD59GqO0F5GuVFR2roeyD5VS6awXAXQzZotYcNmU=w1208-h562-no)

## Array Size and Default Values

When space for an array is allocated, the array size must be given, specifying the number of elements that can be stored in it. The size of an array cannot be changed after the array is created.

Size can be obtained using arrayRefVar.length . For example, myList.length  is 10 . When an array is created, its elements are assigned the default value of 0  for the numeric primitive data types, Äu0000  for char  types, and false  for boolean  types.

## Accessing Array Elements

·arrayRefVar[index];·

For example, myList[9] represents the last element in the array myList.

## Array Initializers

`elementType[] arrayRefVar = {value0, value1, ..., valuek};`

For example, the statement

`double[] myList = {1.9, 2.9, 3.4, 3.5};`

declares, creates, and initializes the array myList with four elements, which is equivalent to

the following statements:

```java
double[] myList = new double[4];
myList[0] = 1.9;
myList[1] = 2.9;
myList[2] = 3.4;
myList[3] = 3.5;
```

## Copy An Array

> To copy the contents of one array into another, you have to copy the array’s individual elements into the other array.

Often, in a program, you need to duplicate an array or a part of an array. In such cases you could attempt to use the assignment statement (=), as follows:

` list2 = list1;`

But unfortunately this will not copy an array but just give the reference of array as fixture below shows:

now reference `list1` and `list2` all point to the same array content.

![img](https://lh3.googleusercontent.com/ZVcbDjdSVcsLyixzJjWXsAdPoN1U2HsvNl37KkTfmJxkYzdtigLB5we06z6RM3PQVZ-azLXKpXHX7XVIsj_FfsvlhhIVb_S6_pwkeuBLICT6n-WvNXBzieGnIaXuexqauoYe1xjYy80YGnvUq3nom0YJtk64wCUD_pLaRvraJsljwndCnojO4wRD_flyb2uyPqdwyhsW_lrdtUYRFNek7QHsSumgTWYC8lw1E47ol50je5r6yLZCaaBzkdSeLwJhkeO9AIBpw1dRJBMdKi_7acwvQYGxq1Jrfp31M5xs_CUa1SkWD3PxiYXIo1IQ8GFlY8OdDf89PYFcWfgzR_8C_RMU1oQqRlE9FDmOYfnYcxg3NYL_7CAOVRcgtGo2NecIcM1Uq9em_CkprGdLq6rH21PbEwvS6FwvDFP4-W-YdHeCk498QmItr32T_JYBZQRxYJ3OVdIXuya-DjjjxbbCtMk4yG5KJ7LFHYOVezGEauKPyBLNNYtupH8qFeaCU86HCKAlkkIbQbnwkj5wk1Di0TZsiDbE8BQo6HdBh1X4h7OF6s0DNyswCRJluqlxqXQnnVjzCvzAZM0P3osarus1UI1f1RflETBWyILQ1r-gsnXjstPZXNB4fxMn6vQwkJY=w1054-h412-no)

So how could we copy an array?Java provides three ways to do:

- Using `for` loop to copy each element in old array to the new one
- Using `arraycopy` method 
- Using `clone` method