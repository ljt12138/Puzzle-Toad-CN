## 解答

#### 问题1

注意到两个蚂蚁相遇可以视作他们“穿过”对方，那么最坏情况就是一只蚂蚁从木棍的一端爬到另外一端，这需要经过 $1~min$。

#### 问题2

仍然将两个蚂蚁相遇视作他们穿过对方，不失一般性假设 Alice 逆时针运动，Alice 编为 0 号，按照逆时针将所有蚂蚁依次编号。那么 Alice 所对应的这个“虚拟 Alice”从起始位置出发逆时针运动一周，经过 $1~min$ 回到起始位置。要想让 Alice 也回到起始位置，需让这只“虚拟 Alice”恰好对应 Alice。

注意到所有蚂蚁的相对位置不会改变，那么“虚拟 Alice”和其他虚拟蚂蚁每一次碰撞，”虚拟 Alice“对应的蚂蚁编号就会 $+1$，而一只顺时针运动的虚拟蚂蚁恰好会贡献两次碰撞。那么，要想让”虚拟 Alice“最终对应 Alice，要么不存在顺时针运动的蚂蚁，要么恰好有 $n/2$ 只顺时针运动的蚂蚁，换言之概率就是： 
$$
\frac{2+2\times[n\bmod 2=0]{n-1\choose n/2}}{2^n}=\frac{1}{2^{n-1}}+[n\bmod 2=0]\frac{{n\choose n/2}}{2^n}
$$

#### 问题3

继续沿用上一问的思想，不妨设 Alice 向左运动。那么当左边不存在向右运动的蚂蚁时，任何蚂蚁都不会传染感冒；当左边存在一只向右运动的蚂蚁时，左边向右运动的蚂蚁和右边向左运动的蚂蚁，都会被传染感冒。那么期望患感冒的蚂蚁数量就是
$$
\sum_{1\le k \le n} \frac {n\choose k} {2^n}\sum_{1\le j\le n}\sum_{0\le l\le n-k}\frac{{k\choose j}}{2^k} \frac{{n-k\choose l}}{2^{n-k}}(j+l)=n\left(\frac{1}{2}-\frac{3^{n-1}}{4^n}\right)
$$
