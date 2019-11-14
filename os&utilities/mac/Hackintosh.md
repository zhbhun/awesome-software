# 黑苹果

- https://www.tonymacx86.com
- [Hackintosh-Installer-University](https://github.com/huangyz0918/Hackintosh-Installer-University)
- [daliansky/Hackintosh](https://github.com/daliansky/Hackintosh) - Hackintosh long-term maintenance model EFI and installation tutorial.
- [黑苹果乐园](https://imac.hk)
- [黑苹果社区](https://osx.cx)

## 教程

- [Hackintosh从入门到精通](https://www.yuque.com/tangjiaqiang/hackintosh)

## VMWare

- [How to install macOS Mojave on VMware Workstation](https://www.aioboot.com/en/macos-vmware-workstation/#VMware-macOS-Unlocker) / https://www.youtube.com/watch?v=cX4FavnzhtY / https://www.youtube.com/watch?v=JkOFf68EeZU
- [Install macOS 10.15 catalina in VMware on Windows](https://hackintoshpro.com/install-macos-10-15-catalina-in-vmware-on-windows/)
- [VMware Pro 15安装macOS 10.14 Mojave](https://www.yuque.com/tangjiaqiang/hackintosh/ew0qmr?language=en-us#74dd31a6)
- [VMWare14 安装Mac OS系统](https://www.lovyou.top/post/51.html)
- [Mac装在真机上和虚拟机上性能有很大差别吗？](https://www.zhihu.com/question/24693842)

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

### 如何安装 VMWare Tools

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

### 提升显卡内存

- [I am running High Sierra on VMWare Workstation. Does anyone know how to increase graphics memory?](https://www.reddit.com/r/hackintosh/comments/8sszhb/i_am_running_high_sierra_on_vmware_workstation/)
- [How to increase graphics memory in Mac OS running as a client in VMware?](https://apple.stackexchange.com/questions/79452/how-to-increase-graphics-memory-in-mac-os-running-as-a-client-in-vmware)
- [Improving Sierra performance in VMWare?](https://www.insanelymac.com/forum/topic/321911-improving-sierra-performance-in-vmware/)

### Y9000x

- [Github](https://github.com/search?q=y9000x)
- [V2ex](https://www.google.com/search?newwindow=1&safe=active&sxsrf=ACYBGNTk3dwlBpAC6JbumR0kubVfoAo1WA%3A1573735516885&ei=XEzNXcXUNaDXz7sPpei5wAo&q=y9000x+%E9%BB%91%E8%8B%B9%E6%9E%9C+v2ex&oq=y9000x+%E9%BB%91%E8%8B%B9%E6%9E%9C+v2ex&gs_l=psy-ab.3..33i160l2.63867.68578..68797...1.0..0.229.1108.0j6j1......0....1..gws-wiz.......35i39j0i30.IwWNxYL2baw&ved=0ahUKEwjF8tDT3enlAhWg63MBHSV0DqgQ4dUDCAs&uact=5)
- [y9000x如何安装黑苹果？](https://www.zhihu.com/question/352678380)
