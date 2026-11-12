# Exercise 2 — Gaussian Elimination — One Solution

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2. \\
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

## Method

Use Gaussian elimination on the augmented matrix, then apply back substitution. Row additions and row swaps preserve the solution set.

## Solution

### 1. Form the augmented matrix

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}.
$$

### 2. Eliminate the first column

Apply $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}.
$$

Swap $R_2$ and $R_3$ to use the pivot $1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}.
$$

Apply $R_3\leftarrow R_3+3R_2$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}.
$$

### 3. Back substitution

The last row gives $-7z=-21$, so $z=3$. The second row gives $y-2z=-4$, so $y=2$. The first row gives $x+y+z=6$, so $x=1$.

**Result**

$$
(x,y,z)=(1,2,3).
$$

There is a pivot for every unknown, so the solution is unique.

## Verification

Substitute the result into every original equation.

$$
\begin{aligned}
1+2+3 &= 6, \\
2(1)-2+3 &= 3, \\
1+2(2)-3 &= 2.
\end{aligned}
$$

All three equations hold.
