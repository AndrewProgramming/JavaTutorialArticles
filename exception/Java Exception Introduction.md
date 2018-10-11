##Introduction

Exception handling enables a program to deal with exceptional situations and continue its normal execution.

### What Is an Exception?

The term *exception* is shorthand for the phrase "exceptional event."

> **Definition:** An *exception* is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.

When an error occurs within a method, the method creates an object and hands it off to the runtime system. The object, called an **exception object**, contains information about the error, including its type and the state of the program when the error occurred. Creating an exception object and handing it to the runtime system is called **throwing an exception**.

After a method throws an exception, the runtime system attempts to find something to handle it. The set of possible "somethings" to handle the exception is the ordered list of methods that had been called to get to the method where the error occurred. The list of methods is known as the *call stack* (see the next figure).

![img](https://lh3.googleusercontent.com/E5sqZAbw-R9OH9rJdN_TrN6OaHyRksivUGo8R3U9V4AulbNDBr5OTKfbYotF_Yu5RRTZ5gluMphM37mOK22IB2T7XKjy--F7jDYteK5KjNl0qAZZCNv5Pu-v1DoJZdQa2LRXJ6DOLo7JZMPvzMdmACWL4BMfpD07U7wKN9QpMLWfRIJ5C1H5lB5BRvBKpuqsSoEvIG6WrT6SAKvY1ftcyGNrBozwiuejeLVJjWn8nGtnWOszjZsT17ZWANHo6XeGHOOg7denjlNRQS4Sc5xZmF_Ydogate2RENUFmOwfZPglNcKBMAKtVy-so19gO46NnR4YGi03CK40w21zbvFvcxWrm2W3Mpk8rg5gOb5Mpl0JTJrb3f-q7iEofAGtPqS-7wlYJhc79QYIk1McZydqNYJYvDfKOpuTlEYMDe8bmXymC0EDZlpCDz9hBS4xytYCF-iiO6lVH8hqBGOzgRxDyvHUoaIdBC2VqATVumsW61dvnDSJ1u2Rsb2suQCF_w34IVrKZ75vy_CpHHnyH8Y-mLoX0u6YfgoOpIP5Hq5gc-L4BRkH6K_S2oub8h-sXPlWx4NiXcFq7LNw8cfquZ1weHPI-93HGmGAs6T2sG9TeMfWW1ioYnvwP3DclDxt47s=w288-h193-no)

​                   							The call stack.

The runtime system searches the call stack for a method that contains a block of code that can handle the exception. This block of code is called an *exception handler*. The search begins with the method in which the error occurred and proceeds through the call stack in the reverse order in which the methods were called. When an appropriate handler is found, the runtime system passes the exception to the handler. An exception handler is considered appropriate if the type of the exception object thrown matches the type that can be handled by the handler.

The exception handler chosen is said to *catch the exception*. If the runtime system exhaustively searches all the methods on the call stack without finding an appropriate exception handler, as shown in the next figure, the runtime system (and, consequently, the program) terminates.

![img](https://lh3.googleusercontent.com/7TB6nfKSK8t0NZdhOuzqfud6ryHeziD0y1wNpQEqEkIHxKBrJ35prdI0VB6Fa-MRCbU6K-b5nNDiUpgzPSia0vL_QB421TR87An6fkDjcZF7Fnxw8Gq1QPpztt7dgRqWKAfNu8v1Vf83RFL9KgkjejOaaLESHG06DANNs76eoUCCe4vNnGMDVlaIcT0iaoarGSra64KTxgGOG-QJ_VUt2M1r8KzZexrWhZOBPnPK5qTWY3TecYmj_lVZ60pyxFooCek3IiEEi9ZCqKhxQNWkGajHFV63bfXQjMjm-IF8S4QdL6Zz8lWiIw3qxDzl8ww2uBZQ-MOj6KbB_ox5kIV95dgDQC0-jry1m1sbYaRP2TD_tBVB-AMMdrg_tGEefS79Ubk5BZvbKDPmaQdiot_sZpkyFLbhi1imddw1qultEu4C0_UfsuXM8FF8kNzYTuo1mDKxbi2oW5fRX-W6asNVL16EqRqkAnVE3o-2fMPDpXLhQZEjKFChTIGknPRF-Xbs2tfNA_VtgGVudpSUKFNB0kPFpO14VCGE-52WNAq04Z6R7VrjX3vG2SqdpaX1XBWtLRMdesyObvuGcjBvZB7nyPNAxNV2HEX7f_DrlidJLRDmAnVJ-erVASuOG_lclTo=w411-h193-no)

​							Searching the call stack for the exception handler.

Using exceptions to manage errors has some advantages over traditional error-management techniques. 