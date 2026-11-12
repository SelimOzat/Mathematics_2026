# Exercise 11 — A Parameter in a System of Three Equations

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3. \\
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Method

Subtract the first equation from the other two. Check when the resulting coefficients vanish before dividing by them. Here $x,y,z$ are the unknowns; $t$ is a fixed coefficient parameter whose value determines which system is being solved.

## Solution

### 1. Eliminate the first column

The augmented matrix is

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
1 & t & 1 & \mid & 2 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-R_1$ and $R_3\leftarrow R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t-1 & 0 & \mid & 1 \\
0 & 0 & t-1 & \mid & 2 \\
\end{pmatrix}.
$$

The last two rows mean $(t-1)y=1$ and $(t-1)z=2$. Division by $t-1$ is valid only if $t\ne1$.

### 2. Case $t=1$

The second row becomes $0=1$, and the third becomes $0=2$. These are contradictions, so the system has no solution. In the original system all three left-hand sides would be $x+y+z$, but they would have to equal three different numbers.

### 3. Case $t\ne1$

The last two rows determine $y$ and $z$. Back substitution into the first row gives $x$.

$$
\begin{aligned}
y &= \frac{1}{t-1}, \\
z &= \frac{2}{t-1}, \\
x &= 1-y-z \\
  &= 1-\frac{3}{t-1} \\
  &= \frac{t-4}{t-1}.
\end{aligned}
$$

There is a nonzero pivot for each unknown, so this solution is unique.

**Result**

| Parameter | Number of solutions |
| --- | --- |
| $t=1$ | No solution |
| $t\ne1$ | Exactly one solution |

For $t\ne1$, the solution is

$$
(x,y,z)=\left(\frac{t-4}{t-1},\frac{1}{t-1},\frac{2}{t-1}\right).
$$

No value of $t$ gives infinitely many solutions: at the only exceptional value, elimination produces contradictions rather than redundant equations.

## Verification

For $t\ne1$, substitution into all three original equations gives

$$
\begin{aligned}
x+y+z &= \frac{t-4+1+2}{t-1}=1, \\
x+ty+z &= \frac{t-4+t+2}{t-1}=2, \\
x+y+tz &= \frac{t-4+1+2t}{t-1}=3.
\end{aligned}
$$

For example, $t=2$ gives $(x,y,z)=(-2,1,2)$. The three left-hand sides are $1,2,3$, as required. The value $t=1$ was checked separately without division.
