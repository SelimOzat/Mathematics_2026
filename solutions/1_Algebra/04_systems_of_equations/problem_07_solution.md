# Exercise 7 — Choosing a Method Deliberately

[Exercise sheet](../../../exercises/1_Algebra/04_systems_of_equations_en.md)

## Problem

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8; \\
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Method

Choose a method from the matrix structure, the number of right-hand sides, and the information already available.

## Solution

### Case 1. Triangular matrix

Use back substitution. The system is already upper triangular.

$$
\begin{pmatrix}
2 & -1 & \mid & 3 \\
0 & 4 & \mid & 8 \\
\end{pmatrix}.
$$

The second row gives $4y=8$, so $y=2$. The first row gives $2x-y=3$.

$$
2x-2=3,\qquad x=\frac52.
$$

**Result for case 1**

$$
(x,y)=\left(\frac52,2\right).
$$

### Case 2. Three right-hand sides and a known inverse

Use the inverse that is already supplied.

$$
x_i=A^{-1}b_i,\qquad i=1,2,3.
$$

The same matrix $A^{-1}$ is reused in all three matrix–vector products. Recomputing the inverse or performing three separate eliminations would repeat work already represented by the known inverse.

### Case 3. One 3×3 system and no supplied inverse

Use Gaussian elimination on the augmented matrix formed from $A$ and the single vector $b$, then use back substitution. Only one right-hand side must be carried through the row operations.

Computing the entire inverse would require solving for three identity columns before multiplying by $b$. For this single requested solution, elimination works directly with the needed right-hand side.

## Verification

For case 1,

$$
2\left(\frac52\right)-2=3,\qquad 4(2)=8.
$$

For case 2, the inverse identity verifies the plan.

$$
A(A^{-1}b_i)=(AA^{-1})b_i=b_i.
$$

For case 3, the resulting candidate should be substituted into $Ax=b$. If elimination produces a zero or contradictory row, classify the solution set from that row before back substitution. Numerical coefficients are supplied only in case 1, whose solution is given above.
