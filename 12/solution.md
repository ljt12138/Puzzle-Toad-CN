## 解法

我们的证明是构造性的，需对山的拐点个数施归纳法，证明两人总能在最高峰相会。基本情形是平凡的。

假设最高的山峰是 $M$，若有多个则任取一个。首先找到除去两端出发点之外，最低的点 $A$，那么为到达 $A$ 至少有一个人不需要翻越山峰 $M$，不失一般性假设是 Yuki。设 Yuki 为了到达 $A$ 需要越过的最高峰是 $B$。

沿着 $B$ 做水平线，找到最靠近 Rikka 的交点，称为 $C$。

将 $PB$ 段和 $PC$ 段拼起来，将 $B$ 和 $C$ 合并成一个点，构成的新问题正是规模更小的原问题，根据归纳假设 Yuki 可以到达 $B$，同时 Rikka 可以到达 $C$。

![](C:\Users\ljt12138\Desktop\puzzle-toad\12\s1.png)

接下来沿着 $A$ 做平行线，设最靠近 $Q$ 的点为 $D$，将 $DC$ 段做轴对称翻转，并将 $A$ 和 $D$ 点合并成一个点，$B\to A(D)\to C$ 就构成了一个旋转了 $180^{\circ}$ 的规模更小的原问题，根据归纳假设 Yuki 可以到达 $A$，同时 Rikka 可以到达 $D$。*注意，由于 $C$ 点是最靠近 $Q$ 的和  $B$ 的等高点，那么 $DC$ 中不存在高于 $C$ 点的其他点；由于 $B$ 是到达 $A$ 之前的最高峰，因此 $BP$ 段也不存在高于 $B$ 的点。*

![](C:\Users\ljt12138\Desktop\puzzle-toad\12\s2.png)

最后一步非常简单，由于 $A, D$ 正是中间的最低点，$D\to M\to A$ 构成了一个更小的原问题，根据归纳假设他们一定可以相遇。

![](C:\Users\ljt12138\Desktop\puzzle-toad\12\s3.png)

这样便完成了归纳。

另外，http://www.cs.cmu.edu/puzzle/solution12.pdf 给出了一个非常漂亮的非构造性证明。