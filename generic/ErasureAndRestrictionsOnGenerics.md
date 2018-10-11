# Erasure and Restrictions on Generics

> The information on generics is used by the compiler but is not available at runtime.
>
> This is called type erasure.

Generics are implemented using an approach called type erasure : The compiler uses the generic type information to compile the code, but erases it afterward. Thus, the generic information is not available at runtime. This approach enables the generic code to be backward compatible with the legacy code that uses raw types.

The generics are present at compile time. Once the compiler confirms that a generic type is used safely, it converts the generic type to a raw type. For example, the compiler checks whether the following code in (a) uses generics correctly and then translates it into the equivalent code in (b) for runtime use. The code in (b) uses the raw type.

## Examples

![img](https://lh3.googleusercontent.com/C5Er_b8JYhUUVV2FRNGjd1dV9d5m-U3eSlULM_QHGzuRlfscGoDsHewqVw5b8pGAvbhxauHxHaqOh4QF7by70yFC0MBlwk2O4cvd3jWVt9jUsT3oxKrK8Xe_769AoJuttkJtsuKk6NZwXfcTfstD9iA3SpU2Cf7V9GquwqTtxtZzcSKzlTZsEEaQ9GZx3lHTHouMGdHGPTSZo0zbqAdRiFE3WefZ7jKQXGWc4PrtiTnvjqBgxudyTPjZ-stUbowOqmqI3rBdpZYrkFkR_kdihRU7rz5iGytldg_6XFxHp847vcz8qF8XmgeXazRjiId3U7ojChyJeXN8KhmFK2M7uZxhUSpi0NEl66WbXXCWTh-PFaBAXg5vr4sU9Ha0oxlfNL9Ss-R5pPtfnS84HoCruuicOrb66oqBkZDf4c6jMwd7OedZxk_CmS-1rvYsEF2Ei8BG-WDL7lx32Ve4El0yrK_9MemivWMl21Z7_ELrAQJJmvhATZqYaj-1jBxY73GKqXD71HDg1AT0Zl8A3dLi2gVdEh-ulHt5tWNUR17ozvUPRqPncxWj0HR15_3Bkjf8H5LiP3-C54sU_2ZLX02vSVRFi5w0lLJOkFVb2iBPblFs5fByfIJ9m0W3Fid7ESM=w1482-h218-no)

![img](https://lh3.googleusercontent.com/o5XpkSCrA6bORqqq-hm2HuJrmJWhpXopsW64z9D6EL30m69E1ZOntdL9MO-lhAnwmAUUTFaQuEdD4aJl4-W1tAKZ0UPjNIUhXIDKx53JBRVi3tT8MrzhHE6I-Cq1TRmvydcHcauQ4KpEQQYKKz56Isvm2oio0CSk3HlB4rdLUhbRx6oQ-tO12vYekWdwRz8NezoY57Bdc7cMcT_-Pj_5xkVxmqGwfjSmJ82XqTFXYj0qYnSohaDRoBEfT52JDN7dwqwYifgJN_zi5pHWadsvJcvChkKsFn4b7elU3cUGV6lREyMXHuNlMP_O754HQX4TAUgv_h_iRq4izpCfgpV8tAIVj2Mtka_McPpwINKz38p-9aQdvkDhjW2_T9RKhOVpVuTzQyeeY8HduweEUHOWQgoHmYPqZ2ntRsC4NqLKIKg1Re7HOdkDUXLJHAPhnhmBw6A2OuVH11_bCQB5LGX_1IdcwF98v-u4Or1CX_-g_KcMXSBBBhkYzlvhy13nWtXB41XajJs0Qva_NebM2w4vuSIZq8VzHzgksaGE9kbdD_hXi9YD3DRCx_wnnO0cQK94mAzmFI5AhkhHifKyppzQwy5Hww4_l5mGFrFshsk876R4waEWE19J2KRmLJjpphM=w1420-h274-no)

![img](https://lh3.googleusercontent.com/4T6cQYTOt--pYLBOa3WuFA5Vd_a-IFXaE3DqrD06u6K70uPpcnAhGnfXqlbM2QgBsmUtfhvurcHmD5DrFYoVJWsfZ9SCmHUZuk2Cjp37vHg2TfjRvqAqmW9M5diqFO7UPAH79GOhrVa-O9sxh3jpiGKCj-BqO_nN86Rb1ks15JfE_FunW1eci2w_O47QwvBvXSI5cVZPJo8aGCi7Z_eGGNZSnJIqhbCxn-nEFjwzjl5yzj1wJKNOuLLlxiN0wFlU4_E-YAyfwtLF71UBQDap9IEM285uGwCjfBSJQycWW0tzzg3zBIi6UeJHlRzYCMwIBb84K99J5TQPvi4UhgKAfE3er25K-vHLftYneKwSJRIQ0WFuVPysTjBuIFgRHmawfi4KnhNLUiaF1w8HgjzE2Z6qNSGfzaks3MujNTl_Dix-rTytn2-X2s8_nPNRrJf5K6HDRBS_MbwlIbzg7qL0ug9PbNvN5Zu65wpVDw_Hg9p3d9mf7rKuE9_G2G2kPAucZr3Im0A9nMaz9Qgxu0QzdQRfpg9TKX48g4IWPGvGsCwY8oXdp4AgUGfkQ--Pu5EV7ZTFh6lt9CRXdE6pF0jkDpznAWf6ut3-jqGrv6Ya2WXaxfooWd7I16Ssvn67AxM=w1448-h326-no)



##Restions

- Restriction 1: Cannot Use `new E()`
- Restriction 2: Cannot Use `new E[]`
- Restriction 3: A Generic Type Parameter of a Class Is Not Allowed in a Static Context
- Restriction 4: `Exception` Classes Cannot Be Generic

## Questions

1. What is erasure? Why are Java generics implemented using erasure?

2. If your program uses` ArrayList<String>` and` ArrayList<Date>`, does the JVM load both of them?

3. Can you create an instance using new E() for a generic type E? Why
4. Can a method that uses a generic class parameter be static? Why?

5. Can you define a custom generic exception class? Why?