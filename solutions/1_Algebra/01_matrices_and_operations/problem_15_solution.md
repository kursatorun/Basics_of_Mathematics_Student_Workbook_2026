# Problem 15 — Associativity of Multiplication and Different Calculation Paths

## Problem Statement

We have three matrices:

$$
A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}
$$

$$
B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}
$$

$$
C=\begin{pmatrix}2&1\\0&-1\end{pmatrix}
$$

We need to calculate (AB)C and A(BC), compare the answers, and check the number of operations.

## Theoretical Background and Concepts

Matrix multiplication is associative.

This means we can change the grouping of matrices without changing the final answer.

$$
(AB)C=A(BC)
$$

But the number of calculations can be different.

## Detailed Step-by-Step Solution

### Step 1 — Find AB

First, multiply A by B.

$$
AB=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}
\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}
$$

Calculate:

- Top-left: 1(1) + 2(2) + 0(-1) = 5
- Top-right: 1(0) + 2(1) + 0(3) = 2
- Bottom-left: 0(1) + 1(2) + 1(-1) = 1
- Bottom-right: 0(0) + 1(1) + 1(3) = 4

$$
AB=\begin{pmatrix}5&2\\1&4\end{pmatrix}
$$

### Step 2 — Find (AB)C

$$
(AB)C=\begin{pmatrix}5&2\\1&4\end{pmatrix}
\begin{pmatrix}2&1\\0&-1\end{pmatrix}
$$

Calculate:

- Top-left: 5(2) + 2(0) = 10
- Top-right: 5(1) + 2(-1) = 3
- Bottom-left: 1(2) + 4(0) = 2
- Bottom-right: 1(1) + 4(-1) = -3

$$
(AB)C=\begin{pmatrix}10&3\\2&-3\end{pmatrix}
$$

### Step 3 — Find BC

Now we try the other order of grouping.

$$
BC=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}
\begin{pmatrix}2&1\\0&-1\end{pmatrix}
$$

Calculate:

- Row 1: 1(2) + 0(0) = 2, and 1(1) + 0(-1) = 1
- Row 2: 2(2) + 1(0) = 4, and 2(1) + 1(-1) = 1
- Row 3: -1(2) + 3(0) = -2, and -1(1) + 3(-1) = -4

$$
BC=\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}
$$

### Step 4 — Find A(BC)

$$
A(BC)=
\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}
\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}
$$

Calculate:

- Top-left: 1(2) + 2(4) + 0(-2) = 10
- Top-right: 1(1) + 2(1) + 0(-4) = 3
- Bottom-left: 0(2) + 1(4) + 1(-2) = 2
- Bottom-right: 0(1) + 1(1) + 1(-4) = -3

$$
A(BC)=\begin{pmatrix}10&3\\2&-3\end{pmatrix}
$$

### Step 5 — Compare the results

We found:

$$
(AB)C=\begin{pmatrix}10&3\\2&-3\end{pmatrix}
$$

$$
A(BC)=\begin{pmatrix}10&3\\2&-3\end{pmatrix}
$$

Both answers are equal.

This shows that matrix multiplication is associative.

### Step 6 — Compare the number of operations

Matrix sizes:

- A is 2x3.
- B is 3x2.
- C is 2x2.

For (AB)C:

- AB needs 2x2x3 = 12 multiplications.
- (AB)C needs 2x2x2 = 8 multiplications.
- Total = 20 multiplications.

For A(BC):

- BC needs 3x2x2 = 12 multiplications.
- A(BC) needs 2x2x3 = 12 multiplications.
- Total = 24 multiplications.

So (AB)C needs fewer multiplications.

If we also count additions:

- (AB)C needs 12 additions: 8 for AB and 4 for multiplying AB by C.
- A(BC) needs 14 additions.

The first method is faster in terms of arithmetic operations for these matrices.

## Verification and Consistency Checks

I checked both results.

- (AB)C gives rows (10, 3) and (2, -3).
- A(BC) gives the same rows.
- Both results have size 2x2.

The final matrices are equal, but the first method uses fewer operations.

This confirms the associative property.
