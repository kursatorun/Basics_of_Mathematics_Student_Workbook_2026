
## Exercise 9 — Solution

Given two vectors:

$$
u=\begin{pmatrix}3\\1\end{pmatrix},
\qquad
v=\begin{pmatrix}1\\4\end{pmatrix}
$$

**Step 1: Calculate the determinant**

The area of a parallelogram is the absolute value of the determinant.

$$
\text{Area}=|\det(u,v)|
$$

Using the vectors as columns:

$$
\det(u,v)=
\begin{vmatrix}
3&1\\
1&4
\end{vmatrix}
$$

$$
=3\cdot4-1\cdot1
$$

$$
=12-1=11
$$

Therefore:

$$
\boxed{\text{Area}=11}
$$

**Step 2: Reverse the order of the vectors**

Now we use v first and u second:

$$
\det(v,u)=
\begin{vmatrix}
1&3\\
4&1
\end{vmatrix}
$$

$$
=1\cdot1-3\cdot4
$$

$$
=1-12=-11
$$

**Step 3: Calculate the area again**

$$
\text{Area}=|-11|
$$

$$
\boxed{\text{Area}=11}
$$

**Conclusion:**

The area of the parallelogram is **11 square units**.

When we reverse the order of the vectors, the determinant changes from 11 to -11.

However, the area stays the same because we use the absolute value of the determinant.
