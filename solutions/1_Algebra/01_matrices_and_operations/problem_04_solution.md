# Exercise 4 — Matrix Multiplication and Noncommutativity

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Method

Each entry of a product is the dot product of a row of the left matrix and a column of the right matrix. Compute both orders separately.

## Solution

**Product $AB$**

$$
AB=\begin{pmatrix}
1\cdot2+2\cdot3 & 1\cdot0+2\cdot1 \\
0\cdot2+1\cdot3 & 0\cdot0+1\cdot1 \\
\end{pmatrix}=\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}.
$$

**Product $BA$**

$$
BA=\begin{pmatrix}
2\cdot1+0\cdot0 & 2\cdot2+0\cdot1 \\
3\cdot1+1\cdot0 & 3\cdot2+1\cdot1 \\
\end{pmatrix}=\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

**Result**

$$
AB\ne BA.
$$

The upper-left entries are already different, $8\ne2$. Noncommutativity means that changing the order of two matrix factors can change the result.

## Verification

Apply the matrices to $e_1=(1,0)^T$ in two stages.

$$
A(Be_1)=A\begin{pmatrix}
2 \\
3 \\
\end{pmatrix}=\begin{pmatrix}
8 \\
3 \\
\end{pmatrix},\qquad B(Ae_1)=B\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}=\begin{pmatrix}
2 \\
3 \\
\end{pmatrix}.
$$

These are the first columns of the computed products, and they are different.
