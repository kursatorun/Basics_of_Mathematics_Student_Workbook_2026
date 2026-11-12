
# Problem 13 — A Recurrence Written in Matrix Form

## Problem Statement

We have:

```math
F=\begin{pmatrix}1&1\\1&0\end{pmatrix}
```

We need to find F², F³, F⁴, and F⁵.

Then we compare the numbers with the sequence 0, 1, 1, 2, 3, 5, 8, ...

We also need to multiply F by a vector with entries a and b.

## Theoretical Background and Concepts

The sequence is called the Fibonacci sequence.

Each new number is the sum of the previous two numbers.

For example, 2 + 3 = 5 and 3 + 5 = 8.

## Detailed Step-by-Step Solution

### Step 1 — Find F²

```math
F^2=\begin{pmatrix}1&1\\1&0\end{pmatrix}
\begin{pmatrix}1&1\\1&0\end{pmatrix}
```

Calculate:

- Top-left: 1(1) + 1(1) = 2
- Top-right: 1(1) + 1(0) = 1
- Bottom-left: 1(1) + 0(1) = 1
- Bottom-right: 1(1) + 0(0) = 1

```math
F^2=\begin{pmatrix}2&1\\1&1\end{pmatrix}
```

### Step 2 — Find F³

```math
F^3=F^2F
```

```math
F^3=\begin{pmatrix}2&1\\1&1\end{pmatrix}
\begin{pmatrix}1&1\\1&0\end{pmatrix}
```

Calculate:

- Top-left: 2 + 1 = 3
- Top-right: 2
- Bottom-left: 1 + 1 = 2
- Bottom-right: 1

```math
F^3=\begin{pmatrix}3&2\\2&1\end{pmatrix}
```

### Step 3 — Find F⁴

```math
F^4=F^3F
```

```math
F^4=\begin{pmatrix}3&2\\2&1\end{pmatrix}
\begin{pmatrix}1&1\\1&0\end{pmatrix}
```

```math
F^4=\begin{pmatrix}5&3\\3&2\end{pmatrix}
```

### Step 4 — Find F⁵

```math
F^5=F^4F
```

```math
F^5=\begin{pmatrix}5&3\\3&2\end{pmatrix}
\begin{pmatrix}1&1\\1&0\end{pmatrix}
```

```math
F^5=\begin{pmatrix}8&5\\5&3\end{pmatrix}
```

### Step 5 — Compare with the sequence

We can see the numbers 1, 2, 3, 5, and 8 in the matrices.

These are Fibonacci numbers.

Each new matrix has numbers made by adding the previous numbers.

### Step 6 — Multiply F by a vector

```math
F\begin{pmatrix}a\\b\end{pmatrix}
=
\begin{pmatrix}1&1\\1&0\end{pmatrix}
\begin{pmatrix}a\\b\end{pmatrix}
```

Calculate:

- First entry: 1(a) + 1(b) = a + b
- Second entry: 1(a) + 0(b) = a

```math
F\begin{pmatrix}a\\b\end{pmatrix}
=\begin{pmatrix}a+b\\a\end{pmatrix}
```

The first entry adds the two numbers. The second entry keeps a.

This is how the matrix creates the next step of the Fibonacci sequence.

## Verification and Consistency Checks

I checked the powers again.

- F² has 2, 1, 1, 1.
- F³ has 3, 2, 2, 1.
- F⁴ has 5, 3, 3, 2.
- F⁵ has 8, 5, 5, 3.

The numbers follow the Fibonacci sequence.

The vector multiplication also gives (a + b, a), so the result is correct.
