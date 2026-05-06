## Steps

Step 1:
First consider $a_0 \geq 0$. Then all $a_i \geq 0$. For $a_i \geq 1$, since $\langle a_i \rangle < 1$ and $\lfloor a_i \rfloor \geq 1$, we have

$$
\lfloor a_{i+1} \rfloor \leq a_{i+1} = \lfloor a_i \rfloor \cdot \langle a_i \rangle < \lfloor a_i \rfloor.
$$

Thus the sequence $\lfloor a_i \rfloor$ is strictly decreasing as long as its terms are in $[1, \infty)$. Eventually a term from $[0,1)$ appears, after which all subsequent terms are $0$. Hence for $a_0 \geq 0$, the sequence eventually becomes constantly $0$, so $a_i = a_{i+2}$ for all sufficiently large $i$.

Step 2:
Now consider $a_0 < 0$; then all $a_i \leq 0$. Suppose the sequence never hits $0$. Then $\lfloor a_i \rfloor \leq -1$ for all $i$. Since $\lfloor a_i \rfloor < 0$ and $0 \leq \langle a_i \rangle < 1$, we have

$$
\lfloor a_i \rfloor < a_{i+1} = \lfloor a_i \rfloor \cdot \langle a_i \rangle < 1 + \lfloor a_{i+1} \rfloor.
$$

This means $\lfloor a_{i+1} \rfloor \geq \lfloor a_i \rfloor$, so the sequence $\lfloor a_i \rfloor$ is nondecreasing. Since all terms are integers in $(-\infty, -1]$, this sequence must become constant:

$$
\lfloor a_i \rfloor = c \quad \text{for} \quad i \geq i_0,
$$

where $c$ is a negative integer.

Step 3:
Once $\lfloor a_i \rfloor = c$ for $i \geq i_0$, the recurrence becomes

$$
a_{i+1} = c \cdot \langle a_i \rangle = c(a_i - c) = ca_i - c^2.
$$

Define the auxiliary sequence

$$
b_i = a_i - \frac{c^2}{c-1}.
$$

Then

$$
b_{i+1} = a_{i+1} - \frac{c^2}{c-1} = ca_i - c^2 - \frac{c^2}{c-1} = c\left(a_i - \frac{c^2}{c-1}\right) = cb_i,
$$

which implies $b_i = c^{i-i_0} b_{i_0}$ for $i \geq i_0$.

Step 4:
Since all $a_i$ for $i \geq i_0$ lie in $[c, c+1)$, the sequence $(b_i)$ is bounded. The relation $b_i = c^{i-i_0} b_{i_0}$ can only hold for a bounded sequence if either $b_{i_0} = 0$ or $|c| = 1$, i.e., $c = -1$.

**Case 1:** If $b_{i_0} = 0$, then $b_i = 0$ for all $i \geq i_0$, so $a_i = \frac{c^2}{c-1}$ is constant, and $a_i = a_{i+2}$.

**Case 2:** If $c = -1$, then $a_i = -\frac{1}{2} + (-1)^{i-i_0} b_{i_0}$, giving

$$
a_i = \begin{cases} a_{i_0} & \text{for } i = i_0, i_0+2, i_0+4, \ldots, \\ -1 - a_{i_0} & \text{for } i = i_0+1, i_0+3, i_0+5, \ldots \end{cases}
$$

In this case the sequence alternates between two values in $(-1, 0)$, so $a_i = a_{i+2}$.

Step 5:
Summarizing: from some index onward, the sequence $(a_i)$ either is constant or alternates between two values in $(-1, 0)$. In both cases, $a_i = a_{i+2}$ for all sufficiently large $i$.

Final Answer: $\boxed{a_i = a_{i+2} \text{ for all sufficiently large } i}$

---

## Answer

$a_i = a_{i+2} \text{ for all sufficiently large } i$

---

## Classification

**Problem Type:** Symbolic derivation

**Answer Type:** Exact symbolic expression
