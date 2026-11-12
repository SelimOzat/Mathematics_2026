# Exercise 8 — Row Operations and Their Reversibility

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Method

Apply each operation to the current matrix in the stated order. A row addition is reversed by subtracting the same multiple, and a row swap reverses itself.

## Solution

**Step 1**

Apply $R_2\leftarrow R_2-2R_1$.

$$
A_1=\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

**Step 2**

Apply $R_3\leftarrow R_3+R_1$.

$$
A_2=\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}.
$$

**Step 3 and result**

Interchange $R_2$ and $R_3$.

$$
A_3=\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}.
$$

| Original operation | Reversing operation |
| --- | --- |
| $R_2\leftarrow R_2-2R_1$ | $R_2\leftarrow R_2+2R_1$ |
| $R_3\leftarrow R_3+R_1$ | $R_3\leftarrow R_3-R_1$ |
| $R_2\leftrightarrow R_3$ | $R_2\leftrightarrow R_3$ |

## Verification

Undo the operations in reverse order. First swap the last two rows of $A_3$ to recover $A_2$. Then

$$
(0,3,2)-(1,2,-1)=(-1,1,3).
$$

Finally,

$$
(0,0,3)+2(1,2,-1)=(2,4,1).
$$

Together with the unchanged first row, these are exactly the original rows of $A$.
