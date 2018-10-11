## Multidimensional Array In Java

> Data in a table or a matrix can be represented using a two-dimensional array.

The preceding chapter introduced how to use one-dimensional arrays to store linear collections of elements. You can use a two-dimensional array to store a matrix or a table. For example, the following table that lists the distances between cities can be stored using a twodimensional array named distances .

![img](https://lh3.googleusercontent.com/QgF9J6uVcNaMk_b4bZnHbYhktY9Y2PwFgDp2L_p3SlZrA1CN0YTOOpUiISwL_cRo-uicztm35DmipNuC3T9h4YNNHN1ANecGQtAcnz875mOAsiVSAu31q1oZdCFJum_9PYBMrLUnDsxNWiuc42pfEtQoIy9yF5IiJwgL6e80L0EgpOrlwBTrdnOR9Qe6mDpqaNKP46tll5uMnc-WVRYXGECyvU2ySkDwJoOfZR2PFpeWBbGpVuRrqLDWu72r5x0iRxXrDQF6uqadifftejkOjkFQOjC_5zWJUI5b6NTucskcq7aeGPYepS0zjRntWu8Ng9c9Do62_V1Dca8ytDn8bii0Bp-6VZh2s3UlAjFSlQB7ymReK_Gy036m90Fs8vu6Xv0MnOPVtszW_w6gWVKMKwygxfr6Ioo5cgWR-If8b9f9kGCVeLirBLJ198vcFdLL4R8rYSMfUZnJS_kQ4LJLSGbg5N4KIVr7iTyhPt2igcRDLFIWPXUm--KhYxMNApbNEOIal0LDj8jJI6A-rmWSZsr7hGzHN-fyvwirZ4kWK3TVFhdLogrf0wfJC0z4qABtb05SBAlqn38VauaVLrBC3Rot5j6p5C-wkfyK_lnxskSNcrnVr1PCm-42WYrLeFI=w1318-h810-no)

## Two-Dimensional Array Basics

How do you declare a variable for two-dimensional arrays? How do you create a twodimensional

array? How do you access elements in a two-dimensional array? This section addresses these issues.

###Declaring Variables of Two-Dimensional Arrays and Creating Two-Dimensional Arrays

The syntax for declaring a two-dimensional array is:

`elementType[][] arrayRefVar;`

 or

`elementType arrayRefVar[][];` // Allowed, but not preferred

 As an example, here is how you would declare a two-dimensional array variable matrix

 of int  values:

`int[][] matrix;`

 or

`int matrix[][];`

![img](https://lh3.googleusercontent.com/mC64pYe2khWHdgVlHOIPO2AhfxTn0W0FcubcK0ggdgoeHjpnOnTkmgBiPbmXPlaGNrXpJ4NoK5HXeTuuz-nrVjfY4g2oop8Io8yhGudmW6oVut858WtfIQLNQ74fqQgMU98aWbmeE7sk_0oiivd9zOvR5TpVaxnfZpcR69UPevKVBX--o3DlbDqxiGGQVTbjHiHNrHCGhTaIyAs7BELHVWVB8qRQzaeLe57LME_UvtE1wHI4JE1sXCILnHuIa-mjOdejfwTWiG6mdU-2kuD41Go0eINAHAeUysN1mtNnSWjuL4TET0BGrYb_moUzN4X4V9S4v4PwoUnZPLhLbtUH36utHhkNdozI-YzDry2zaMo6YBFEViq6F52KuY2E-ToyZoWiH6CX13nwebUBQ4pKI5Gh645H8Z7QiRh9FeiGeI5UjP3wBiIqu_0Ybq3qHD7T4DGxgmJoSujlEDjJR84B6Q9oOXfGHiTQmHE367gc80dHDvvQ8TpBkdd7-X3-ToOksw2LTcn0R7VXHCF8atraz5GPCsv4fvHgJVdhlxA-d9wfGNxI4xr143WX47O9f2lzyE0vRr0dEVK_dTx_TIQ9k1grW2sqUrsuZGF0Z2XSq1AlV-IKcgLEKWqg5S9CHMg=w1306-h494-no)

You can also use an array initializer to declare, create, and initialize a two-dimensional

array. 

![img](https://lh3.googleusercontent.com/dmbbZfycQuty9C67VuoAQkiPaLC5ewrasK0BwmJWG81bCtU-6Rb6gcFpMeOy41HJF7TIYWkeKrVS1rI0iEy-n0A68DxLc-950P-XEMrIkykun_Nu_WY2J4XQ7b2d5iuscYhuX1UR_pq9eLJZ3EFLn2ONhDi26ZtSnWdNTTl_2aWSDapvqKzWyDml2dQcET2TH30Be6NvPacZ1N5OL3euDMgUueBS-cpGemKZk5FGxcpY4ggtoHFz9VeyIZu7k0AQcQoyMHHhdwA6lAb0nb61YwzRYiKnEMunWV2lnwZdKbku12J9Ruq0GLmfQOtY3G058Pef4R46x4Pq9mhJUk85Kx9T1B8y1UDcxX-hP10snW6ybLOmgoAn0XxJ_dMItMDAhr1RuvMsQhCJBC9PbUNPakPJ1nFH2RAJgQOB76x3fVSV5trz6TJjIjggg4EPfnr1jbcLSTvY1p8CdFWb7WKjIzHuPjo2L2KZ9_jnRaBF4k-QjXTFnWypcsmnWt8qZMspMe_IwI1E5jB6QpT3PVti72GgNZvyMPDjgDhzNBy3ZTyNf_BdOG2UNc9_VaCMsk96brioM-mhagN9jcLr4Ja7gNH4SH75DQCE4jlbsx7xe3CDcMj8x4cPfk8neY8XOvQ=w1492-h304-no)

