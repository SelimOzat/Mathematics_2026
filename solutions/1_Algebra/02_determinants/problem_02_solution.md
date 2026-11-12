# Exercise 2 — Determinant of a 3×3 Matrix

[Exercise sheet](../../../exercises/1_Algebra/02_determinants_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Method

Sarrus' rule applies to $3\times3$ matrices. Subtract the sum of the three upward diagonal products from the sum of the three downward diagonal products.

## Solution

**Downward diagonal products**

$$
P=1\cdot3\cdot5+2\cdot4\cdot2+(-1)\cdot0\cdot1=15+16+0=31.
$$

**Upward diagonal products**

$$
Q=(-1)\cdot3\cdot2+2\cdot0\cdot5+1\cdot4\cdot1=-6+0+4=-2.
$$

**Result**

$$
\det A=P-Q=31-(-2)=33.
$$

## Verification

Adding a multiple of one row to another preserves the determinant. Apply $R_3\leftarrow R_3-2R_1$.

$$
A_1=\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}.
$$

The first column has one nonzero entry, so

$$
\det A=\det A_1=1\cdot\bigl(3\cdot7-4(-3)\bigr)=21+12=33.
$$

This confirms Sarrus' result using a determinant-preserving row operation.
