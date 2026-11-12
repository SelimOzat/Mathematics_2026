# Exercise 13 — Does Every Equation Add New Information?

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Method

Use elimination in the fixed variable order $x_1,x_2,x_3$. A zero row indicates an equation that adds no new restriction. Identify that dependency directly in the original equations.

## Solution

### 1. Eliminate the first column

The augmented matrix is

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
1 & 0 & -1 & \mid & 2 \\
\end{pmatrix}.
$$

Apply $R_3\leftarrow R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & -8 \\
\end{pmatrix}.
$$

Apply $R_3\leftarrow R_3+R_2$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

The last row means $0=0$. There are two pivots and three unknowns, so one variable is free.

### 2. Parameterize all solutions

Set $x_3=s$, where $s\in\mathbb{R}$. Back substitution gives

$$
\begin{aligned}
x_2 &= 8-s, \\
x_1 &= 10-x_2=2+s.
\end{aligned}
$$

**Result**

$$
(x_1,x_2,x_3)=(2+s,8-s,s),\qquad s\in\mathbb{R}.
$$

The system has infinitely many solutions.

### 3. Show the redundant equation

Subtract the second original equation from the first.

$$
\begin{aligned}
(x_1+x_2)-(x_2+x_3) &= 10-8, \\
x_1-x_3 &= 2.
\end{aligned}
$$

This is exactly the third equation, including its right-hand side. Thus the first two equations already describe the whole solution set; the third adds no new information. All three equations are not independently necessary.

## Verification

For every real $s$,

$$
\begin{aligned}
(2+s)+(8-s) &= 10, \\
(8-s)+s &= 8, \\
(2+s)-s &= 2.
\end{aligned}
$$

All three original equations hold. Conversely, the first two equations force $x_2=8-x_3$ and $x_1=2+x_3$, so no other solutions are omitted.
