# Problem 4 — Matrix Multiplication and Noncommutativity

## Problem Statement

We are given two matrices:

$$
A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
$$

We need to:
1. Compute $AB$ and $BA$.
2. Check if $AB = BA$.
3. Explain what noncommutativity of matrix multiplication means.

## Theoretical Background and Concepts

To find an entry of a product, we take a row from the first matrix and a column from the second matrix. Then we multiply the matching numbers and add them.

For normal numbers, the order does not matter, for example $2 \cdot 3 = 3 \cdot 2$. For matrices, the order can change the answer. This is called noncommutativity.

## Detailed Step-by-Step Solution

### Step 1 — Compute $AB$

$$
AB = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
$$

- Top-left: $1\cdot2 + 2\cdot3 = 2 + 6 = 8$
- Top-right: $1\cdot0 + 2\cdot1 = 0 + 2 = 2$
- Bottom-left: $0\cdot2 + 1\cdot3 = 0 + 3 = 3$
- Bottom-right: $0\cdot0 + 1\cdot1 = 0 + 1 = 1$

$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
$$

### Step 2 — Compute $BA$

$$
BA = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
$$

- Top-left: $2\cdot1 + 0\cdot0 = 2 + 0 = 2$
- Top-right: $2\cdot2 + 0\cdot1 = 4 + 0 = 4$
- Bottom-left: $3\cdot1 + 1\cdot0 = 3 + 0 = 3$
- Bottom-right: $3\cdot2 + 1\cdot1 = 6 + 1 = 7$

$$
BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

### Step 3 — Compare

$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \ne \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix} = BA
$$

So $AB \ne BA$. This example shows that matrix multiplication is not commutative: changing the order of the matrices can change the result.

## Verification and Consistency Checks

- $A$ and $B$ are both $2\times2$, so $AB$ and $BA$ must both be $2\times2$. Our answers have this size.
- The top-left entries are different ($8$ and $2$), so the two matrices are not equal.
- I checked one entry again. For the top-right entry of $AB$, we use row 1 of $A$ and column 2 of $B$: $(1,2)\cdot(0,1) = 1\cdot0 + 2\cdot1 = 2$. It matches.
