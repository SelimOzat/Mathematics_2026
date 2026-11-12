# Exercise 8 — Inverse of a Transformation

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

## Method

Invert each nonzero diagonal scaling factor. Interpret the result as undoing the original horizontal and vertical scalings.

## Solution

The matrix $S$ maps $(x,y)$ to $(2x,y/2)$. It doubles horizontal coordinates and halves vertical coordinates.

To undo these changes, halve the horizontal coordinate and double the vertical coordinate.

**Result**

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}.
$$

For example, take the vector $v=(1,2)^T$. The two successive actions are

$$
Sv=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\qquad
S^{-1}(Sv)=
\begin{pmatrix}
\frac12(2) \\
2(1) \\
\end{pmatrix}
=\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=v.
$$

## Verification

The coordinate factors cancel in both orders:

$$
SS^{-1}=S^{-1}S=
\begin{pmatrix}
2\cdot\frac12 & 0 \\
0 & \frac12\cdot2 \\
\end{pmatrix}
=I.
$$

Thus the inverse restores every vector, including the example above.
