# Exercise 14 — A Small Change in the Right-Hand Side

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3 \\
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1. \\
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Method

Compare the third equation with the sum of the first two. Use the same row operations on both augmented matrices to reveal whether the extra equation is redundant or contradictory. Treat the given decimal $3.1$ as an exact number.

## Solution

### 1. First system

The augmented matrix is

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & 3 \\
\end{pmatrix}.
$$

First apply $R_3\leftarrow R_3-R_1$, then $R_3\leftarrow R_3-R_2$. Together these subtract the sum of the first two original rows from the third. Finally apply $R_2\leftarrow R_2-2R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}.
$$

The last row is $0=0$. The second row gives $y=1$, and the first then gives $x=1$.

There is a pivot for each unknown, so the first system is consistent and has exactly one solution.

$$
(x,y)=(1,1).
$$

### 2. Second system

Only the final right-hand side changes.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & 3.1 \\
\end{pmatrix}.
$$

Apply the same three row operations, in the same order.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & 0 & \mid & 0.1 \\
\end{pmatrix}.
$$

The last row means $0=0.1$, which is impossible. The second system is inconsistent and has no solution.

**Result**

| Third equation | Consistency | Number of solutions |
| --- | --- | --- |
| $3x=3$ | Consistent | Exactly one: $(1,1)$ |
| $3x=3.1$ | Inconsistent | None |

### 3. Why the small change matters

Adding the first two equations always gives

$$
(x+y)+(2x-y)=2+1,\qquad 3x=3.
$$

In the first system, this agrees with the third equation, so that equation is redundant. In the second, it contradicts the third equation. Exact simultaneous equations must all hold; even a difference of $0.1$ makes these two requirements incompatible.

## Verification

For the first system, substitution of $(1,1)$ gives

$$
\begin{aligned}
1+1 &= 2, \\
2(1)-1 &= 1, \\
3(1) &= 3.
\end{aligned}
$$

For the second system, its unchanged first two equations still force $(1,1)$, but $3(1)=3\ne3.1$. Equivalently, subtracting their sum from the third equation gives the exact contradiction $0=3.1-3=1/10$.
