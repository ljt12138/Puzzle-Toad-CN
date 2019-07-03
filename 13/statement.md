##   Puzzle 13: The Voting Problem 

给定函数 $f:\{A,B,C\}^n\to\{A,B,C\}$，满足：

-  如果对于任意的 $i$ 均有 $x_i\ne y_i$，那么 $f(x_1, x_2, \dots, x_n)\ne f(y_1, y_2, \dots, y_n)$

**证明或推翻：**一定存在某个 $1\le i\le n$ 和函数 $h:\{A, B, C\}\to \{A, B, C\}$，使得
$$
f(x_1, x_2, \dots, x_n) = h(x_i)
$$
