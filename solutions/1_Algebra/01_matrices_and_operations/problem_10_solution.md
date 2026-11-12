
# Problem 10 — Columns of a Matrix Product

## Problem Statement

We have two matrices:

```math
A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}
```

```math
B=\begin{pmatrix}1&2\\-1&0\\3&1\end{pmatrix}
```

We need to find Ab1, Ab2, and AB. Then we compare the results.

## Theoretical Background and Concepts

When we multiply a matrix by a vector, we multiply each row by the vector and add the numbers.

The columns of AB can be found by multiplying A by each column of B.

## Detailed Step-by-Step Solution

### Step 1 — Find Ab1

The first column of B is:

```math
b_1=\begin{pmatrix}1\\-1\\3\end{pmatrix}
```

Now multiply:

```math
Ab_1=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}
\begin{pmatrix}1\\-1\\3\end{pmatrix}
```

Calculate:

- First entry: 1(1) + 2(-1) + 0(3) = -1
- Second entry: 0(1) + 1(-1) + 1(3) = 2

```math
Ab_1=\begin{pmatrix}-1\\2\end{pmatrix}
```

### Step 2 — Find Ab2

The second column of B is:

```math
b_2=\begin{pmatrix}2\\0\\1\end{pmatrix}
```

```math
Ab_2=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}
\begin{pmatrix}2\\0\\1\end{pmatrix}
```

Calculate:

- First entry: 1(2) + 2(0) + 0(1) = 2
- Second entry: 0(2) + 1(0) + 1(1) = 1

```math
Ab_2=\begin{pmatrix}2\\1\end{pmatrix}
```

### Step 3 — Find AB

```math
AB=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}
\begin{pmatrix}1&2\\-1&0\\3&1\end{pmatrix}
```

Calculate each entry:

- Top-left: 1(1) + 2(-1) + 0(3) = -1
- Top-right: 1(2) + 2(0) + 0(1) = 2
- Bottom-left: 0(1) + 1(-1) + 1(3) = 2
- Bottom-right: 0(2) + 1(0) + 1(1) = 1

```math
AB=\begin{pmatrix}-1&2\\2&1\end{pmatrix}
```

### Step 4 — Compare the results

The first column of AB is (-1, 2), which is Ab1.

The second column of AB is (2, 1), which is Ab2.

This happens because matrix multiplication calculates each column of the result by multiplying A with the matching column of B.

## Verification and Consistency Checks

- A is 2x3 and B is 3x2, so AB must be 2x2.
- The first column matches Ab1.
- The second column matches Ab2.

All the results match.
