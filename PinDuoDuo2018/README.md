拼多多2018内推编程题
----
#### 1.最大乘积
* 题目：<br>
给定一个无序数组，包含正数、负数和0，要求从中找出3个数的乘积，使得乘积最大，要求时间复杂度：O(n)，空间复杂度：O(1) 。
* 思路：遍历数组，找到五个数值，分别为最小值，次小值，最大值，次大值，第三大值。因为三个数的乘积最大有两种情况，两负一正或三正。
* 注意：题目描述有错误，输入应该包含元素的个数，题目并没有指出。元素应声明为long long型，否则不能AC。五个值的初始化应该为极大值和极小值更为合理，但是并不能AC，所以全部初始化为1，其实并不合理。
* [代码](https://github.com/Tramac/NewCoder/blob/master/PinDuoDuo2018/maxMultiply.cpp)