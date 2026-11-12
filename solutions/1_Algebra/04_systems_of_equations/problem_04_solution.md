# Exercise 4 — Infinitely Many Solutions

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0. \\
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Method

Reduce the augmented matrix to echelon form. Express the pivot variables in terms of a free variable.

## Solution

### 1. Elimination

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}.
$$

Swap the last two rows and divide the new second row by $-2$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 1 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

### 2. Parameterize the solution

The second row gives $y=1$. The first row then gives $x+z=1$. The variable $z$ is free, so set $z=t$, where $t\in\mathbb{R}$.

**Result**

$$
(x,y,z)=(1-t,1,t),\qquad t\in\mathbb{R}.
$$

Equivalently,

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}
+t
\begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix}.
$$

There are infinitely many solutions, forming a line in three-dimensional space.

## Verification

Choose $t=2$. Then $(x,y,z)=(-1,1,2)$, and

$$
\begin{aligned}
-1+1+2 &= 2, \\
2(-1)+2(1)+2(2) &= 4, \\
-1-1+2 &= 0.
\end{aligned}
$$

More generally, substitution of $(1-t,1,t)$ gives $2,4,0$ for every real $t$.
