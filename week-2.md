# 第二周打卡

## Algorithm

LeetCode 516. 最长回文子序列

https://leetcode-cn.com/submissions/detail/74336040/

## Tips

Tmux 基本操作：

prefix := Ctrl+B

1. session相关操作
    - 查看/切换session	prefix s
    - 离开Session	prefix d
    - 重命名当前Session	prefix $

2. window相关操作 
    - 新建窗口	prefix c
    - 切换到上一个活动的窗口	prefix space
    - 关闭一个窗口	prefix &
    - 使用窗口号切换	prefix 窗口号

3. Pane相关操作
    - 切换到下一个窗格	prefix o
    - 查看所有窗格的编号	prefix q
    - 垂直拆分出一个新窗格	prefix “
    - 水平拆分出一个新窗格	prefix %
    - 暂时把一个窗体放到最大	prefix z
    - 滚动 prefix [

4. 插件
    - Mouse https://github.com/NHDaly/tmux-better-mouse-mode

## Review

[Programming principles from id software](https://blog.usejournal.com/programming-principles-from-id-software-bed83e762210)

ID software 不到10个人的开发团队，在6年时间内快速交付了 28 个游戏。如何做到的？

1. 直接做（并且做好）
    1. 不是做demo，而是直接做游戏。迭代开发。保持高标准，但不过早优化。
2. 让代码永远可运行
    1. 出错时可以fallback
3. 保持简单
    1. KISS
4. 花时间构建好的工具
    1. 效率工具
5. 尽量测试代码
    1. 吃自己的狗粮
    2. 自己找自己的bug
    3. 写尽可能多的测试
6. 尽快修复bug
7. 使用先进的开发系统
8. 只为当前版本写代码，而不是未来
    1. 保持克制，不过早优化
9. 使用好的组件抽象
    1. 封装功能性保证设计的一致性。
10. 编码时从同伴获得反馈
11. 给程序员创造的自由
    1. 结果重要

## Share

[12 Signs You’re Working in a Feature Factory](https://cutle.fish/blog/12-signs-youre-working-in-a-feature-factory)

[12 Signs You’re Working in a Feature Factory — 3 Years Later](https://amplitude.com/blog/12-signs-youre-working-in-a-feature-factory-3-years-later)
