# Package In Java

A package is a namespace that organizes a set of related classes and interfaces. Conceptually you can think of packages as being similar to different folders on your computer. 

Package helps developer better organize the code.

## Type of package

- User-Defined package
- Build-In package

## Define a package

Syntax

```java
package [package name]
```

Using the keyword package you can define a package.Let take a look at fixture below, here we define a package named `com.zentut;` and the class `Hello` is under this package.

![img](https://lh3.googleusercontent.com/bFZh2iDuTjM-L7uqt1ojvOreAis9cAsPIMVOALcLnau3vjhiA5p22VJl5FhJCK-9rw1EH0CMrQRW2UK3l0KP5vXYDGPL3dP0uw2PpJOchJg-jGyYffGR3dUQHDYAM4GhUzHiEJQpMxrjASOWE4KMKyWzd91Vxd7wisdzu9qfugqHeaixu6QfcaknkGnkxeNRy6_6UI5Mcz9a9bPJXiU2v_GdFnbP3oOrjiGmA0KUybFzbhFErw9PgmW7qxdC6h2Go34qh6LFOz2ojHc1L4SOCVwfnlwMN0gIxIyC0-nd5un_U7W3Bv_XiI7qvKfmMceeah7HVL5vToMDHWEnefnnLqjv2xWulDCsZBiQEuXmbVYllogYao2PaTHPP2X6kWL-aHEE_G-KtxePEEPzwRRmZnNfTn0KZl-ipQI6QP9WSplgPyjEjYogLg61pD6TqOVb6jpHCfC7dmDoMEQlILmwBAXIqRu-ZPyz5iY6d1qfIKjCFRHz4IqKnDICwKBTCfEm9keWJ-DJWJE5OsQNmRUkICJjPqp_fgyC3JmB5PJXneGAijRR150CA9FPNuNbMBPsOU4gMg5m1rNTcbJajnfpvFtyUxhetlRdteQluFpTsodKicMTvL-BHXw72zlvNyg=w642-h321-no)



Package can helps better organize the code as fixture below classes related to Array are under package `arraydemo` and classed about varialbe are under `variabledemo` package.

![img](https://lh3.googleusercontent.com/fHVegqPMI332Ecc9jsgb1stdWGLeytPVo8AK5LBRWfScNJA2Mtgvcf27WHNYcVJcd1f2DBPIrDjlxpa9rOA0tk4F1DQycoJlDphjkTzpyOrv-Vb1FQV_zvsX2HCnrVeqe-dlm7Q9l6-7C8UvHJ2NrYs4SFV6b5633Auh5GrxFWxJFUj8bGk97DIxGjSa7YWma9KMnWvDl07l0nf4-Z62LKzhmEPRPZeFPC28Rg7XqjokPVwYweSW7M9EsWLMwDN8AV2rmwpENLjs8Gv2Udzn7NouVE6aHlLmO450ZWJvvr_pP6TYkp0yYuGqDAXT-m6uhf9o0kt4FZfTEl_Y0G1f8opQK4TT8_IU99B-dXdNya9aG2KSQSGnzF6qzW5puyvpNAY_KtBi1TUoS3w_moAnuzfSip4rCC0MR1_3LvWt7Wg7b2e0-0UfsOLOXl0Iob5WNIWJmFKJxI_K2VswDsZVFD1a-va2DhTynvuW8kX9Gbn8qMdd4nhGFoYFp7KDGN5Fuc_x0vEewntrCKN4c_bBVSK0vy7Ih-slGfRIebVzySMoIMMbQ6yzcIR5acWM5YD8opvgoFftQe_tFLhOt_T1fY5QY1nvz6C8QoCArhM48OVWMP7a5-J60FP1Wf-aaJk=w800-h1000-no)

Actually package is translate to folder on OS as show below:

![img](https://lh3.googleusercontent.com/k85tT64DLerEGPADCbghuT9tn4zq6yTmAwvxfGFaQiXATraux6YKBIf9Laoef506604AVkAKgDdTKlOsivAR9zfvVDgRZjik7_nUTTFO_WrqmvNKZKO0-TfqSXPMzwhk9HwoUCNCVX2Sz3h13yVJAOOnjTzNTWVjbVCGKRm_arrem0aYoYzxvxAl-44JJsAqESxrftvcrOhOv-Rns-hQsUSX4HmMuTJry7VuCTv_ouLhs7IcM9r_XBP04_h9QogHIC4eFim5Gs7aiFq1xj11W99rK1a3sGOyQadPfuGYgRdkK7yvtRPoYjc8DjS6FKohIDg0s7q4nuCsYvYUG7PduEbqvijWlw-eP3iavcfUUHA9tX1C3BlQE8W0oS6khGhJHu02SzdR-En7EwwlUOIuk-gyubVsC5jYtu_vfCBHZ1TE_wSZQ7FpbC2PrXYSMyc2IkCV3X6VEG_bzSmEkCBwY8lj0G8ZTdRuSA1q8NNZtgd2JgnXBLcVbnnt3LEEKDZhUyxspCXSAkTQ_N-hUGyltQK3vQk3KTA60w1yVULJXicvTaeQHsdXfJuVLw5WdxYrqvntnXAs6x7sQVHDWDTMovP-xiZ0kJutxKS04bOeReacySjsgMXiaWSXBa-5RBk=w1574-h888-no)

## Build-In package

![img](https://lh3.googleusercontent.com/QIqnWfgn4eMwiIPQlhX7dVFgrfxdSRpGDop1PI8BVVQ98BnQG0y9qHQ0fhxmDo-FZGO1sP1hYlt94rgelXSvhfsbpfG_peY4Y9f8W2iEfxMzDrR4HXfMl15c-xP5CMau2027ARgcideA22_rzChWs8DIKlxgFdM3yQMwyIpSPaDWaBS7oyRQ0EpT8nnHeIo8dfFoseqpoxm1wVPBEXvM0hgkk8YEewQAxu4QdeCsTKTfeOw6zxFEEuHFgE3j_6eByoIld-QESjnz6vZjfScC1AYjnFRibxrKxUyt51GJ2W1Ms14ugsq2BbmbbvDgClGFhPo_SExfdk_xFwMotzOZfOflMxtRI4iRdO7XX5WlRefK5L-0BbBLNRJTxinIu9UyXyI4ftsW_F1lRk8YVASBHrg_RQrw-IAsccyQ4tz5EjU6abSUHJwiw2Io4D6QRW_Jw_QAmE-Xs4pZ0POqcafMBUmBXp8MI_MvDrYjvhn8t7aVQrqAWVPzsjjgWlF1iAMc3z_zs46LY05vi6Ubuvx41O7fW9kz-qV2zmqzFZuLqHzQgEFwm47qoNmcX_GmW7fHcxH59ajWojFR5vLkZow9iCEI0dW62weSw8Z_UfPpCIvu2ooTt4aJkzuqNuWYSrc=w502-h623-no)



