# Exercise 13 — Undoing a Composite Transformation

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

## Method

First invert $T=HS$ directly. Then undo the two transformations in reverse order and compare with the product in the incorrect order.

## Solution

### 1. Compute $T$, then invert it

$$
T=HS=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
=\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Its determinant is $2$, so

$$
T^{-1}=\frac12
\begin{pmatrix}
1 & -1 \\
0 & 2 \\
\end{pmatrix}
=\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

### 2. Use the inverse-of-a-product rule

The separate inverses are

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad
H^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

Therefore

$$
S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}
=T^{-1}.
$$

The two methods give the same matrix.

### 3. Compare with the incorrect order

$$
H^{-1}S^{-1}=
\begin{pmatrix}
\frac12 & -1 \\
0 & 1 \\
\end{pmatrix}
\ne T^{-1}.
$$

The upper-right entries differ: $-1$ instead of $-1/2$.

**Result**

$$
(HS)^{-1}=S^{-1}H^{-1}
=\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

For a column vector, $HS$ first applies the scaling $S$ and then the shear $H$. Undo the shear first with $H^{-1}$, then undo the scaling with $S^{-1}$. Written as a matrix product, this is $S^{-1}H^{-1}$.

## Verification

The correct product gives the identity:

$$
TT^{-1}=
\begin{pmatrix}
1 & -1+1 \\
0 & 1 \\
\end{pmatrix}
=I.
$$

The incorrect order fails the inverse test:

$$
T(H^{-1}S^{-1})=
\begin{pmatrix}
1 & -2+1 \\
0 & 1 \\
\end{pmatrix}
=\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\ne I.
$$
