##Hierarchy of Exception classes

The Throwable  class is the root of exception classes. All Java exception classes inherit directly or indirectly from Throwable . You can create your own exception classes by extending Exception  or a subclass of Exception. 

![img](https://lh3.googleusercontent.com/7T3hp27aQm8e9v10Jf0Mu4JSvGdsB8uNYo9EnD_2rZsQFbAldhbm0NNMHxwjNSc1qbYKdhaZyKWhZ_HyuCyj3tnSzXuk2oCas_Sqllv58qSKH5AdoW6Ilspi1gBU9SXPy6-njfVukYtavg7Kl8mq4dS1LeMdZ9EuTPkjUcBz59vIo4hqNLy89FNJOmmwNAFol2EKfm9NYvsIrZJgoEn3dJF1lXNg9mVDSuY4oeOZcgG92_JIc7m58MYC-Z9LihOvxy9aDGcrM4UhmhTvW1NSe4UGzD9oKQOheMQb2fQhlOPtKuqxoCVS9Es_7T_gS933paQ2O2_8BvqIvelS1KQyDLqXHk2JEStgPIW0LUT2QnkWgDtfavQNg0LzcDmDH0oViPYODommV1Sg_oMZ5NbgLehtHLM3E9FAXRMOhf675OXJ1M3_9wMqmnR84bx53t7XjX0xcr94cJIwyfKWYqQ0pi4-edFUfrSrDhpGnHfhiktlrLE7pPcjlBckYB5_BJ8_4Fyyu2x4BlebrRvHc650D4j6FvZWrDSS5MQ7WDM5yrYPcT2dia3Htw-aqJvJmAnrHFIOcl8ZGgQx1AxHgkhAlBY_TRYulQ-tqOizTnHgxfibpM7n-qfJ5IiLVNHNHsU=w613-h546-no)



##Exception Type

There are three types of exception in java:

- checked exception
- runtime exception
- error

### Checked Exception

These are exceptional conditions that a well-written application should anticipate and recover from. For example, suppose an application prompts a user for an input file name, then opens the file by passing the name to the constructor for `java.io.FileReader`. Normally, the user provides the name of an existing, readable file, so the construction of the `FileReader` object succeeds, and the execution of the application proceeds normally. But sometimes the user supplies the name of a nonexistent file, and the constructor throws `java.io.FileNotFoundException`. A well-written program will catch this exception and notify the user of the mistake, possibly prompting for a corrected file name.

### Runtime Exception

The third kind of exception is the *runtime exception*. These are exceptional conditions that are internal to the application, and that the application usually cannot anticipate or recover from. These usually indicate programming bugs, such as logic errors or improper use of an API. For example, consider the application described previously that passes a file name to the constructor for `FileReader`. If a logic error causes a `null` to be passed to the constructor, the constructor will throw `NullPointerException`. The application can catch this exception, but it probably makes more sense to eliminate the bug that caused the exception to occur.

Errors and runtime exceptions are collectively known as *unchecked exceptions*.

###Error

The second kind of exception is the *error*. These are exceptional conditions that are external to the application, and that the application usually cannot anticipate or recover from. For example, suppose that an application successfully opens a file for input, but is unable to read the file because of a hardware or system malfunction. The unsuccessful read will throw `java.io.IOError`. An application might choose to catch this exception, in order to notify the user of the problem — but it also might make sense for the program to print a stack trace and exit.









