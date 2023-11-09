# --MSI-MPG-Z790-13700K-6800xt-EFI-Hackintosh

# 1. 说明

环境为：
* 1.CPU为13700K。(13代的别的CPU，例如13600K，13700K也完全可以参考)
* 2.显卡为AMD6800XT。
* 3.主板为微星暗黑Z790

需要提前在微星主板BIOS(开机按Delete键可以进入BIOS)执行下面的操作。

*   1.关闭安全启动(SecureBoot)，位置在"Settings"-"安全"-"安全引导"-"安全启动"，关闭。
*   2.关闭CFG Lock，位置在"OC"-"CPU特征"-"CFG锁定"，关闭。
*   3.关闭快速启动，位置在"Settings"-"启动"-"快速启动"，关闭。

## 问题记录
1.  安装Mac os 时创建安装盘失败（抹盘失败-西部数据SN850硬盘）：
    （1）当 ESP 分区为 300 MB 时抹盘失败（创建 afps 分区和日志格式失败）
    （2）当 ESP 分区为 400 MB 时创建 afps 时抹盘失败，创建日志格式成功后再抹成 afps 即可
6.  hidpi 可以用 better display（docs 有教程） 来创建分辨率 可以用 RDM 来控制或切换 dpi;
7.  VideoProc Converter 可以看显卡相关
8.  stats 软件可以监控
9.  蓝牙配置半天（更换不同版本的 kexts 时可以 clear nvram 一下）其实就可以了，更新 OC 版本同理

## 总结
除了安装遇到硬盘无法抹盘和蓝牙无法打开（更新 kexts 后 clear nvram）其余基本都挺顺利的。安装日期为6月份版本 Mac OS ventura 13.4 (22F66)，本人没啥技术含量有问题多换换 efi 再试试、分享出来只为你能亮机 加油

> https://github.com/wanna280/HackintoshUEFI-MSI-Z790I-Edge 参考（抄袭）
> https://github.com/xtvj/Gigabyte-Z790-Aorus-Elite-AX-13700K-OpenCore-Hackintosh 参考（小抄）
