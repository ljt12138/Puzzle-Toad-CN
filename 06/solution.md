## 解答

**引理：** 任何时候所有孩子拥有的糖果数不超过初始时糖果最多的孩子（如果是奇数则$+1$）

**证明**：设 $M=\max\{a_i+(a_i\bmod 2)\}$，那么初始时一定满足 $a_i\le M$，并且对于每次操作
$$
a_i'=\frac{a_i+(a_i\bmod 2)+a_{(i+1)\bmod n}+(a_{(i+1)\bmod n)}\bmod 2)}{2}\le 2M/2=M
$$
**定理**：经过有限次后所有孩子糖果数都相等。

**证明**：定义势能函数 $\Phi(a)=\sum a_i^2$，由于加 $1$ 操作执行的次数是有限的，因此势能函数增加的总量是有限的。家下来我们证明势能函数在“传递糖果”的操作中会减小。

$$
\begin{aligned}
\Phi(a')-\Phi(a) &=\sum_i\left(\frac{a_i+a_{i+1}}{2}\right)^2-\sum_i a_i^2\\
&= \frac{1}{2}\left(\sum_i a_i^2+\sum_i a_ia_{i+1}\right)-\sum_i a_i^2\\
&= \frac{1}{2}\left(\sum_i a_ia_{i+1}-\sum_i a_i^2\right)
\end{aligned}
$$

根据排序不等式，当 $a_i$ 不全相等时总有

$$
\sum_i a_ia_{i+1}<\sum_i a_i^2
$$

这说明 $\Delta \Phi < 0$，那么显然经过有限次操作后 $a_i$ 必然全部相等。