# Exercise 10 — Columns of a Matrix Product

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Method

Apply $A$ to each column of $B$. The $j$th column of $AB$ is $A$ multiplied by the $j$th column of $B$.

## Solution

**Images of the columns**

$$
b_1=\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},\qquad b_2=\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}.
$$

$$
Ab_1=\begin{pmatrix}
1-2+0 \\
0-1+3 \\
\end{pmatrix}=\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}.
$$

$$
Ab_2=\begin{pmatrix}
2+0+0 \\
0+0+1 \\
\end{pmatrix}=\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

**Product and result**

$$
AB=\left(Ab_1\; Ab_2\right)=\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

Fixing a column of $B$ and taking its dot product with every row of $A$ gives exactly that column of $AB$. This explains why the two calculations agree.

## Verification

Use the sum of the columns as an additional check.

$$
A(b_1+b_2)=A\begin{pmatrix}
3 \\
-1 \\
4 \\
\end{pmatrix}=\begin{pmatrix}
1 \\
3 \\
\end{pmatrix}=Ab_1+Ab_2.
$$

The result is also the sum of the two columns of the computed product.
