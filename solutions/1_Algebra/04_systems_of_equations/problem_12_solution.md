# Exercise 12 — Homogeneous System

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0. \\
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

## Method

Use Gaussian elimination to identify the independent equations and a free variable. A homogeneous system has zero on every right-hand side, so the zero vector always satisfies it.

## Solution

### 1. Eliminate dependent rows

The augmented matrix is

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
2 & 4 & -2 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$.

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
\end{pmatrix}.
$$

Swap $R_2$ and $R_3$, then divide the new second row by $-3$.

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 1 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

### 2. Express the pivot variables using a free variable

The second row gives $y-z=0$, so $y=z$. The first row then gives $x+z=0$, so $x=-z$.

The variable $z$ is free. Set $z=s$, where $s\in\mathbb{R}$.

**Result**

$$
(x,y,z)=(-s,s,s),\qquad s\in\mathbb{R}.
$$

Equivalently, the solution vector is

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
=s
\begin{pmatrix}
-1 \\
1 \\
1 \\
\end{pmatrix}.
$$

There are infinitely many solutions, forming a line through the origin. Every solution must have $y=z$ and $x=-z$, so this parameterization includes all of them.

### 3. Why the zero vector is always a solution

In any homogeneous linear system, substituting zero for every unknown makes every left-hand side zero, matching the right-hand side. Here $s=0$ gives $(0,0,0)$.

## Verification

Substitute $(-s,s,s)$ into each original equation.

$$
\begin{aligned}
-s+2s-s &= 0, \\
2(-s)+4s-2s &= 0, \\
-s-s+2s &= 0.
\end{aligned}
$$

All three equations hold for every real $s$. In particular, $s=1$ gives the nonzero solution $(-1,1,1)$, while $s=0$ gives the zero solution.
