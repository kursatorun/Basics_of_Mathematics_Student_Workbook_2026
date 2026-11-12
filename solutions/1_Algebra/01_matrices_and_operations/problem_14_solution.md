
# Problem 14 — Rotation Matrices

## Problem Statement

We have the rotation matrix:

```math
R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}
```

We need to calculate R(alpha)R(beta) and show that it is equal to R(alpha + beta).

We also need to explain what this means geometrically.

## Theoretical Background and Concepts

A rotation matrix rotates a vector by an angle.

When we rotate a vector two times, the angles are added.

We can use sine and cosine formulas to check this.

## Detailed Step-by-Step Solution

### Step 1 — Write the two matrices

```math
R(\alpha)=\begin{pmatrix}\cos\alpha&-\sin\alpha\\\sin\alpha&\cos\alpha\end{pmatrix}
```

```math
R(\beta)=\begin{pmatrix}\cos\beta&-\sin\beta\\\sin\beta&\cos\beta\end{pmatrix}
```

### Step 2 — Multiply the matrices

```math
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha&-\sin\alpha\\
\sin\alpha&\cos\alpha
\end{pmatrix}
\begin{pmatrix}
\cos\beta&-\sin\beta\\
\sin\beta&\cos\beta
\end{pmatrix}
```

Calculate each entry:

Top-left:

```math
\cos\alpha\cos\beta-\sin\alpha\sin\beta
```

Top-right:

```math
-\cos\alpha\sin\beta-\sin\alpha\cos\beta
```

Bottom-left:

```math
\sin\alpha\cos\beta+\cos\alpha\sin\beta
```

Bottom-right:

```math
-\sin\alpha\sin\beta+\cos\alpha\cos\beta
```

### Step 3 — Use the angle formulas

We know:

```math
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta
```

```math
\sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta
```

Using these formulas, our matrix becomes:

```math
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta)&-\sin(\alpha+\beta)\\
\sin(\alpha+\beta)&\cos(\alpha+\beta)
\end{pmatrix}
```

This is exactly the rotation matrix for alpha + beta.

So:

```math
R(\alpha)R(\beta)=R(\alpha+\beta)
```

### Step 4 — Geometrical explanation

If we rotate a vector by beta degrees and then by alpha degrees, the total rotation is alpha + beta degrees.

For example, rotating 30 degrees and then 60 degrees gives a total rotation of 90 degrees.

So two rotations around the same origin can be combined into one rotation.

## Verification and Consistency Checks

Let's check with alpha = 90 degrees and beta = 90 degrees.

```math
R(90^\circ)=\begin{pmatrix}0&-1\\1&0\end{pmatrix}
```

Multiplying:

```math
R(90^\circ)R(90^\circ)=
\begin{pmatrix}0&-1\\1&0\end{pmatrix}
\begin{pmatrix}0&-1\\1&0\end{pmatrix}
```

```math
=\begin{pmatrix}-1&0\\0&-1\end{pmatrix}
```

This is the same as R(180 degrees).

So the result matches the formula.
