
## Exercise 14 — Solution

Given the system Ax = b, where:

$$
A=\begin{pmatrix}
1&2\\
k&4
\end{pmatrix}
$$

**Step 1: Calculate the determinant**

For a 2×2 matrix:

$$
\det(A)=ad-bc
$$

Therefore:

$$
\det(A)=1\cdot4-2\cdot k
$$

$$
\det(A)=4-2k
$$

**Step 2: Find when there is exactly one solution**

The system has exactly one solution for every b when the determinant is not zero.

$$
4-2k\neq0
$$

$$
\boxed{k\neq2}
$$

**Step 3: Check the special case k = 2**

When k = 2:

$$
A=\begin{pmatrix}
1&2\\
2&4
\end{pmatrix}
$$

The second row is twice the first row, so the determinant is zero.

**Step 4: Example with infinitely many solutions**

Choose:

$$
b=\begin{pmatrix}1\\2\end{pmatrix}
$$

The system becomes:

$$
x_1+2x_2=1
$$

$$
2x_1+4x_2=2
$$

The second equation is twice the first equation.

Let:

$$
x_2=s
$$

Then:

$$
x_1=1-2s
$$

So the solutions are:

$$
\boxed{x_1=1-2s,\quad x_2=s,\quad s\in\mathbb{R}}
$$

There are infinitely many solutions because s can be any real number.

**Step 5: Example with no solution**

Choose:

$$
b=\begin{pmatrix}1\\3\end{pmatrix}
$$

The system becomes:

$$
x_1+2x_2=1
$$

$$
2x_1+4x_2=3
$$

Multiplying the first equation by 2 gives:

$$
2x_1+4x_2=2
$$

But the second equation says:

$$
2x_1+4x_2=3
$$

This is a contradiction, so there is no solution.

**Conclusion:**

For k ≠ 2, the system has exactly one solution for every b.

For k = 2:
- If b = (1, 2), there are infinitely many solutions.
- If b = (1, 3), there is no solution.
