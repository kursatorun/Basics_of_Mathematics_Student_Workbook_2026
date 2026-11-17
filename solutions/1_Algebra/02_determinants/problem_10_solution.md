
## Exercise 10 — Solution

Given matrix:

$$
A=\begin{pmatrix}
1&2&3\\
2&4&6\\
0&1&5
\end{pmatrix}
$$

**Step 1: Check the rows**

We can see that the second row is twice the first row.

$$
R_1=(1,2,3)
$$

$$
R_2=(2,4,6)
$$

Therefore:

$$
R_2=2R_1
$$

**Step 2: Use the determinant property**

If one row is a multiple of another row, the rows are linearly dependent.

A matrix with linearly dependent rows has a determinant equal to zero.

Therefore:

$$
\boxed{\det(A)=0}
$$

**Step 3: Explain invertibility**

A square matrix is invertible only if its determinant is not zero.

Since:

$$
\det(A)=0
$$

Matrix A is not invertible.

**Conclusion:**

The determinant is **0** because the second row is twice the first row.

The rows are linearly dependent, so the matrix is not invertible.
