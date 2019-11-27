# 命令

## 包管理

区别

| 工具\说明 | |
| --- | --- |
| dpkg | 只能安装包，不会安装相应的依赖（Debian 系统最早推出的包管理工具） |
| apt-get / apt-cache | 在 dpkg 基础上实现的可自动安装依赖的包管理工具 |
| aptitude | 对比 apt-get，aptitude 更加指南，并且提供了交互界面 |
| apt | 简化了 apt-get，apt-cache 等命令  |

用法

| 工具\功能 | 查找 | 查看 | 安装 | 更新 | 升级 | 删除 |
| --- | --- | --- | --- | --- | --- | --- |
| dpkg | `dpkg -l | grep xxx` | `dpkg -L xxx` / `dpkg -s xxx` | `dpkg -i /path/to/file` | - | - | `dpkg -r package_name` |
| apt-get / apt-cache | `apt-cache search xxx` | `apt-cache show xxx` / `apt-cache policy xxx` / `apt-cache depends xxx` / `apt-cache rdepends` | `apt-get install xxx` | `apt-get update` | `apt-get upgrade` / `apt-get dist-upgrade` | `apt-get remove package` / `apt-get autoremove` |
| aptitude | `aptitude search xxx` | `aptitude show xxx` | `aptitude install xxx` | `aptitude update` | `aptitude upgrade` / `aptitude full-upgrade` | `aptitude remove` |
| apt | `apt search xxx` | `apt show xxx` | `apt install xxx` | `apt update` | `apt upgrade` | `apt remove xxx`

参考文献

- [What is the difference between dpkg and aptitude/apt-get?](https://askubuntu.com/questions/309113/what-is-the-difference-between-dpkg-and-aptitude-apt-get)
- [有多少人用 apt 命令而不是用 apt-get 命令的？](https://www.v2ex.com/t/357932)

### dpkg

### aptitude

- aptitude update

## 文件管理

- ln

    - [每天一个linux命令（35）：ln 命令](https://www.cnblogs.com/peida/archive/2012/12/11/2812294.html)

- tee

    - [tee命令](http://man.linuxde.net/tee)

## 网络管理

- [Linux 查看端口占用情况](https://www.runoob.com/w3cnote/linux-check-port-usage.html)


## 系统管理

- [Systemd 入门教程：命令篇](http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-commands.html)
- [Systemd 入门教程：实战篇](http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-part-two.html)
- [init,service和systemctl的区别](https://blog.csdn.net/lineuman/article/details/52578399)
- [Difference between systemctl init.d and service](https://askubuntu.com/questions/911525/difference-between-systemctl-init-d-and-service)

### 权限管理

- [bash: 一键修改 硬盘 权限和用户组](https://blog.csdn.net/JNingWei/article/details/76339428)

### 用户管理

- [Linux查看用户所属的组](https://blog.csdn.net/yasi_xi/article/details/8493574)

### 定时任务

- [Linux/UNIX 定时任务 cron 详解](https://linux.cn/article-7513-1.html)
- [Linux crontab命令](https://www.runoob.com/linux/linux-comm-crontab.html)

### 会话管理

- screen

    - [screen 命令使用及示例](https://linux.cn/article-8215-1.html)
    - [Linux screen命令](https://www.runoob.com/linux/linux-comm-screen.html)

### 防火墙

- [ubuntu关闭防火墙](https://www.jianshu.com/p/a1a4455ff8fd)
- [iptables命令](https://man.linuxde.net/iptables)
- [iptables的基本语法格式](https://www.cnblogs.com/ggjucheng/archive/2012/08/19/2646476.html)

## 设备管理

### 磁盘管理

- [Linux中查看硬盘信息](https://daemon369.github.io/linux/2018/01/06/01-get-disks-info-in-linux)

挂在

- [linux里挂载（mount）和取消挂载（umount）命令的使用](https://blog.csdn.net/xiyangyang8/article/details/49725039)
- [Linux文件挂载配置文件fstab详解](https://blog.csdn.net/Kevinlou2008/article/details/15335151)
- [linux磁盘管理、新增磁盘、分区、挂载](https://www.cnblogs.com/alylee/p/Linux_disk_management_partition_mount.html)
- [Ubuntu下exFat格式移动磁盘的挂载](https://my.oschina.net/u/2306127/blog/777840)
- [【完整流程】Linux / Ubuntu 服务器 如何挂载 exfat 格式的 U盘 / 移动硬盘](https://blog.csdn.net/MLQ8087/article/details/53837791)
- [Ubuntu下挂载exfat格式移动硬盘](https://blog.csdn.net/penghouwen/article/details/49942155)
- [Ubuntu环境下挂载新硬盘](https://blog.csdn.net/zhengchaooo/article/details/79500116)
- [ubuntu下添加硬盘，分区以及自动挂载](https://www.jianshu.com/p/ec5579ef15a6)
- ...

分区

- [Linux下使用fdisk扩展分区容量](https://www.linuxprobe.com/linux-fdisk-size.html)
- [Linux下使用fdisk扩大分区容量（不丢失数据）](https://blog.51cto.com/sandshell/2119523)
- 

## 测试

### 性能测试

- [在 Linux 上检测 IDE/SATA SSD 硬盘的传输速度](https://zhuanlan.zhihu.com/p/33752337)
