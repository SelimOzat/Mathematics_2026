# Exercise 3 — Inconsistent System

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7. \\
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Method

Eliminate the first unknown. A row with zero coefficients and a nonzero right-hand side represents a contradiction.

## Solution

The augmented matrix is

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 & 4 & \mid & 7 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-2R_1$.

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}.
$$

The last row represents $0x+0y=1$, or $0=1$. No values of $x,y$ can satisfy this equation.

**Result**

$$
\mathcal{S}=\varnothing.
$$

The system is inconsistent. Geometrically, the equations describe two distinct parallel lines.

## Verification

Doubling the first original equation requires $2x+4y=6$. The second original equation requires the same left-hand side to equal $7$. These conditions are incompatible.
