
来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/flatten-nested-list-iterator/

给你一个嵌套的整数列表 nestedList 。每个元素要么是一个整数，要么是一个列表；该列表的元素也可能是整数或者是其他列表。请你实现一个迭代器将其扁平化，使之能够遍历这个列表中的所有整数。

实现扁平迭代器类 NestedIterator ：

NestedIterator(List<NestedInteger> nestedList) 用嵌套列表 nestedList 初始化迭代器。
int next() 返回嵌套列表的下一个整数。
boolean hasNext() 如果仍然存在待迭代的整数，返回 true ；否则，返回 false 。
你的代码将会用下述伪代码检测：

initialize iterator with nestedList
res = []
while iterator.hasNext()
append iterator.next() to the end of res
return res
如果 res 与预期的扁平化列表匹配，那么你的代码将会被判为正确。

 


输入：
```
nestedList = [[1,1],2,[1,1]]
```
输出：
```
[1,1,2,1,1]
通过重复调用 next 直到 hasNext 返回 false，next 返回的元素的顺序应该是: [1,1,2,1,1]。
```

输入：
```
nestedList = [1,[4,[6]]]
```
输出：
```
[1,4,6]
通过重复调用 next 直到 hasNext 返回 false，next 返回的元素的顺序应该是: [1,4,6]。
```

提示
* 1 <= nestedList.length <= 500
* 嵌套列表中的整数值在范围 [-106, 106] 内

总结：
* 如果要在slice的循环中，删除元素，一定要在for 的判断条件里增加 len > 0,否则最后一次删除会报错