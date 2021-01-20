# 第四周打卡

## Algorithm

LeetCode



## Tips

Android Root工具：

1. 打开开发者选项，打开 USB 调试和 OEM 解锁选项。
2. 用 adb reboot bootloader 命令重启进入 bootloader 菜单。
3. 在adb输入 fastboot oem unlock 解锁 bootloader，即允许安装任何OS。同时手机用户数据被清零。
4. 刷 TWRP。我的一加8pro目前还没有官方的 TWRP 镜像，用的第三方编译的。使用脚本。
5. 安装 Magisk。刷完并重启进入 recovery 模式，即我们刚刷的 TWRP，自带了 Root 命令，执行完即安装了 Magisk 工具。此工具为台湾大佬 John Wu 开发维护，支持 Android 4.2 - 10。root方式是 Syatemless 的，比之前的 xposed 侵入系统分区的方式更无痛。
4. 安装 EdXposed 框架，即 systemless xposed。
5. 安装 XDA 等脚本下载 app



## Review

[Learn Rust With Entirely Too Many Linked Lists]: https://rust-unofficial.github.io/too-many-lists/index.html

### 通过实现 6 种链表，教学以下知识点：
- The following pointer types: `&`, `&mut`, `Box`, `Rc`, `Arc`, `const`, `mut`
- Ownership, borrowing, inherited mutability, interior mutability, Copy
- All The Keywords: struct, enum, fn, pub, impl, use, ...
- Pattern matching, generics, destructors
- Testing
- Basic Unsafe Rust

### 为啥是链表

#### I can't afford amortization 不能忍受分期偿还？

#### Linked lists waste less space 空间浪费更少

#### I use linked lists all the time in <functional language> 
在函数式语言中，链表非常优雅，可以不用改变他们而操作它们（？），可以递归地描述，可以利用惰性实现无穷链表。
可以不用可变状态实现迭代。

#### Linked lists are great for building concurrent data structures! 链表很适合构建并发数据结构

#### Mumble mumble kernel embedded something something intrusive.

#### Iterators don't get invalidated by unrelated insertions/removals （？）

#### They're simple and great for teaching!

### 教学特点
教程以一个初学者使用 Rust 的视角去趟编译器的各种坑（不会直接给你正确答案），并解读这些错误都是什么，背后原理是啥，怎么去改。

## Share
