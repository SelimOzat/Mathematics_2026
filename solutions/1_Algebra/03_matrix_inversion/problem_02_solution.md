# Exercise 2 — Formula for a 2×2 Matrix

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

## Method

For a $2\times2$ matrix, first check that the determinant is nonzero. Then interchange the diagonal entries, negate the off-diagonal entries, and divide by the determinant.

## Solution

The determinant is

$$
\det A=3(4)-2(5)=2\ne0.
$$

The inverse formula therefore applies.

$$
A^{-1}=\frac{1}{\det A}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}.
$$

**Result**

$$
A^{-1}=\frac12
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}
=\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix}.
$$

## Verification

Multiply by the original matrix.

$$
AA^{-1}=\frac12
\begin{pmatrix}
3(4)+2(-5) & 3(-2)+2(3) \\
5(4)+4(-5) & 5(-2)+4(3) \\
\end{pmatrix}
=\frac12
\begin{pmatrix}
2 & 0 \\
0 & 2 \\
\end{pmatrix}
=I.
$$
