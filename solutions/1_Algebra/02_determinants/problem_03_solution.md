# Exercise 3 — Swapping Two Rows

[Exercise sheet](../../../exercises/1_Algebra/02_determinants_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## Method

Compute the original determinant, use the row-swap property to predict the new determinant, then calculate the new value independently.

## Solution

**Original determinant**

Expand along the first row.

$$
\det A=1(3\cdot1-1\cdot1)-2(0\cdot1-1\cdot2)=2+4=6.
$$

**Swap and prediction**

$$
B=\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

One interchange of two rows reverses the sign of a determinant.

$$
\det B=-\det A=-6.
$$

**Result**

$$
\det A=6,\qquad \det B=-6.
$$

## Verification

Expand $\det B$ along its first row.

$$
\det B=-3(1\cdot1-0\cdot2)+1(1\cdot1-2\cdot2)=-3-3=-6.
$$

The calculated value agrees with the prediction.
