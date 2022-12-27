import Image from 'next/image';

## 1. 介绍
**散列表(Hash table，也叫哈希表)**，是根据键值(Key value)而直接进行访问的数据结构。也就是说，它通过把键值映射到表中一个位置来访问记录，以加快查找的速度。

## 2. 原理

哈希表有多种不同的实现方法，下面是最常用的一种方法——拉链法，我们可以理解为“链表的数组”，如图：

<Image src="/data-structure-and-algorithm/07-hash-table.png" alt="hash-table" width={720} height={720} />

左边很明显是个数组，数组的每个成员包括一个指针，指向一个链表的头，当然这个链表可能为空，也可能元素很多。我们根据元素的一些特征把元素分配到不同的链表中去，也是根据这些特征，找到正确的链表，再从链表中找出这个元素。