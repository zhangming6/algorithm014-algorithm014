学习笔记

动态规划的核心问题就是穷举。因为穷举存在重叠子问题，所以写出正确【状态转移方程】的穷举，就是动态规划的意义所在。

动态规划一般采用自底向上的方式，这种方式一般就脱离了递归，采用循环迭代方式实现。

dp的大致模板如下：

```
# 初始化 base case
dp[0][0][...] = base
# 进行状态转移
for 状态1 in 状态1的所有取值：
    for 状态2 in 状态2的所有取值：
        for ...
            dp[状态1][状态2][...] = 求最值(选择1，选择2...)
```

