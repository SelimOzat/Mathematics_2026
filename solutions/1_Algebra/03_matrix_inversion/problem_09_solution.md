# Exercise 9 — Matrix Equation

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## Method

In $AX=B$, the matrix $A$ multiplies $X$ from the left. Multiply both sides on the left by $A^{-1}$ so that $A^{-1}A$ cancels.

## Solution

### 1. Choose the correct side

Before calculating,

$$
A^{-1}(AX)=A^{-1}B,\qquad X=A^{-1}B.
$$

Multiplication on the right would produce $AXA^{-1}=BA^{-1}$, where $A$ and $A^{-1}$ are separated by $X$ and cannot be cancelled.

### 2. Compute the inverse and the solution

Since $\det A=1$,

$$
A^{-1}=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}.
$$

Therefore

$$
X=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
=\begin{pmatrix}
3-4 & 1-8 \\
2 & 4 \\
\end{pmatrix}.
$$

**Result**

$$
X=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$

## Verification

Substitute the computed matrix into $AX$.

$$
AX=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
=\begin{pmatrix}
-1+4 & -7+8 \\
2 & 4 \\
\end{pmatrix}
=\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
=B.
$$
