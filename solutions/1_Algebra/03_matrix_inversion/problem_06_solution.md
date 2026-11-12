# Exercise 6 — Solving a System Using the Inverse

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

## Method

Check that $A$ is invertible, compute its inverse, and multiply $Ax=b$ on the left by $A^{-1}$ to obtain $x=A^{-1}b$.

## Solution

The determinant is $2(3)-1(1)=5\ne0$. Thus

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

Write the unknown vector as $x=(x_1,x_2)^T$. Multiplying on the left gives

$$
x=A^{-1}b
=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}
=\frac15
\begin{pmatrix}
15-7 \\
-5+14 \\
\end{pmatrix}.
$$

**Result**

$$
x=
\begin{pmatrix}
\frac85 \\
\frac95 \\
\end{pmatrix}.
$$

The solution is unique because $A$ is invertible.

## Verification

Substitute the vector into the original equation.

$$
Ax=\frac15
\begin{pmatrix}
2(8)+9 \\
8+3(9) \\
\end{pmatrix}
=\frac15
\begin{pmatrix}
25 \\
35 \\
\end{pmatrix}
=\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}
=b.
$$
