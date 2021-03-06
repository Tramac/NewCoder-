京东2017编程题
----
#### 1.保卫方案
* 题目:<br>
战争游戏的至关重要环节就要到来了，这次的结果将决定王国的生死存亡，小B负责首都的防卫工作。首都位于一个四面环山的盆地中，周围的n个小山构成一个环，作为预警措施，小B计划在每个小山上设置一个观察哨，日夜不停的瞭望周围发生的情况。 一旦发生外地入侵事件，山顶上的岗哨将点燃烽烟，若两个岗哨所在的山峰之间没有更高的山峰遮挡且两者之间有相连通路，则岗哨可以观察到另一个山峰上的烽烟是否点燃。由于小山处于环上，任意两个小山之间存在两个不同的连接通路。满足上述不遮挡的条件下，一座山峰上岗哨点燃的烽烟至少可以通过一条通路被另一端观察到。对于任意相邻的岗哨，一端的岗哨一定可以发现一端点燃的烽烟。 小B设计的这种保卫方案的一个重要特性是能够观测到对方烽烟的岗哨对的数量，她希望你能够帮她解决这个问题。<br>
* 输入描述:<br>
输入中有多组测试数据，每一组测试数据的第一行为一个整数n(3<=n<=10^6),为首都周围的小山数量，第二行为n个整数，依次表示为小山的高度h（1<=h<=10^9）.<br>
* 输出描述:<br>
对每组测试数据，在单独的一行中输出能相互观察到的岗哨的对数。<br>
* 我的思路：<br>
暴力枚举所有的岗哨对，然后两边判断，只要有一个方向满足就可以。复杂度过高，卡在了90%。这个方法是真的麻烦。<br>
* [我的代码](https://github.com/Tramac/NewCoder/blob/master/JingDong2017/SecurityPlan.cpp)
#### 2.进制均值
* 题目:<br>
尽管是一个CS专业的学生，小B的数学基础很好并对数值计算有着特别的兴趣，喜欢用计算机程序来解决数学问题，现在，她正在玩一个数值变换的游戏。她发现计算机中经常用不同的进制表示一个数，如十进制数123表达为16进制时只包含两位数7、11（B），用八进制表示为三位数1、7、3，按不同进制表达时，各个位数的和也不同，如上述例子中十六进制和八进制中各位数的和分别是18和11,。 小B感兴趣的是，一个数A如果按2到A-1进制表达时，各个位数之和的均值是多少？她希望你能帮她解决这个问题？ 所有的计算均基于十进制进行，结果也用十进制表示为不可约简的分数形式。 <br>
* 输入描述:<br>
输入中有多组测试数据，每组测试数据为一个整数A(1 ≤ A ≤ 5000).<br>
* 输出描述:<br>
对每组测试数据，在单独的行中以X/Y的形式输出结果。<br>
* 我的思路：<br>
实现方法还是很麻烦的，都是最基本的思路，没有找到快捷的方法，但是测试全部通过。本体的关键就是如何求出数值value用base进制表示时的各个位的和，用递归的方法实现。另外一个需要注意的地方是，输出时可以约分时要约分，这就涉及到如何约分，我是先寻找公约数，其中寻找公约数的方法也是递归，要记住，以后可能经常用到。<br>
* [我的代码](https://github.com/Tramac/NewCoder/blob/master/JingDong2017/SystemMean.cpp)
#### 3.幸运数
* 题目:<br>
小明同学学习了不同的进制之后，拿起了一些数字做起了游戏。小明同学知道，在日常生活中我们最常用的是十进制数，而在计算机中，二进制数也很常用。现在对于一个数字x，小明同学定义出了两个函数f(x)和g(x)。 f(x)表示把x这个数用十进制写出后各个数位上的数字之和。如f(123)=1+2+3=6。 g(x)表示把x这个数用二进制写出后各个数位上的数字之和。如123的二进制表示为1111011，那么，g(123)=1+1+1+1+0+1+1=6。 小明同学发现对于一些正整数x满足f(x)=g(x)，他把这种数称为幸运数，现在他想知道，小于等于n的幸运数有多少个？ <br>
* 输入描述:<br>
每组数据输入一个数n(n<=100000)<br>
* 输出描述:<br>
每组数据输出一行，小于等于n的幸运数个数。<br>
* 我的思路：<br>
其实主要还是求其它进制各个数位上数字之和的问题，和上一道题有些类似。<br>
* [我的代码](https://github.com/Tramac/NewCoder/blob/master/JingDong2017/LuckyNumber.cpp)
#### 4.集合
* 题目: <br>
给你两个集合，要求{A} + {B}。 注：同一个集合中不会有两个相同的元素。 
* 输入描述:<br>
每组输入数据分为三行,第一行有两个数字n,m(0 ≤ n,m ≤ 10000)，分别表示集合A和集合B的元素个数。后两行分别表示集合A和集合B。每个元素为不超过int范围的整数,每个元素之间有个空格隔开。<br>
* 输出描述:<br>
针对每组数据输出一行数据，表示合并后的集合，要求从小到大输出，每个元素之间有一个空格隔开,行末无空格。
* 我的思路:<br>
我的思路真的是太普通了，而且超内存了，只让过20%。基本的数组操作还是要多多联系啊。首先建立两个数组来保存两行输入，然后分别对两个数组排序，对两个数组依次遍历，如果和前一个输出的元素不相同就输入较小的数字，然后递归调用。好多这样的题，只会这样最简单最笨的思路，唉。
* [我的代码](https://github.com/Tramac/NewCoder/blob/master/JingDong2017/MergeSet.cpp)
* 更新<br>
新增通过的python代码和c++代码，python代码是真的简洁，本来自己也是主要用python的，可是为什么不能灵活运用呢。<br>
