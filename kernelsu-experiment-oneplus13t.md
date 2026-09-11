#KernelSU在OnePlus13T上的实验研究
##实验概述
学习KernelSU LKM根、根检测、SELinux模式和根隐藏理论。

##环境
-设备：OnePlus13T
根解决定方案：KernelSU(LKM)
-测试工具：Su、top、dmesg、LSPosed

##按键操作
1.补丁引导。IMG和闪存KernelSU到引导分区。
2.使用su命令获取根shell，检查进程和系统负载。
3.测试SELinux许可/强制开关。
4.研究根检测方法：检测su二进制，检查内核符号。
5.尝试隐藏根跟踪以进行应用程序环境检测研究。

##结论
1.KernelSU LKM工作在内核级别，不同于Zygisk用户模式根。
2.多根检查扫描`/proc`和内核日志。
3.隐藏根需要修改内核层跟踪，不只是用户空间。

##声明
仅用于个人安全学习。不用于未经授权或非法目的。
