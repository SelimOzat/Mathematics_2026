# Exercise 1 — Matrix Size and Entries

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Method

A matrix size is the number of rows followed by the number of columns. In $a_{ij}$, $i$ selects the row and $j$ selects the column.

## Solution

**Sizes**

$A$ has two rows and three columns. $B$ has three rows and two columns.

$$
A\in\mathbb{R}^{2\times3},\qquad B\in\mathbb{R}^{3\times2}.
$$

**Entries**

$$
a_{12}=-1,\qquad a_{23}=5,\qquad b_{21}=-2,\qquad b_{32}=1.
$$

**Row and column vectors**

The second row of $A$ is a row vector. The first column of $B$ is a column vector.

$$
R_2(A)=\begin{pmatrix}
0 & 4 & 5 \\
\end{pmatrix},\qquad C_1(B)=\begin{pmatrix}
1 \\
-2 \\
4 \\
\end{pmatrix}.
$$

## Verification

The row vector has three entries, matching the three columns of $A$. The column vector has three entries, matching the three rows of $B$. The entry $b_{32}=1$ is the last entry in the second column of $B$.
