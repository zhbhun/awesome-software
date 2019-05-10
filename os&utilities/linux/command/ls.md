# 常见用法
- `ls -l`：按行显示文件，包含文件的类型，权限，硬链接个数，所属人，所属组，大小，最后访问或修改时间，名称；
- `ls -a`：显示所有文件，包含隐藏文件；
- `ls -la`：按行显示所有文件；
- `ls -lh`：按行显示文件，文件大小使用可读单位（KB，MB，GB）；
- `ls -lS`：按行显示文件，并按大小降序排列；
- `ls -ltr`：按行显示文件，并按修改日期从最早开始排列；

# 文件属性
- 节点

    Innode，索引节点，每个存储设备或存储设备的分区被格式化为文件系统后，应该有两部份，一部份是 Inode，另一部份是 Block。Block 是用来存储数据用的，而 Innode 是用来存储这些数据的信息索引值。

- 种类

    - `-`：普通文件，例如：纯文本文档，二进制文件，数据格式文件；
    - `d`：目录文件；
    - `c`：字符设备文件，例如猫等串口设备，`ls -al /dev/tty`；
    - `b`：区块设备文件，例如硬盘，光驱等设备，`ls -la /dev/sda1`；
    - `s`：数据接口文件，通常被用在网络上的数据承接，最常在 `/var/run` 这个目录中看到这种文件类型了；
    - `l`：符号链接文件；
    - `p`：数据输送文件；

    备注：区块设备文件是支持随机存取的接口设备，字符设备文件是一些串行端口的接口设备。

- 权限模式
- 链接数量
- 所归属的用户和用户组
- 最近访问或修改的时间
- 文件名或目录名

# 参考文献
- [每天一个 Linux 命令（25）：Linux 文件属性详解](http://blog.jobbole.com/105269/)
- [每天一个 Linux 命令（24）：Linux 文件类型与扩展名](http://blog.jobbole.com/109254/)