# 黑苹果

- https://www.tonymacx86.com
- [Hackintosh-Installer-University](https://github.com/huangyz0918/Hackintosh-Installer-University)
- [daliansky/Hackintosh](https://github.com/daliansky/Hackintosh) - Hackintosh long-term maintenance model EFI and installation tutorial.
- [黑苹果乐园](https://imac.hk)
- [黑苹果社区](https://osx.cx)

## 教程

- [Hackintosh从入门到精通](https://www.yuque.com/tangjiaqiang/hackintosh)

## VMWare Hackintosh

几种方式

1. 使用别人提供的 VMDK 文件，创建好 VMWare MacOS 虚拟机后，直接替换 VMDK 就可以安装运行
2. 制作可引导的 CDR 或 ISO 镜像，创建好 VMWare MacOS 虚拟机后，设置虚拟光驱执行可引导镜像，然后启动安装运行
3. 制作可引导的 U 盘，创建好 VMWare MacOS 虚拟机后，以物理磁盘的方式添加 U 盘，然后启动安装运行

参考文献

- [How to install macOS Mojave on VMware Workstation](https://www.aioboot.com/en/macos-vmware-workstation/#VMware-macOS-Unlocker) / https://www.youtube.com/watch?v=cX4FavnzhtY / https://www.youtube.com/watch?v=JkOFf68EeZU
- [Install macOS 10.15 catalina in VMware on Windows](https://hackintoshpro.com/install-macos-10-15-catalina-in-vmware-on-windows/)
- [VMware Pro 15安装macOS 10.14 Mojave](https://www.yuque.com/tangjiaqiang/hackintosh/ew0qmr?language=en-us#74dd31a6)
- [VMWare14 安装Mac OS系统](https://www.lovyou.top/post/51.html)
- [Mac装在真机上和虚拟机上性能有很大差别吗？](https://www.zhihu.com/question/24693842)
- [Install macOS 10.15 catalina in VMware on Windows](https://hackintoshpro.com/install-macos-10-15-catalina-in-vmware-on-windows/)
- [在普通PC 电脑上使用VMware虚拟机安装苹果 macOS系统](https://www.applex.net/threads/pc-vmware-macos.92998/)
- [黑苹果从入门到精通 篇一：可能是世界上最详细的VMware安装macOS教程](https://post.smzdm.com/p/ax08lz74/)

### 常见问题

#### unlocker 下载 VMWare 文件失败

- [填坑黑苹果(VMware装MacOS) - 修改 Unlocker 补丁源码版](https://zhuanlan.zhihu.com/p/83470329)
- [paolo-projects/unlocker](https://github.com/paolo-projects/unlocker)

#### MacOS 已经损坏

1. 关闭网络
2. 打开终端，修改时间

    ```
    date 0201010116
    ```

3. 再次安装

参考文献

- [安装Mac OS X，提示:应用程序副本不能验证 它在下载过程中可能已遭破坏或篡改](https://www.applex.net/threads/mac-os-x.57768/)
- [黑苹果 安装系统出现"安装 macOS xxx"应用程序副本已损坏，不能用来安装macOS解决方法](https://blog.csdn.net/qq_41855420/article/details/102762647)

#### 如何安装 VMWare Tools

在 unlocker 下载的工具 tools/com.vmware.fusion.zip.tar/com.vmware.fusion.zip.tar/com.vmware.fusion.zip/payload/VMware Fusion.app/Contents/Library/isoimages/ 里面。

- [VMware虚拟机安装Mac OS X后怎么安装VMware Tools?](https://www.lovyou.top/post/52.html)
- [VMware Tools for OS X / macOS (darwin.iso and darwinPre15.iso) 11.5.0](https://www.insanelymac.com/forum/files/file/987-vmware-tools-for-os-x-macos-darwiniso-and-darwinpre15iso/)

#### 调整分辨率

1. 设置 Mac 分辨率

    - 1920*1080 分辨率：

        ```bash
        $ sudo nvram AC20C489-DD86-4E99-992C-B7C742C1DDA9:width=%80%07%00%00
        $ sudo nvram AC20C489-DD86-4E99-992C-B7C742C1DDA9:height=%38%04%00%00
        ```

    - 3840*2160 分辨率：

        ```bash
        $ sudo nvram AC20C489-DD86-4E99-992C-B7C742C1DDA9:width=%00%0F%00%00
        $ sudo nvram AC20C489-DD86-4E99-992C-B7C742C1DDA9:height=%70%08%00%00
        ```

	- 1536*864 分辨率

        ```bash
        $ sudo nvram AC20C489-DD86-4E99-992C-B7C742C1DDA9:width=%00%06%00%00
        $ sudo nvram AC20C489-DD86-4E99-992C-B7C742C1DDA9:height=%60%03%00%00
        ```

2. 修改 VMWare 虚拟机的 vmx 文件（设置一下最大分辨率）

    ```
    svga.autodetect = "FALSE"
    svga.maxWidth = "3840"
    svga.maxHeight = "2160"
    ```

3. 安装 vmtools，然后重启虚拟机

参考文献

- [VMware15 安装 mac OS 10.14 分辨率调整为1920*1080？本文来自：Dkukoc，原地址：https://www.dkukoc.com/post/226.html](https://www.dkukoc.com/post/226.html)
- [VMware 如何在 Mac OS X 虚拟机中更改屏幕分辨率？](https://www.zhihu.com/question/68703160)

#### 提升显卡内存

- [I am running High Sierra on VMWare Workstation. Does anyone know how to increase graphics memory?](https://www.reddit.com/r/hackintosh/comments/8sszhb/i_am_running_high_sierra_on_vmware_workstation/)
- [How to increase graphics memory in Mac OS running as a client in VMware?](https://apple.stackexchange.com/questions/79452/how-to-increase-graphics-memory-in-mac-os-running-as-a-client-in-vmware)
- [Improving Sierra performance in VMWare?](https://www.insanelymac.com/forum/topic/321911-improving-sierra-performance-in-vmware/)

#### 如何制作 CDR/ISO 镜像

ps：Mac 原版镜像是 DMG 格式，不支持直接在 VMWare 安装，需要转成可引导的镜像 CDR 或 ISO。

- [Mac 原版镜像下载地址](https://www.applex.net/pages/macos/)
- [如何制作适用于VMware Fusion安装的macOS Catalina CDR系统镜像？](https://heipg.cn/tutorial/macos-catalina-cdr.html)
- [镜像转换 DMG => ISO (macOS 10.14.6 18G103)](https://leeyr.com/306.html)
- [制作 MacOS cdr/iso 镜像文件](https://www.jianshu.com/p/24212c95fcc1)
- [黑苹果 制作虚拟机CDR镜像（详细的教程，别再翻了！）](https://blog.csdn.net/qq_41855420/article/details/102750055)

## VietualBox Hackintosh

- [How to Install macOS High Sierra in VirtualBox on Windows 10](https://www.howtogeek.com/289594/how-to-install-macos-sierra-in-virtualbox-on-windows-10/)
