
来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/move-zeroes/

给定一个数组 nums，编写一个函数将所有 0 移动到数组的末尾，同时保持非零元素的相对顺序。

输入：
```
[0,1,0,3,12]
```
输出：
```
[1,3,12,0,0]
```


提示：
    

* 必须在原数组上操作，不能拷贝额外的数组。
* 尽量减少操作次数。


总结：
* golang 可以不用 tmp 实现变量互换
* greatest common divisor gcd 最大公约数
* Smallest Common Multiple scm 最小公倍数