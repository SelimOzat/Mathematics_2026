# Exercise 7 — Identity Matrix, Zero Matrix, and Powers

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Method

Use $I=I_2$ and the $2\times2$ zero matrix. A power of $A$ means repeated matrix multiplication.

## Solution

**Neutral elements**

$$
I=\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad 0=\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}.
$$

$$
AI=IA=A+0=A=\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}.
$$

The identity matrix preserves a matrix under multiplication. The zero matrix preserves it under addition.

**Powers**

$$
A^2=\begin{pmatrix}
4 & 2+2 \\
0 & 4 \\
\end{pmatrix}=\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}.
$$

$$
A^3=A^2A=\begin{pmatrix}
8 & 4+8 \\
0 & 8 \\
\end{pmatrix}=\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

**Pattern**

The diagonal entries double at each step. For integers $n\ge1$,

$$
A^n=\begin{pmatrix}
2^n & n2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

## Verification

Let $N=A-2I$. Then $N^2=0$. In $(2I+N)^n$, only the constant term and the term linear in $N$ remain.

$$
A^n=2^n I+n2^{n-1}N.
$$

This gives the stated pattern and reproduces the computed squares and cubes.
