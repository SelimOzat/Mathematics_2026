# Exercise 3 — When Does the Inverse Not Exist?

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## Method

Check the determinant and the dependence of the rows separately. An invertible matrix must have nonzero determinant and independent rows.

## Solution

### 1. Determinant

$$
\det A=2(2)-4(1)=0.
$$

A square matrix with zero determinant is not invertible.

### 2. Dependence between rows

The first row is twice the second:

$$
(2,4)=2(1,2).
$$

Thus the rows are dependent. Subtracting twice the second row from the first produces a zero row, so the matrix cannot be reduced to $I$.

There is also a direct contradiction with the definition of an inverse. For any matrix $B$, the first row of $AB$ remains twice its second row. The rows of $I$ do not have this relation. Therefore $AB$ can never equal $I$.

**Result**

The matrix $A$ has no inverse. Both the zero determinant and the row dependence show the same loss of independent information.

## Verification

A nonzero vector is sent to zero:

$$
A
\begin{pmatrix}
2 \\
-1 \\
\end{pmatrix}
=\begin{pmatrix}
4-4 \\
2-2 \\
\end{pmatrix}
=\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}.
$$

If $A^{-1}$ existed, multiplying by it would force the nonzero vector $(2,-1)$ to equal the zero vector. This independently confirms noninvertibility.
