
# Problem 12 — Formula for a Matrix Power

## Problem Statement

We have:

```math
A=\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

We need to calculate A², A³, and A⁴, find a pattern for Aⁿ, and explain why the formula works for n + 1.

## Theoretical Background and Concepts

A matrix power means multiplying the matrix by itself.

For example, A² = A times A.

We can use the first few results to find a pattern.

## Detailed Step-by-Step Solution

### Step 1 — Find A²

```math
A^2=\begin{pmatrix}1&1\\0&1\end{pmatrix}
\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

Calculate:

- Top-left: 1(1) + 1(0) = 1
- Top-right: 1(1) + 1(1) = 2
- Bottom-left: 0(1) + 1(0) = 0
- Bottom-right: 0(1) + 1(1) = 1

```math
A^2=\begin{pmatrix}1&2\\0&1\end{pmatrix}
```

### Step 2 — Find A³

```math
A^3=A^2A
```

```math
A^3=\begin{pmatrix}1&2\\0&1\end{pmatrix}
\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

The top-right entry is 1(1) + 2(1) = 3.

```math
A^3=\begin{pmatrix}1&3\\0&1\end{pmatrix}
```

### Step 3 — Find A⁴

```math
A^4=A^3A
```

```math
A^4=\begin{pmatrix}1&3\\0&1\end{pmatrix}
\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

The top-right entry is 1(1) + 3(1) = 4.

```math
A^4=\begin{pmatrix}1&4\\0&1\end{pmatrix}
```

### Step 4 — Find the pattern

The top-right number increases by 1 each time.

The diagonal numbers stay 1 and the bottom-left number stays 0.

So I think the formula is:

```math
A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}
```

### Step 5 — Check the formula for n + 1

Assume the formula works for n.

Multiply Aⁿ by A:

```math
A^{n+1}=\begin{pmatrix}1&n\\0&1\end{pmatrix}
\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

Calculate:

- Top-left: 1
- Top-right: 1 + n
- Bottom-left: 0
- Bottom-right: 1

```math
A^{n+1}=\begin{pmatrix}1&n+1\\0&1\end{pmatrix}
```

This is the same formula with n replaced by n + 1.

Since it works for n = 1, and each step gives the next power, the formula works for every positive integer n.

## Verification and Consistency Checks

Using the formula:

- n = 2 gives top-right 2.
- n = 3 gives top-right 3.
- n = 4 gives top-right 4.

These match our calculations.

The formula is correct.
