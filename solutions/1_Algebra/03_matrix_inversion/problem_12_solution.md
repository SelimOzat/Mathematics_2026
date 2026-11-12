# Exercise 12 — Finding Inverses Without Starting from Scratch

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## Method

Write $M=A^{-1}$ and reuse it. Apply the inverse rules for a nonzero scalar multiple, a transpose, and a power; there is no need to recover $A$.

## Solution

### 1. Inverse of the scalar multiple

The scalar factor is inverted as well as the matrix.

$$
(3A)^{-1}=\frac13A^{-1}
=\frac13
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
=\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix}.
$$

### 2. Inverse of the transpose

Taking an inverse commutes with taking a transpose.

$$
(A^T)^{-1}=(A^{-1})^T
=\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}.
$$

### 3. Inverse of the square

Use $(A^2)^{-1}=(A^{-1})^2=M^2$.

$$
M^2=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
=\begin{pmatrix}
4+3 & -2-2 \\
-6-6 & 3+4 \\
\end{pmatrix}.
$$

**Result for the square**

$$
(A^2)^{-1}=
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}.
$$

## Verification

Since $AM=MA=I$, each proposed expression satisfies the defining inverse identities.

$$
\begin{aligned}
(3A)\left(\frac13M\right) &= AM=I, \\
\left(\frac13M\right)(3A) &= MA=I, \\
A^TM^T &= (MA)^T=I, \\
M^TA^T &= (AM)^T=I, \\
A^2M^2 &= A(AM)M=I, \\
M^2A^2 &= M(MA)A=I.
\end{aligned}
$$

These checks use only the supplied inverse and its properties, without calculating $A$.
