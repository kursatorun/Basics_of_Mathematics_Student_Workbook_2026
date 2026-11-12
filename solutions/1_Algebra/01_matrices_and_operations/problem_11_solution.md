
# Problem 11 — When Do Matrices Commute?

## Problem Statement

We have:

```math
A=\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

```math
B=\begin{pmatrix}a&b\\c&d\end{pmatrix}
```

We need to find when AB = BA and describe the possible matrices B.

## Theoretical Background and Concepts

Matrix multiplication is not always commutative. This means AB and BA can be different.

To find when they are equal, we calculate both products and compare their entries.

## Detailed Step-by-Step Solution

### Step 1 — Find AB

```math
AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}
\begin{pmatrix}a&b\\c&d\end{pmatrix}
```

Calculate:

- Top-left: a + c
- Top-right: b + d
- Bottom-left: c
- Bottom-right: d

```math
AB=\begin{pmatrix}a+c&b+d\\c&d\end{pmatrix}
```

### Step 2 — Find BA

```math
BA=\begin{pmatrix}a&b\\c&d\end{pmatrix}
\begin{pmatrix}1&1\\0&1\end{pmatrix}
```

Calculate:

- Top-left: a
- Top-right: a + b
- Bottom-left: c
- Bottom-right: c + d

```math
BA=\begin{pmatrix}a&a+b\\c&c+d\end{pmatrix}
```

### Step 3 — Compare

For AB = BA, the matching entries must be equal.

```math
a+c=a
```

So c = 0.

```math
b+d=a+b
```

So d = a.

The other entries also agree when c = 0.

### Step 4 — Final answer

We found:

- c = 0
- d = a
- a and b can be any numbers.

So the general form of B is:

```math
B=\begin{pmatrix}a&b\\0&a\end{pmatrix}
```

## Verification and Consistency Checks

We put c = 0 and d = a into both products.

```math
AB=\begin{pmatrix}a&a+b\\0&a\end{pmatrix}
```

```math
BA=\begin{pmatrix}a&a+b\\0&a\end{pmatrix}
```

Both results are equal, so the conditions are correct.
