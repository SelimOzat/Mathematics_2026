# Exercise 5 — Row Echelon Form and Number of Solutions

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Method

Read the pivot columns and the zero row directly from the echelon matrix. Use back substitution to express the pivot variables in terms of the nonpivot variable.

## Solution

### 1. Identify pivots and a free variable

The first two columns contain pivots, corresponding to $x$ and $y$. The third column has no pivot, so $z$ is free. The last row gives $0=0$ and adds no restriction.

There are three unknowns and two pivots. Therefore there is one free variable.

### 2. Back substitution

Set $z=t$, where $t\in\mathbb{R}$. The second row gives

$$
y+2z=1,\qquad y=1-2t.
$$

Substitute into the first row.

$$
\begin{aligned}
x+2y-z &= 3, \\
x+2(1-2t)-t &= 3, \\
x &= 1+5t.
\end{aligned}
$$

**Result**

$$
(x,y,z)=(1+5t,1-2t,t),\qquad t\in\mathbb{R}.
$$

The system has infinitely many solutions. Its solution set is a line with direction vector $(5,-2,1)$.

## Verification

Substitution into the nonzero rows gives

$$
\begin{aligned}
(1+5t)+2(1-2t)-t &= 3, \\
(1-2t)+2t &= 1.
\end{aligned}
$$

Both identities hold for every real $t$. For example, $t=1$ gives $(6,-1,1)$, which satisfies $6+2(-1)-1=3$ and $-1+2(1)=1$.
