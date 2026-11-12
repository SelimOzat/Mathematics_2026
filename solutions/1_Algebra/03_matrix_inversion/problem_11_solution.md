# Exercise 11 — Parameter and Invertibility

[Exercise sheet](../../../exercises/1_Algebra/03_matrix_inversion_en.md)

## Problem

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## Method

Find the parameter values where the determinant is zero before applying the inverse formula. Examine those excluded values in the original matrix.

## Solution

The determinant factors as

$$
\det A(t)=1-t^2=(1-t)(1+t).
$$

It is nonzero exactly when $t\ne1$ and $t\ne-1$. For these values the $2\times2$ formula gives the inverse.

**Result**

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix},\qquad t\ne\pm1.
$$

At $t=1$, the two rows of $A(t)$ are equal. At $t=-1$, they are negatives of one another. Both matrices are singular.

The denominator of the inverse formula is zero at these excluded values, so the formula is undefined there. This reflects actual noninvertibility, rather than a removable problem with the notation.

## Verification

For every allowed value of $t$,

$$
A(t)A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1-t^2 & -t+t \\
t-t & 1-t^2 \\
\end{pmatrix}
=I.
$$

The reverse product gives the same diagonal matrix before division. At the excluded values, $A(1)(1,-1)^T=0$ and $A(-1)(1,1)^T=0$ give nonzero vectors sent to zero, confirming that no inverse exists.
