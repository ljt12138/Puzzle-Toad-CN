## 解答

当且仅当 $n = 2^k$ 时，Rikka 总可以在有限次将所有台灯关闭。

**证明：**先证充分性，施归纳于 $k$：

- 基础：$k = 0$ 时显然可以一次关闭打开的灯
- 归纳：$k > 0​$ 时我们将 $i​$ 号灯和 $i+2^{k-1}​$ 号灯看作一个“大灯”，这个灯亮当且仅当两个灯状态不同。那么根据归纳假设所有的大灯都会灭，即两灯颜色相同，这就规约到了 $2^{k-1}​$ 个大灯的情景。

再证必要性，设 $n=s\times 2^k$，其中 $s$ 为奇数，我们将所有灯分为 $2^k$ 组。初始时，Yuki 仅仅将其中一盏灯打开，容易说明可以通过旋转，保证有相邻两组亮着灯的奇偶性不同，从而不可能将所有灯熄灭。

 