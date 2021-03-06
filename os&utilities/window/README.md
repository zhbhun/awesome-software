# Window

- http://msdn.itellyou.cn/
- [Download virtual machines](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/)

    - [3分钟快装Windows虚拟机特供版(附Windows通用激活工具)](https://www.jianshu.com/p/af0db8b231b0)

## 开发环境

- [Build with Windows](https://docs.microsoft.com/en-us/windows/dev-environment/)

## 录屏/截屏

- [FastStone](http://www.faststone.org/index.htm)
- [LICEcap](https://github.com/justinfrankel/licecap)
- [ScreenToGif](https://github.com/NickeManarin/ScreenToGif)

## 系统工具

- [microsoft/PowerToys](https://github.com/microsoft/PowerToys)

    [微软 PowerToys 小工具合集 - 免费给 Win10 加装各种增强新功能的效率利器](https://www.iplaysoft.com/powertoys.html)

## 常见问题

### Win10 升级专业版

[Win10家庭版如何升级到win10专业版](https://www.zhihu.com/question/37424608)

### 怎么关闭文件共享

在 Windows 系统的默认配置下，会启动一个共享服务（Samba, SMB），以使局域网内的机器可以通过如 \\192.168.1.1 的形式来访问系统中共享的文件和打印机等。该服务主要使用 445 端口进行通信，我们可以通过命令 netstat -an | findstr :445 来确认该端口被占用。如果无需使用该服务，或者想要释放 445 端口供其他应用使用的话，我们可以禁用 Windows 共享服务 —— Server（LanmanServer）和 Computer Browser（Browser）。

```cmd
sc.exe config Browser start= disabled
sc.exe stop Browser

sc.exe config LanmanServer start= disabled
sc.exe stop LanmanServer
```

要使 Windows 释放 445 端口，除了停止服务，我们还需要重启一次计算机。

- [禁用 Windows 共享服务，释放 445 端口](https://zzz.buzz/zh/2016/08/10/disable-windows-server-service-to-release-port-445/)
- [windows如何关闭默认共享和共享服务 windows7关闭网络共享的方法]( https://www.jb51.net/os/windows/576213.html )
- [外网文件共享445端口被封解决办法](https://blog.csdn.net/magaiou/article/details/91845324)

### 怎么读写 ext 文件系统

-  http://www.ext2fsd.com/ 
- [Windows系统读写ext2/3/4文件系统的工具「ext2fsd」](https://blog.csdn.net/cruise_h/article/details/12894135)
- [如何在Windows系统中访问Linux分区的文件？](https://www.zhihu.com/question/21281805)
- [windows 为何迟迟不肯支持 ext 格式？]( https://www.v2ex.com/t/178598 )

### 怎么打开  VHD  文件

- [如何打开vhd文件？](https://answers.microsoft.com/zh-hans/windows/forum/windows_8-files/%e5%a6%82%e4%bd%95%e6%89%93%e5%bc%80vhd%e6%96%87/df7fbf1b-3a1b-43d9-85c2-88fb689e0fea?messageId=90425f51-e432-49da-8a79-28c54c6377c0)

### 怎么设置开机启动程序

- [如何让应用程序在计算机开机后延迟启动？](https://blog.csdn.net/lordwish/article/details/51742585)
- [win10怎样把应用程序加入开机启动项](https://jingyan.baidu.com/article/90895e0ff3a41f64ec6b0bc3.html)

---

- http://msdn.itellyou.cn/

---
