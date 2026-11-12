# Exercise 14 — A Matrix That Is Its Own Inverse

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## Method

Use the definition of an inverse: a matrix is its own inverse if multiplying it by itself gives the identity. Construct an example that interchanges the two coordinates.

## Solution

The assumption $A^2=I$ means

$$
AA=I.
$$

Thus $A$ itself satisfies both requirements $AA^{-1}=I$ and $A^{-1}A=I$ when the proposed inverse is $A$.

**Result**

$$
A^{-1}=A.
$$

An example is

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Its off-diagonal entries are nonzero, so it is different from both $I$ and $-I$. Geometrically it interchanges the two coordinates; doing this twice restores the original vector.

## Verification

Direct multiplication gives

$$
A^2=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
=\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
=I.
$$

Therefore this example satisfies the hypothesis and has $A$ as its inverse.
