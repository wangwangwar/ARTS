# 第三周打卡

## Algorithm

LeetCode 547. 朋友圈

https://leetcode-cn.com/submissions/detail/77478218/

# Review

[Container technologies at Coinbase](https://blog.coinbase.com/container-technologies-at-coinbase-d4ae118dcb6c)

1. 前容器时代，单体应用，large operation team
2. 容器时代，分布式应用，容器天然地让你思考水平扩展而不是垂直扩展。
3. 容器编排平台解决了什么问题：部署，水平扩展，自愈。
4. 我们的容器编排平台用了什么：容器编排：Odin + AWS ASGs；处理密钥和配置：动态配置中心；服务发现和负载均衡：Route53 (DNS), ALBs (Application Load Balancers), gRPC客户端本地负载均衡
5. 为什么不用 k8s：k8s没有解决任何客户问题，反而制造一堆新问题：a. 需要全新建设一支全职运维团队  b. 让k8s保持安全并不容易 c. k8s管理平台（EKS on AWS, GKE on Google）才起步，并没有解决运行k8s中的各种挑战。d. 集群升级和管理比我们现在要更关注操作。e.目前还没有迫切需求
6. 未来会用 k8s 吗？如果未来需要相关use case我们会首先考虑是否能通过扩展现有系统来解决，当无法解决时会考虑其他的选项，不仅是k8s
7. 我们讨厌k8s吗，k8s作为一个容器平台是失败的吗？不，k8s除了使用上有一些挑战之外都很好。


# Tips

Android Root工具：

1. 打开开发者选项，打开 USB 调试和 OEM 解锁选项。
2. 用 adb reboot bootloader 命令重启进入 bootloader 菜单。
3. 在adb输入 fastboot oem unlock 解锁 bootloader，即允许安装任何OS。同时手机用户数据被清零。
4. 刷 TWRP。我的一加8pro目前还没有官方的 TWRP 镜像，用的第三方编译的。使用脚本。
5. 安装 Magisk。刷完并重启进入 recovery 模式，即我们刚刷的 TWRP，自带了 Root 命令，执行完即安装了 Magisk 工具。此工具为台湾大佬 John Wu 开发维护，支持 Android 4.2 - 10。root方式是 Syatemless 的，比之前的 xposed 侵入系统分区的方式更无痛。
6. 安装 EdXposed 框架，即 systemless xposed。
7. 安装 XDA 等脚本下载 app

# Share

[Consume less, create more](https://tjcx.me/posts/consumption-distraction/)
与其被动地接受别人推给你的内容，不如每天一点一点地创作自己的内容。
