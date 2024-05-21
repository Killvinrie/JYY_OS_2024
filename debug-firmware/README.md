**调试固件**：课程和互联网上的文档都声称是 Firmware 代码将具有 55 aa Magic Number 磁盘的前 512 字节载入内存。经过一些尝试 (例如修改 Magic Number)，我们确认了这一行为；更进一步地，我们能否调试固件的代码，看看到底是什么指令实现了磁盘到内存的搬运？这就用到了《计算机系统基础》实验中的 Watch Point。

在这里，我们还用到了 init.gdb，它可以帮我们省去每次运行时的重复输入命令，也可以设置 hook (钩子)，每当程序暂停时显示一些我们关心的信息——我们**定制和扩展**了 gdb，使它在调试专属于我们的任务时更加强大。