# Exercise 4 — Triangular Matrix

[Exercise sheet](../../../exercises/1_Algebra/02_determinants_en.md)

## Problem

Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

## Method

The determinant of any square upper or lower triangular matrix is the product of its diagonal entries.

## Solution

The given matrix is upper triangular because every entry below the diagonal is zero. Its diagonal entries are $2$, $-3$, and $7$.

**Result**

$$
\det A=2\cdot(-3)\cdot7=-42.
$$

For a triangular $n\times n$ matrix $T$,

$$
\det T=\prod_{i=1}^{n}t_{ii}.
$$

The triangular pattern makes the product of diagonal entries the only potentially nonzero term in the determinant sum.

## Verification

As a structural check, $R_1\leftarrow R_1+\frac43R_2$ removes the entry $4$, $R_2\leftarrow R_2-\frac57R_3$ removes the entry $5$, and $R_1\leftarrow R_1-\frac{23}{21}R_3$ removes the remaining upper-right entry. All three operations preserve the determinant and give

$$
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

The diagonal product is still $-42$.
