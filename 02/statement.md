 ## Puzzle 2: THE LIGHTS OF THE ROUND TABLE

Rikka 和 Yuki 在玩游戏。有一个圆形的桌子，$n$ 个台灯依次摆放在圆周上，编号为 $0$ 到 $n-1$，Yuki 首先选择一些灯打开。每一轮游戏如下：

- Rikka 选择一些编号 $a_1, a_2, \dots, a_n$
- Yuki 选择一个数 $x$，改变所有编号为 $(a_i + x)\bmod n$ 的台灯的状态。换言之，亮着的关掉，关着的打开。

那么，在什么情况下，Rikka 可以确保用有限次将所有台灯关闭？