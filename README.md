 #来自hipda带着爱，具体教程慢慢写，目前我试下来基本完美，除了某些特殊的usb键盘休眠有问题找不到原因，算是99%成品了。
 
 配置：
 
 - 9900es qqz5
 - 华擎B365M itx
 - 科赋16G 2666普条 * 2
 - RX588矿卡
 - wd sn530 1tb
 - 网卡dw1820a
 
#使用opencore引导：

还是刚才那个可以启动的U盘，把EFI文件夹删除，然后把repo里的EFI文件夹拷贝进去；

开机按f12，选择U盘启动，进入boot menu的时候，先选reset nvram清除一下nvram，然后再次u盘启动进入系统看看有没有问题；

确认所有东西都ok以后，使用你喜欢的任何工具挂载硬盘上的EFI分区，然后删除掉原来就有的EFI文件夹（注意备份），然后把U盘里面的EFI文件夹拷贝进去；

重启，硬盘启动，老样子，先清一遍nvram，然后启动；

进系统以后自己用tools里面的hackintool算序列号什么的，然后编辑 EFI分区下的 /EFI/OC/config.plist 文件，在systeminfo里面注入三码啊，序列号啊这些。

enjoy！

#目前支持状态：

- [x] cpu变频

- [x] Rx580 显卡驱动、metal、opencl、硬解

- [x] 上述无线网卡以及蓝牙，handoff，智能热点，airdrop

- [x] 内置声卡，usb声卡

- [x] dp输出4k 60hz，hidpi

- [x] 休眠、唤醒正常

- [x] 内置有线网卡

- [x] 所有usb端口（通过usbports.kext定制）



目前问题：

暂无
