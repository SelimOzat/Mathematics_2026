# Exercise 13 — A Recurrence Written in Matrix Form

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$
0,1,1,2,3,5,8,\ldots
$$

and describe the relationship you observe. Then compute

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## Method

Repeated multiplication gives the powers. Interpret multiplication by $F$ as an update of a pair of consecutive Fibonacci numbers.

## Solution

**Powers**

$$
F^2=\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad F^3=\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

$$
F^4=\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},\qquad F^5=\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

Define $f_0=0$, $f_1=1$, and $f_{n+1}=f_n+f_{n-1}$. The entries follow

$$
F^n=\begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1} \\
\end{pmatrix},\qquad n\ge1.
$$

**Recurrence step**

$$
F\begin{pmatrix}
a \\
b \\
\end{pmatrix}=\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}.
$$

If $a=f_{n+1}$ and $b=f_n$, the new pair is $(f_{n+2},f_{n+1})$. The first entry is the new sum, and the second entry retains the previous first entry.

## Verification

Starting from $(1,0)^T$ gives the successive pairs $(1,1)^T$, $(2,1)^T$, $(3,2)^T$, $(5,3)^T$, and $(8,5)^T$. These match the first columns of $F$, $F^2$, $F^3$, $F^4$, and $F^5$. Multiplying the general displayed form by $F$ also updates each entry using the recurrence.
