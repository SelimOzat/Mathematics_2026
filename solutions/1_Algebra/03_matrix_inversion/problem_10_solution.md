# Exercise 10 — Inverse of a Diagonal Matrix

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## Method

A diagonal matrix is invertible exactly when every diagonal entry is nonzero. Its inverse contains the reciprocal diagonal entries, so no elimination is needed.

## Solution

### 1. The matrix $D$

The diagonal entries $2,-3,5$ are all nonzero. Taking their reciprocals gives the inverse.

**Result**

$$
D^{-1}=
\begin{pmatrix}
\frac12 & 0 & 0 \\
0 & -\frac13 & 0 \\
0 & 0 & \frac15 \\
\end{pmatrix}.
$$

### 2. The matrix $E$

The second diagonal entry of $E$ is zero. In particular, $E(0,1,0)^T=(0,0,0)^T$, so it loses the second coordinate and cannot be reversed.

Equivalently, for every matrix $B$, the second row of $EB$ is zero and therefore cannot be the second row of $I_3$.

Thus $D$ is invertible and $E$ is not invertible.

## Verification

For $D$, multiplication in either order gives

$$
DD^{-1}=D^{-1}D=
\begin{pmatrix}
2\cdot\frac12 & 0 & 0 \\
0 & (-3)\left(-\frac13\right) & 0 \\
0 & 0 & 5\cdot\frac15 \\
\end{pmatrix}
=I_3.
$$

For $E$, a supposed inverse would imply $(0,1,0)^T=E^{-1}E(0,1,0)^T=(0,0,0)^T$, a contradiction.
