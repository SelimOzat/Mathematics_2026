# Exercise 1 — From a System to a Matrix

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7. \\
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Method

Keep the unknowns in the fixed order $x,y,z$. Each equation supplies one row of the coefficient matrix and one entry of the right-hand side.

## Solution

**Coefficient matrix**

$$
A=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}.
$$

**Unknown vector and right-hand side**

$$
\mathbf{x}=
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix},\qquad
b=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}.
$$

**Result**

$$
A\mathbf{x}=b.
$$

The first row contains the coefficients $2,-1,1$ of the first equation. The second row contains $1,3,-2$, and the third contains $3,1,1$. The corresponding constants are $4,1,7$.

## Verification

Multiplying the matrix by the unknown vector recovers the three left-hand sides in their original order.

$$
A\mathbf{x}=
\begin{pmatrix}
2x-y+z \\
x+3y-2z \\
3x+y+z \\
\end{pmatrix}=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}.
$$

Thus the matrix equation is equivalent to the given system.
