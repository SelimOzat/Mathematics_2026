# Exercise 2 — Addition and Scalar Multiplication

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

## Method

Add and subtract corresponding entries. Scalar multiplication multiplies every entry by the same number.

## Solution

**Addition**

$$
A+B=\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix}=\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}.
$$

**Subtraction**

$$
A-B=\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix}=\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}.
$$

**Linear combination**

$$
3A-2B=\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}-\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}=\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

Matrix addition requires equal numbers of rows and columns so that every entry has a corresponding entry in the other matrix.

## Verification

Subtracting $B$ from the computed sum recovers $A$.

$$
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}-\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}=\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=A.
$$
