# Exercise 3 — When Can Matrices Be Multiplied?

[Exercise sheet](../../../exercises/1_Algebra/01_matrices_and_operations_en.md)

## Problem

The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Method

A product of an $m\times n$ matrix and an $n\times p$ matrix is defined and has size $m\times p$. The two inner dimensions must agree.

## Solution

| Product | Inner dimensions | Defined? | Resulting size |
| --- | --- | --- | --- |
| $AB$ | $3=3$ | Yes | $2\times4$ |
| $BA$ | $4\ne2$ | No | — |
| $BC$ | $4=4$ | Yes | $3\times2$ |
| $CB$ | $2\ne3$ | No | — |
| $AC$ | $3\ne4$ | No | — |
| $CA$ | $2=2$ | Yes | $4\times3$ |
| $AD$ | $3\ne2$ | No | — |
| $DA$ | $2=2$ | Yes | $2\times3$ |

**Result**

The defined products are $AB$, $BC$, $CA$, and $DA$.

## Verification

For $CA$, each row of $C$ and each column of $A$ has two entries, so their dot product is defined. Four rows of $C$ and three columns of $A$ give twelve entries in a $4\times3$ result. The same row–column test gives every entry in the table.
