# Exercise 4 — Gauss–Jordan

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## Method

Apply each elementary row operation to the entire augmented matrix $[A\mid I]$. Reduce the left block to $I$; the right block then gives $A^{-1}$.

## Solution

### 1. Form the augmented matrix

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}.
$$

### 2. Eliminate below the first pivot

Apply $R_2\leftarrow R_2-3R_1$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}.
$$

### 3. Normalize the second pivot

Apply $R_2\leftarrow -R_2$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}.
$$

### 4. Eliminate above the second pivot

Apply $R_1\leftarrow R_1-2R_2$.

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}.
$$

**Result**

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

### Why the right block is the inverse

Let $E$ represent the combined row operations. Applying them to the two blocks gives $[EA\mid EI]=[I\mid E]$. Every row operation is reversible, so $E$ is invertible. Since $EA=I$, it follows that $A=E^{-1}$ and hence $E=A^{-1}$.

## Verification

Check both products.

$$
AA^{-1}=
\begin{pmatrix}
-5+6 & 2-2 \\
-15+15 & 6-5 \\
\end{pmatrix}
=I,
\qquad
A^{-1}A=
\begin{pmatrix}
-5+6 & -10+10 \\
3-3 & 6-5 \\
\end{pmatrix}
=I.
$$
