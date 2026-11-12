# Exercise 15 — Classifying Three Systems

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0, \\
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4, \\
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5. \\
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## Method

Eliminate $x$ from the second row and inspect the result. Stop when the number of pivots, a redundant row, or a contradictory row determines the type.

## Solution

### System 1. One solution

The augmented matrix is

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
1 & -1 & \mid & 0 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2 \\
\end{pmatrix}.
$$

There is a pivot for each of the two unknowns and no contradictory row. Therefore the system has exactly one solution. No further row reduction is needed for the classification.

### System 2. Infinitely many solutions

The augmented matrix is

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 4 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-2R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

The second row means $0=0$ and adds no restriction. Only $x+y=2$ remains, so there is one free variable and infinitely many solutions.

### System 3. No solution

The augmented matrix is

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 5 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-2R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}.
$$

The second row means $0=1$. This contradiction makes the system inconsistent, so it has no solution.

**Result**

| System | Decisive information after elimination | Classification |
| --- | --- | --- |
| 1 | Two pivots for two unknowns | Exactly one solution |
| 2 | One pivot, one free variable, and $0=0$ | Infinitely many solutions |
| 3 | A contradictory row: $0=1$ | No solution |

## Verification

These classifications can also be checked directly from the original equations.

- **System 1:** adding and subtracting the equations determines $x=1$ and $y=1$ uniquely. This pair satisfies $1+1=2$ and $1-1=0$.
- **System 2:** the second equation is exactly twice the first, including its right-hand side. Every pair $(2-s,s)$ with $s\in\mathbb{R}$ satisfies both equations.
- **System 3:** twice the first equation requires $2x+2y=4$, whereas the second requires $2x+2y=5$. No pair can satisfy both.
