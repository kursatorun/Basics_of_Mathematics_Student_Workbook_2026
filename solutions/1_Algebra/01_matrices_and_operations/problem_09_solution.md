
# Problem 9 — Composing Transformations

## Problem Statement

We have two matrices and a vector:

```math
S=\begin{pmatrix}2&0\\0&1\end{pmatrix}
```

```math
R=\begin{pmatrix}0&-1\\1&0\end{pmatrix}
```

```math
x=\begin{pmatrix}1\\2\end{pmatrix}
```

We need to find RSx and SRx, compare the answers, and explain why the order matters.

## Theoretical Background and Concepts

Matrix S changes the size of a vector. It multiplies the first coordinate by 2 and keeps the second coordinate the same.

Matrix R rotates a vector 90 degrees counterclockwise.

When we multiply matrices and vectors, we start from the right side.

## Detailed Step-by-Step Solution

### Step 1 — Find RSx

First, we calculate Sx:

```math
Sx=\begin{pmatrix}2&0\\0&1\end{pmatrix}
\begin{pmatrix}1\\2\end{pmatrix}
```

Calculate:

- First entry: 2(1) + 0(2) = 2
- Second entry: 0(1) + 1(2) = 2

So:

```math
Sx=\begin{pmatrix}2\\2\end{pmatrix}
```

Now we multiply by R:

```math
RSx=\begin{pmatrix}0&-1\\1&0\end{pmatrix}
\begin{pmatrix}2\\2\end{pmatrix}
```

Calculate:

- First entry: 0(2) + (-1)(2) = -2
- Second entry: 1(2) + 0(2) = 2

The result is:

```math
RSx=\begin{pmatrix}-2\\2\end{pmatrix}
```

### Step 2 — Find SRx

First, we calculate Rx:

```math
Rx=\begin{pmatrix}0&-1\\1&0\end{pmatrix}
\begin{pmatrix}1\\2\end{pmatrix}
```

Calculate:

- First entry: 0(1) + (-1)(2) = -2
- Second entry: 1(1) + 0(2) = 1

So:

```math
Rx=\begin{pmatrix}-2\\1\end{pmatrix}
```

Now we multiply by S:

```math
SRx=\begin{pmatrix}2&0\\0&1\end{pmatrix}
\begin{pmatrix}-2\\1\end{pmatrix}
```

Calculate:

- First entry: 2(-2) + 0(1) = -4
- Second entry: 0(-2) + 1(1) = 1

The result is:

```math
SRx=\begin{pmatrix}-4\\1\end{pmatrix}
```

### Step 3 — Compare the results

We have:

```math
RSx=\begin{pmatrix}-2\\2\end{pmatrix}
```

```math
SRx=\begin{pmatrix}-4\\1\end{pmatrix}
```

The results are different, so RSx is not equal to SRx.

In RSx, we first stretch the vector horizontally and then rotate it.

In SRx, we first rotate the vector and then stretch it horizontally.

The order matters because the rotation changes the direction of the vector. So the scaling affects different coordinates depending on when we apply it.

## Verification and Consistency Checks

I checked the calculations again.

- Sx = (2, 2), and rotating it gives (-2, 2).
- Rx = (-2, 1), and scaling it gives (-4, 1).

Both answers are correct.

This shows that changing the order of the transformations can change the final vector.
