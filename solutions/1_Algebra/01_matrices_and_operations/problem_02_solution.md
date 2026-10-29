# Problem 2 — Addition and Scalar Multiplication

## Problem Statement

We are given two matrices:

$$
A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
$$

We need to:
1. Compute $A+B$, $A-B$, and $3A-2B$.
2. Explain why matrix addition only works for matrices of the same size.

## Theoretical Background and Concepts

To add or subtract matrices, we add or subtract the numbers that are in the same position.
Scalar multiplication means multiplying every number in the matrix by that scalar.
Addition only works when both matrices have the same size, because each number needs a partner in the same position.

## Detailed Step-by-Step Solution

### Step 1 — Compute $A+B$

$$
A+B = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
$$

### Step 2 — Compute $A-B$

$$
A-B = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
$$

### Step 3 — Compute $3A-2B$

First we multiply each matrix by its number:

$$
3A = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}, \qquad 2B = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
$$

Now we subtract:

$$
3A-2B = \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
$$

### Step 4 — Why the sizes must match

Addition works position by position. If the matrices had different sizes, some numbers would have no partner in the other matrix, so we could not add them.

## Verification and Consistency Checks

- If we add $B$ back to $A-B$, we should get $A$:

$$
\begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = A
$$

- $A$ and $B$ are both $2 \times 2$, so $A+B$, $A-B$, and $3A-2B$ are also $2 \times 2$.
- Top-left entry of $3A-2B$: $3\cdot1 - 2\cdot4 = 3-8 = -5$, which matches.