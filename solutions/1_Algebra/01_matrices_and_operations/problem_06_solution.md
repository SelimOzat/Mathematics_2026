# Exercise 6 — Transpose

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

## Method

Transposition exchanges rows and columns. Calculate both sides of the product rule to verify it for the given matrices.

## Solution

**Transposes**

$$
A^T=\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix},\qquad B^T=\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}.
$$

**Product**

$$
AB=\begin{pmatrix}
1+4-3 & 0+2+9 \\
4+10-6 & 0+5+18 \\
\end{pmatrix}=\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}.
$$

**Result**

$$
(AB)^T=\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

## Verification

Multiplying the transposes in reversed order gives

$$
B^TA^T=\begin{pmatrix}
1+4-3 & 4+10-6 \\
0+2+9 & 0+5+18 \\
\end{pmatrix}=\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}=(AB)^T.
$$

Both sides have size $2\times2$. In general, transposition reverses the order of factors.
