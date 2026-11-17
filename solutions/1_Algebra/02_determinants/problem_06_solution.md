
## Exercise 6 — Solution

Given matrix:

$$
A(t)=\begin{pmatrix}
t&1\\
2&t
\end{pmatrix}
$$

**Step 1: Calculate the determinant**

For a 2×2 matrix, we use:

$$
\det(A)=ad-bc
$$

Therefore:

$$
\det(A(t))=t\cdot t-1\cdot2
$$

$$
\det(A(t))=t^2-2
$$

**Step 2: Find when the matrix is not invertible**

A matrix is not invertible when its determinant is zero.

$$
t^2-2=0
$$

$$
t^2=2
$$

Taking the square root:

$$
\boxed{t=\pm\sqrt{2}}
$$

**Step 3: Verification**

For both values:

$$
\det(A(t))=(\pm\sqrt{2})^2-2
$$

$$
=2-2=0
$$

**Conclusion:**

The matrix is not invertible when:

$$
\boxed{t=\sqrt{2}\quad\text{or}\quad t=-\sqrt{2}}
$$

For all other real values of t, the determinant is not zero, so the matrix is invertible.
