# Exercise 12 — Formula for a Matrix Power

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## Method

Compute the first powers to identify a pattern. Prove the pattern for every positive integer by mathematical induction.

## Solution

**Initial powers**

$$
A^2=\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad A^3=\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix},\qquad A^4=\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}.
$$

**Conjecture and result**

$$
A^n=\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix},\qquad n\ge1.
$$

**Induction proof**

The formula holds for $n=1$. Assume it holds for a positive integer $n$. Multiplication by $A$ gives

$$
A^{n+1}=A^nA=\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}.
$$

This is exactly the formula with $n+1$ in place of $n$. The base case and induction step prove the formula for all positive integers.

## Verification

Write $A=I+N$, where $N$ has only one nonzero entry, $n_{12}=1$. Since $N^2=0$, the binomial expansion gives $(I+N)^n=I+nN$, which confirms the same formula. For $n=0$, the formula also gives $A^0=I$.
