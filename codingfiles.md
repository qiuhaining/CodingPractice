# EASY

个人认为middle和hard级别的题目可以拆解成若干个easy的题，因此，数量掌握easy和基础知识点对coding的深入化非常有益！

C++Background参考：[C++ STL](http://c.biancheng.net/view/413.html) 《C++ Primer Plus》

数据结构与算法参考：《算法》第四版

coding参考：《剑指offer》第2版

### July

| Category           | Date | python&&C++                                                  |
| ------------------ | ---- | ------------------------------------------------------------ |
| singly-linked list | 7.1  | [链表相交](https://leetcode-cn.com/problems/intersection-of-two-linked-lists-lcci/) |
|                    | 7.2  | [返回倒数第k个节点](https://leetcode-cn.com/problems/kth-node-from-end-of-list-lcci/) |
|                    | 7.3  | [删除链表中的节点](https://leetcode-cn.com/problems/delete-node-in-a-linked-list/) |
|                    | 7.4  | [回文链表](https://leetcode-cn.com/problems/palindrome-linked-list-lcci/) |
|                    | 7.5  | [删除排序链表中的重复元素](https://leetcode-cn.com/problems/remove-duplicates-from-sorted-list/) |
|                    | 7.6  | [合并两个有序链表](https://leetcode-cn.com/problems/merge-two-sorted-lists/) |
|                    | 7.7  | [相交链表](https://leetcode-cn.com/problems/intersection-of-two-linked-lists/) |
|                    | 7.8  | [二进制链表转整数](https://leetcode-cn.com/problems/convert-binary-number-in-a-linked-list-to-integer/) |
|                    | 7.9  | [反转链表](https://leetcode-cn.com/problems/fan-zhuan-lian-biao-lcof/) |
|                    | 7.10 | [移除重复节点](https://leetcode-cn.com/problems/remove-duplicate-node-lcci/) |
|                    | 7.11 | [链表的重复节点](https://leetcode-cn.com/problems/middle-of-the-linked-list/) |
|                    | 7.12 | [移出链表元素](https://leetcode-cn.com/problems/remove-linked-list-elements/) |
|                    | 7.13 | [删除链表节点](https://leetcode-cn.com/problems/shan-chu-lian-biao-de-jie-dian-lcof/) |
|                    | 7.14 | [环形链表](https://leetcode-cn.com/problems/linked-list-cycle/) |
|                    | 7.15 | [链表中倒数第k个节点](https://leetcode-cn.com/problems/lian-biao-zhong-dao-shu-di-kge-jie-dian-lcof/) |

***<u>singly-linked list</u>***: 总体思路是**旅行家理论**：将链表比作旅行，该过程由起始点，路和旅行者组成，链表的头结点相当于起始点，每个节点相当于驿站，节点的next表示下一个旅行方向，旅行前会从起始点派出一位旅行家，该过程可由h = head表示；旅行家的旅行方向由next表示，即 h.next=newh；更新旅行家的位置则由h = h.next表示! 旅行家的终点是None或者在旅行中转圈圈！问题点关键是根据有限条件确定找到旅行方向，即对h.next如何赋值！

注意点是1、边界条件，否则容易出现死循环或者None.next的问题！

​               2、根据题目判断返回的是旅行家的位置还是整个旅行过程，旅行过程可用起始点指代！

技巧：哨兵(Sentinel)，可用于伪头

​			哨兵节点广泛应用于树和链表中，如伪头、伪尾、标记等，它们是纯功能的，通常不保存任何数据，     ## 其主要目的是使链表标准化，如使链表永不为空、永不无头、简化插入和删除

| Category | Date | python&&C++                                                  | core code&& tags |
| -------- | ---- | ------------------------------------------------------------ | ---------------- |
| tree     | 7.16 | [检查平衡性](https://leetcode-cn.com/problems/check-balance-lcci/) |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |
|          |      |                                                              |                  |





