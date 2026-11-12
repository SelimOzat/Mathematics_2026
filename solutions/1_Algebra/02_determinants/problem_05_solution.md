# Exercise 5 — Row Operations

[Exercise sheet](../../../exercises/1_Algebra/02_determinants_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Method

Create zeros below the diagonal using row additions. Replacing one row by itself plus a multiple of a different row preserves the determinant.

## Solution

**Step 1**

Apply $R_2\leftarrow R_2-2R_1$. The determinant is unchanged.

$$
A_1=\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}.
$$

**Step 2**

Apply $R_3\leftarrow R_3+R_1$. The determinant is unchanged.

$$
A_2=\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}.
$$

**Step 3**

Apply $R_3\leftarrow R_3+2R_2$. The determinant is unchanged.

$$
U=\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}.
$$

**Result**

No row swaps or row scalings were used, so there is no extra factor.

$$
\det A=\det U=1\cdot(-3)\cdot(-7)=21.
$$

## Verification

A direct expansion along the first row provides an independent check.

$$
\det A=1(1\cdot2-0\cdot4)-2(2\cdot2-0(-1))+3(2\cdot4-1(-1)).
$$

$$
\det A=2-8+27=21.
$$
