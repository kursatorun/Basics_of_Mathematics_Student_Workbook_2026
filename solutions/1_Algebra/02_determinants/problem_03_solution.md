
## Exercise 3 — Solution

Given matrix:

$$
A=\begin{pmatrix}
1&2&0\\
0&3&1\\
2&1&1
\end{pmatrix}
$$

**Step 1: Calculate det(A)**

Expand along the first row:

$$
\det(A)=1(3\cdot1-1\cdot1)-2(0\cdot1-1\cdot2)
$$

$$
=1(3-1)-2(0-2)
$$

$$
=2+4=\boxed{6}
$$

**Step 2: Swap the first two rows**

After swapping the rows:

$$
B=\begin{pmatrix}
0&3&1\\
1&2&0\\
2&1&1
\end{pmatrix}
$$

Swapping two rows changes the sign of the determinant.

Therefore:

$$
\det(B)=-\det(A)
$$

$$
\boxed{\det(B)=-6}
$$

**Step 3: Verification**

Calculate det(B) using the first row:

$$
\det(B)=-3(1\cdot1-0\cdot2)+1(1\cdot1-2\cdot2)
$$

$$
=-3(1)+(1-4)
$$

$$
=-3-3=-6
$$

**Conclusion:**

$$
\boxed{\det(A)=6,\quad\det(B)=-6}
$$

The result confirms that swapping two rows changes the sign of the determinant.
