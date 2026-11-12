# Exercise 15 — Two Methods for Solving the Same System

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Method

Compute the solution once with the inverse and once with Gaussian elimination. Compare the actual computations needed for this single right-hand side.

## Solution

### 1. Using the inverse

The determinant is $2(3)-1(1)=5$, so

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

Hence

$$
x=A^{-1}b=\frac15
\begin{pmatrix}
3(7)-8 \\
-7+2(8) \\
\end{pmatrix}
=\begin{pmatrix}
\frac{13}{5} \\
\frac95 \\
\end{pmatrix}.
$$

### 2. Using Gaussian elimination

Write $x=(x_1,x_2)^T$. Start with the augmented matrix

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}.
$$

Swap $R_1$ and $R_2$ to use a pivot equal to $1$.

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 & 1 & \mid & 7 \\
\end{pmatrix}.
$$

Apply $R_2\leftarrow R_2-2R_1$.

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & -5 & \mid & -9 \\
\end{pmatrix}.
$$

Back substitution gives

$$
\begin{aligned}
-5x_2 &= -9, & x_2 &= \frac95, \\
x_1 &= 8-3x_2, & x_1 &= 8-\frac{27}{5}=\frac{13}{5}.
\end{aligned}
$$

**Result from both methods**

$$
x=
\begin{pmatrix}
\frac{13}{5} \\
\frac95 \\
\end{pmatrix}.
$$

### 3. Compare the essential work

| Method | Essential computations in this example |
| --- | --- |
| Inverse | Evaluate one determinant, form the four inverse entries, and perform one matrix–vector product. That product uses four scalar multiplications and two additions. |
| Gaussian elimination | Perform one row swap and one row elimination, then solve two scalar equations by back substitution. |

For a single system solved from scratch, Gaussian elimination is simpler here: two row operations reach triangular form, and there is no need to construct a complete inverse. The counts above describe the computations performed, rather than treating different kinds of operations as equally costly.

If the inverse is already available, as in Exercise 6, multiplying it by the new right-hand side is convenient. The same inverse can also be reused for further right-hand sides.

## Verification

Substitute the common answer into the original system.

$$
\begin{aligned}
2x_1+x_2 &= \frac{26+9}{5}=7, \\
x_1+3x_2 &= \frac{13+27}{5}=8.
\end{aligned}
$$

Both original equations hold, and $\det A=5\ne0$ confirms that this solution is unique.
