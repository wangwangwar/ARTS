# 第一周打卡

## 1. Algorithm

LeetCode 554. 砖墙
https://leetcode-cn.com/submissions/detail/72767949/

## 2. Review

#### 文章

[Learning From Sudoku Solvers](http://ravimohan.blogspot.com/2007/04/learning-from-sudoku-solvers.html)

#### 阅读点评

背景简介：极限编程创始人 Ron Jeffries 写了 5 篇博客，记录自己实践用 TDD 方法做一个数独解算器（Sudoku Solver）。到最后做了一个半成品后放弃。另一方面计算机科学家 Peter Norvig 也写了一篇博客，完美解决数独问题且效率很高。
网络有人把两者做对比，探讨了很多问题：
1. 自底向上 vs 自顶向下
Norvig 的方法偏向于自顶向下，即先找到了整体解决方法，再动手写细节;而 Jeffries 偏向于从实现一个个小 case 开始，自底向上构建程序。

2. TDD vs. Old-fashioned engineering
进一步来说，是 TDD 和传统软件工程的对比。TDD 号称是先进的软件开发方法， 为什么具体效果还不如传统软件工程？

3. Software engineering vs. Algorithm
本文作者指出，Jeffries 博客展示的就是当一个程序员面对自己不知道怎么解决的问题时，应用 TDD 尝试解决时的表现。所以在文章 [Discussions about TDD always make me think of Ron Jeffries' attempt to develop a sudoku-solver using TDD.](https://news.ycombinator.com/item?id=3033446) 里说到一点我很赞同：
    > "Old-fashioned engineering vs. TDD" is misleading. The difference is that Norvig knew in advance how to solve the problem - constraint propagation - while Jeffries presumably did not.

    我总结是，软件开发两块大的方面，一个是算法，这个关注如何定义问题和给出问题的解;另一个是工程方法，是自顶向下还是自底向上，是TDD还是BDD。对于简单一点的问题，一来就上手实现，比如TDD推崇的，当然可以，因为一开始你就知道怎么解决这个问题;但是对于那些你不知道怎么解决的问题，先停下来思考如何定义这个问题，用什么样的算法，时间和空间复杂度如何，先思考清楚这些是最重要的。 
    想到一个比喻，用 TDD 来解决你不知道怎么解决的问题时，就像盲人摸象，一开始你写了几个 case 并通过了（摸到象腿），后来又增加了几个 case 也通过了（摸到象耳朵），然后又增加了几个 case 还是通过了（摸到象鼻），最后发现写出的程序并不能解决问题（没有见过完整的大象）。

## 3. Tip

默认 Linux 的文件会有 3 个时间：创建时间 ctime，修改时间 mtime，访问时间 atime。初衷是很好的，3 个时间各司其责。但是 atime 访问时间实际上比较低效，原因时读取文件本来只是读操作（随机+顺序），但是每次读完要更新 atime 的话，就会增加一个写操作（随机）。

1. 所以 Linux 提供了 mount 选项： noatime 和 nodireatime。前者指不记录文件访问时间，后者指不记录文件夹访问时间。noatime 已经包含 nodiratime，所以使用时只需要用 noatime。

```bash
# /etc/fstab
/dev/sdb1 /home/disk0 ext4 notime 0 2
```

2. relatime。

3. lazytime。Linux kernel 4.0 出来的选项，配合 *atime 一起使用。

具体可以参考 https://wiki.archlinux.org/index.php/Fstab

## 4. Share

https://www.onivim.io

结合了 Vim 和 VSCode 的编辑器。
1. 结合程度比 VSCode + Vim 插件要好。
2. 支持 Mac，Windows 和 Linux (Ubuntu 16.04+, CentOS 7+, Manjaro), 但是在我的 Arch Linux 上使用还有问题。
3. 支持 VSCode 插件。
4. 使用 ReasonML 开发。