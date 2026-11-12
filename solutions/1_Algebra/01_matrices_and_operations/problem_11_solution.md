# Exercise 11 — When Do Matrices Commute?

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

## Method

Calculate $AB$ and $BA$ symbolically and equate corresponding entries. This gives necessary conditions, which can then be checked by substitution.

## Solution

**Compare the products**

$$
AB=\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix},\qquad BA=\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}.
$$

Equality of the upper-left entries gives $a+c=a$, so $c=0$. Equality of the upper-right entries gives $b+d=a+b$, so $d=a$. The remaining entries impose the same condition $c=0$ and no further restriction.

**Result**

$$
B=\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix},\qquad a,b\in\mathbb{R}.
$$

## Verification

Substituting this form produces identical products.

$$
AB=BA=\begin{pmatrix}
a & a+b \\
0 & a \\
\end{pmatrix}.
$$

Thus the conditions are both necessary and sufficient.
