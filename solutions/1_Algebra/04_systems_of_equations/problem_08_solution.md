# Exercise 8 — Two Systems with the Same Coefficient Matrix

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1, \\
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4. \\
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Method

The systems have the same coefficient matrix. Carry both right-hand sides through one sequence of elimination steps, then back substitute for each column separately.

## Solution

### 1. Place the right-hand sides side by side

The first column to the right of the divider belongs to the first system. The second belongs to the second system.

$$
\begin{pmatrix}
2 & 1 & \mid & 5 & 1 \\
1 & -1 & \mid & 1 & 4 \\
\end{pmatrix}.
$$

Swap $R_1$ and $R_2$.

$$
\begin{pmatrix}
1 & -1 & \mid & 1 & 4 \\
2 & 1 & \mid & 5 & 1 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-2R_1$ to every column.

$$
\begin{pmatrix}
1 & -1 & \mid & 1 & 4 \\
0 & 3 & \mid & 3 & -7 \\
\end{pmatrix}.
$$

### 2. Back substitute in the first system

$$
3y_1=3,\qquad y_1=1,\qquad x_1-y_1=1,\qquad x_1=2.
$$

### 3. Back substitute in the second system

$$
3y_2=-7,\qquad y_2=-\frac73,\qquad x_2-y_2=4,\qquad x_2=\frac53.
$$

**Result**

$$
(x_1,y_1)=(2,1),\qquad (x_2,y_2)=\left(\frac53,-\frac73\right).
$$

The pivot choices, row swap, and elimination multiplier are identical because they depend on the coefficient matrix. The transformed right-hand sides and the resulting solutions differ.

## Verification

For the first system,

$$
2(2)+1=5,\qquad 2-1=1.
$$

For the second system,

$$
2\left(\frac53\right)-\frac73=1,\qquad \frac53-\left(-\frac73\right)=4.
$$

Both original systems are satisfied.
