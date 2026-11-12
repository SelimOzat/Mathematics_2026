# Exercise 15 — Associativity of Multiplication and Different Calculation Paths

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Method

Compare the two parenthesizations while keeping the factor order $A,B,C$ fixed. Count scalar multiplications and additions in the standard row–column algorithm.

## Solution

**First path, $(AB)C$**

$$
AB=\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}.
$$

$$
(AB)C=\begin{pmatrix}
5\cdot2+2\cdot0 & 5\cdot1+2(-1) \\
1\cdot2+4\cdot0 & 1\cdot1+4(-1) \\
\end{pmatrix}=\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Second path, $A(BC)$**

$$
BC=\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}.
$$

$$
A(BC)=\begin{pmatrix}
2+8+0 & 1+2+0 \\
0+4-2 & 0+1-4 \\
\end{pmatrix}=\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Operation counts**

For an $m\times n$ matrix times an $n\times p$ matrix, the standard algorithm uses $mnp$ scalar multiplications and $mp(n-1)$ additions. These counts include operations involving zeros and ones.

| Stage | Multiplications | Additions |
| --- | ---: | ---: |
| $AB$, then $(AB)C$ | $12+8=20$ | $8+4=12$ |
| $BC$, then $A(BC)$ | $12+12=24$ | $6+8=14$ |

**Result**

$$
(AB)C=A(BC)=\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

Associativity permits changing the parentheses. The factor order is preserved. The first path uses fewer scalar operations under the stated counting convention.

## Verification

The two paths independently produce the same four entries. As a further column check, $C$ has first column $(2,0)^T$, so the first column of $(AB)C$ must be twice the first column of $AB$, namely $(10,2)^T$. This matches the final matrix.
