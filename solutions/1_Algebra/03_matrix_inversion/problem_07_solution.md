# Exercise 7 — Inverse of a Product

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## Method

Compute $AB$ and invert that matrix directly. Then find $A^{-1}$ and $B^{-1}$ separately and compare $B^{-1}A^{-1}$ with the direct answer.

## Solution

### 1. Invert the product directly

$$
AB=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix},\qquad \det(AB)=6.
$$

The $2\times2$ inverse formula gives

$$
(AB)^{-1}=\frac16
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix}
=\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}.
$$

### 2. Multiply the separate inverses in reverse order

$$
A^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix},\qquad
B^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}.
$$

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
=\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}.
$$

**Result**

$$
(AB)^{-1}=B^{-1}A^{-1}.
$$

For column vectors, $AB$ applies $B$ first and $A$ second. To undo this, apply $A^{-1}$ first and $B^{-1}$ second, which is the product $B^{-1}A^{-1}$.

## Verification

The order places each inverse next to the matrix it cancels:

$$
\begin{aligned}
(AB)(B^{-1}A^{-1}) &= A(BB^{-1})A^{-1}=I, \\
(B^{-1}A^{-1})(AB) &= B^{-1}(A^{-1}A)B=I.
\end{aligned}
$$

Both the numerical matrices and the inverse identities agree.
