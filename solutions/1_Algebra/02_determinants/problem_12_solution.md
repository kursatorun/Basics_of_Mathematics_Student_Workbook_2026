
## Exercise 12 — Solution

Given matrix:

$$
A(t)=\begin{pmatrix}
1&2&3\\
2&4&t\\
0&1&1
\end{pmatrix}
$$

**Step 1: Apply the given row operation**

$$
R_2\leftarrow R_2-2R_1
$$

The new matrix is:

$$
\begin{pmatrix}
1&2&3\\
0&0&t-6\\
0&1&1
\end{pmatrix}
$$

This row operation does not change the determinant.

**Step 2: Calculate the determinant**

Expand along the first column:

$$
\det(A)=1\cdot
\begin{vmatrix}
0&t-6\\
1&1
\end{vmatrix}
$$

$$
=0\cdot1-(t-6)\cdot1
$$

$$
=-(t-6)
$$

$$
\boxed{\det(A)=6-t}
$$

**Step 3: Find when the matrix is not invertible**

A matrix is not invertible when its determinant is zero.

$$
6-t=0
$$

$$
\boxed{t=6}
$$

**Step 4: Verification**

When t = 6, the original matrix becomes:

$$
A(6)=\begin{pmatrix}
1&2&3\\
2&4&6\\
0&1&1
\end{pmatrix}
$$

The second row is twice the first row:

$$
R_2=2R_1
$$

This means the rows are linearly dependent, so the determinant is zero.

**Conclusion:**

The matrix is not invertible when:

$$
\boxed{t=6}
$$

At this value, the second row is twice the first row.
