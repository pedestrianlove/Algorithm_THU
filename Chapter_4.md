# Chapter 4. Multiplying Square Matrices

## Matrices multiplication.
$$
c_in = \sum_{k=1}^n a_{ik}\cdot b_{kj}
$$

```
MATRIX-MULTIPLY(A, B, C, n)
for i = 1 to n:
    for j = 1 to n:
        c_{ij} = 0
        for k = 1 to n:
            c_{ij} += a_{ik} * b_{kj}
```

## Matrices multiplication (Recursive) 
```
MATRIX-MULTIPLY-RECURSIVE(A, B, C, n)
if n == 1:
    c_{11} = c_{11} + a_{11} * b_{11}
    return

partition A, B and C into n/2 x n/2 submatrices:
    MATRIX-MULTIPLY-RECURSIVE(A_11, B_11, C_11, n/2);
    MATRIX-MULTIPLY-RECURSIVE(A_11, B_12, C_12, n/2);
    MATRIX-MULTIPLY-RECURSIVE(A_21, B_11, C_21, n/2);
    MATRIX-MULTIPLY-RECURSIVE(A_21, B_12, C_22, n/2);
    MATRIX-MULTIPLY-RECURSIVE(A_12, B_21, C_11, n/2);
    MATRIX-MULTIPLY-RECURSIVE(A_12, B_22, C_12, n/2);
    MATRIX-MULTIPLY-RECURSIVE(A_22, B_21, C_21, n/2);
    MATRIX-MULTIPLY-RECURSIVE(A_22, B_22, C_22, n/2);
```

### Improvement (Strassen's Method)

## Recursion
### 1. Substitution

### 2. Recursion Tree

### 3. Master method
Theorem 4.1 (Master theorem)
Let $a \geq 1$, $b > 1$ be constants. Let $f(n)$ be a function and $T(n)$ be defined on the natural number by the recurrence:
$$
T(n) = aT(\frac{n}{b}) + f(n)
$$

where $\frac{n}{b}$ equals to either $\floor{\frac{n}{b}}$ or $\ceil{\frac{n}{b}}$.
