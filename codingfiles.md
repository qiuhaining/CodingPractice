# CodingPractice

从2020年2到4月5号，一直在尝试coding练习，探索coding的方法并内化为自身的技能！经过近两个月的尝试后发现，简单的编写或参考别人答案再自己编写的方法虽然能完成相关coding的题目，但内化率很低，难以在下一个问题中有效的运用学习到的知识！究其原因认为，其一是C++基础知识薄弱，STL的相关知识不扎实，难以对其进行主动应用！其二是coding技巧不熟练，即便是知晓其背后的数据结构，算法和考察点，但依然不能高效的解决！因此，为了避免题海战术以及督促自己每天的coding练习，这里进行了coding中多种解法的记录和总结，总结内容不仅包括每种解法的代码，还包括他人的详细的解释以及需要注意的detail和背后的C++，数据结构与算法的知识，希望做到一个萝卜一个坑和知识和技巧的融汇贯通！

C++Background参考：[C++ STL](http://c.biancheng.net/view/413.html) 《C++ Primer Plus》

数据结构与算法参考：《算法》第四版

coding参考：《剑指offer》第2版

## 2020——primary

### Apr

| Date  | Link                                                         | Tag                                       | Analysis                                                     | Code Link                                                    | Detail                                                       | Background                                                   |
| ----- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 4.5   | [数值的整数次方](https://leetcode-cn.com/problems/shu-zhi-de-zheng-shu-ci-fang-lcof/) | bit op，recursion，dichotomy              | [Reference](https://leetcode-cn.com/problems/shu-zhi-de-zheng-shu-ci-fang-lcof/solution/mian-shi-ti-16-shu-zhi-de-zheng-shu-ci-fang-kuai-s/) | [No.1](https://leetcode-cn.com/submissions/detail/59766296/) | 快速幂注意点：1. 底数为0时，指数不能为负数；2.指数为负数时，底数需要取倒数；因此，该coding不严谨，测试实例不完整！ |                                                              |
|       |                                                              |                                           |                                                              | [No.2](https://leetcode-cn.com/submissions/detail/59860906/) | 该方法很严谨！注意点：1、两个double类型的变量不能直接使用“==”，来判断是否相等；2、带符号的int型，最小值的绝对值大于最大值，因此，当n为最小值时，不能简单使用-n来取绝对值，会溢出，该code是将最小值改写成2*(MIN/2)的形式！ | 1、double型变量判断相等    2、int型范围有界，最小值的绝对值大于最大值 |
|       |                                                              |                                           |                                                              | [No.3](https://leetcode-cn.com/submissions/detail/59860122/) | 为了避免上述问题，这里是将int型的变量赋值给了范围更大的带符号的long型！ |                                                              |
|       |                                                              |                                           |                                                              | [No.4](https://leetcode-cn.com/problems/shu-zhi-de-zheng-shu-ci-fang-lcof/solution/ckuai-su-mi-mo-ban-ti-dai-ma-jian-duan-luo-ji-qing/) | 和上述三种方法不一样的是，这里没有用到递归而是迭代的方法！没有用到n>>1来表示除以2，因为n==-1时，n>>1依然是-1，负数在计算机中是使用补码的形式存放，-1为11111111，右移一位依然是11111111！ | 1、n>>1与n/2的区别                                           |
| 4.6   | [打印从1到最大的n位数](https://leetcode-cn.com/problems/da-yin-cong-1dao-zui-da-de-nwei-shu-lcof/) | recursion；大数问题                       | [reference](https://leetcode-cn.com/problems/da-yin-cong-1dao-zui-da-de-nwei-shu-lcof/solution/c-3chong-jie-fa-by-xdb/) | [No.1](https://leetcode-cn.com/submissions/detail/59785872/) | 该方法不严谨，未考虑大数问题，即超出int，long，甚至longlong的情况！本题测试样例不够！ | pow(10,n)表示10的n次方！                                     |
|       |                                                              |                                           |                                                              | [No.2](https://leetcode-cn.com/submissions/detail/60354576/) | 使用char解决大数问题                                         | **memset(number, '0',   n)**：对number所在的 内存       空间设置同一个初始值！                      **strlen(number)**：用来     计算指定字符串 str 的长度，但不包括结束字符               （即 null 字符）                                **char *number=new char[n+1]** 使用**new**为字符数组开辟空间；           **delete []number;** 清除内存                                         **int num = stoi(s);** 将字符串转成整型 |
|       |                                                              |                                           |                                                              | [No.3](https://leetcode-cn.com/submissions/detail/60356874/) | 使用string表示大数                                           | **string** 构造函数：**string number(n, '0');**构造string的迭代器：**string::iterator it = number.begin();** 该迭代器表示string的第一个元素！it++;进行后续迭代； 如果想在函数中修改实参，需要哦那个到引用传递：**bool Increment(string& number)** |
|       |                                                              |                                           |                                                              | [No.4](https://leetcode-cn.com/submissions/detail/60378387/) | 使用递归实现全排列                                           | 利用递归实现全排列，每当排列完最后一位结束之后才打印!        |
| 4.11* | [正则表达式匹配](https://leetcode-cn.com/problems/regular-expression-matching/) | backtrack；recursion；dynamic programming | [reference](https://leetcode-cn.com/problems/zheng-ze-biao-da-shi-pi-pei-lcof/solution/hui-su-fa-dong-tai-gui-hua-by-luo-jing-yu-yu/) | [No.1](https://leetcode-cn.com/submissions/detail/61836576/) | 递归实现回溯；  **Hard 需要回顾**                            | string 类中，1. 形式：s.substr(pos, n)                        2、解释：返回一个string，包含s中从pos开始的n个字符的拷贝（pos的默认值是0，n的默认值是s.size() - pos，即不加参数会默认拷贝整个s） |

 

