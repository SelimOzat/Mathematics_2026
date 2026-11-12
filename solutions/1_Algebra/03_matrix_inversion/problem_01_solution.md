# Exercise 1 — Definition of the Inverse

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Method

Use the definition: $B$ is the inverse of $A$ when both $AB=I$ and $BA=I$. Compute the products directly, without an inverse formula.

## Solution

The entries of $AB$ are obtained by multiplying rows of $A$ by columns of $B$.

$$
AB=
\begin{pmatrix}
2(1)+1(-1) & 2(-1)+1(2) \\
1(1)+1(-1) & 1(-1)+1(2) \\
\end{pmatrix}
=\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

The reverse product must also be checked.

$$
BA=
\begin{pmatrix}
1(2)+(-1)(1) & 1(1)+(-1)(1) \\
(-1)(2)+2(1) & (-1)(1)+2(1) \\
\end{pmatrix}
=\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

**Result**

$$
B=A^{-1}=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

## Verification

Both direct products equal the identity matrix. Thus $B$ satisfies the defining equations of an inverse on both sides; no inverse formula was needed.
