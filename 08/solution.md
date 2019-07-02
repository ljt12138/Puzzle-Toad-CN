## 解答

设 $f_n(i)$ 表示走到 $(n, i)$ 最短路径的长度，我们对 $n$ 施归纳法说明
$$
\frac{1}{n}\sum_{1\le i\le n} f_n(i) \le H_n
$$
若能说明这一点，那么根据平均值原理就知道最小的 $f_n(i)$ 一定不超过 $H_n$。

- **基础：**当 $n=1$ 时，仅存在一条路径，上式显然成立

- **归纳：**当 $n > 1$ 时，如果有：
  $$
  \frac{1}{n}\sum_{1\le i\le n} f_n(i) \le H_n
  $$
  假设最小的 $f_n(i)$ 为 $f_n(i_0)$，那么如下不等式恒成立：
  $$
  \begin{aligned}
  f_{n+1}(1)&\le f_n(1)+w(n+1, 1)\\
  f_{n+1}(2)&\le f_n(2)+w(n+1, 2)\\
  &\dots\\
  f_{n+1}(i_0)&\le f_n(i_0)+w(n+1, i_0)\\
  f_{n+1}(i_0+1)&\le f_n(i_0)+w(n+1, i_0+1)\\
  f_{n+1}(i_0+2)&\le f_n(i_0+1)+w(n+1, i_0+2)\\
  &\dots\\
  f_{n+1}(n+1)&\le f_n(n) + w(n+1, n+1)
  \end{aligned}
  $$
  两边分别求和并除以 $\frac{1}{n+1}$ 便得到：
  $$
  \frac{1}{n+1}\sum_i f_{n+1}(i)\le \frac{1}{n+1}\left(\sum_{i} f_n(i)+\min\{f_n(i)\}+1\right)
  $$
  根据归纳假设有：
  $$
  \frac{1}{n+1}\left(\sum_{i} f_n(i)+\min\{f_n(i)\}+1\right)\le \frac{1}{n+1}\left(nH_n+H_n+1\right)=H_{n+1}
  $$
  这便完成了归纳。

