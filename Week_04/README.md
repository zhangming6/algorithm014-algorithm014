学习笔记

贪心算法：局部最优值累计得到结果最优。和动态规划区别在于，贪心算法不保存历史记录不能回退，没有回溯。而动态规划保存历史结果 难点在于，从什么点去切入找到局部最优。可能是从前，或者从中间，或者从后向前。

二分法，要先跟面试官讲为什么要用二分法：具有单调性

### 二分法

```
left, right = 0, len(array) - 1
while left <= right:
    mid = (left + right)/2
    if array[mid] == target:
        # find target!
        return result
    elif array[mid] < target:
        left = mid + 1
    else:
        right = mid - 1
```