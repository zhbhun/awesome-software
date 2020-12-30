# 同步

## rsync

rsync 是一个常用的 Linux 应用程序，用于文件同步。它可以在本地计算机与远程计算机之间，或者两个本地目录之间同步文件（但不支持两台远程计算机之间的同步）。它也可以当作文件复制工具，替代 cp 和 mv 命令。

- [rsync 用法教程](http://www.ruanyifeng.com/blog/2020/08/rsync.html)
- [rsync命令](https://man.linuxde.net/rsync)

### 安装

```bash
# Debian
$ sudo apt-get install rsync

# Red Hat
$ sudo yum install rsync

# Arch Linux
$ sudo pacman -S rsync
```

### 用法

```bash
# 递归同步，将源目录同步到目标目录，递归同步
$ rsync -r source destination

# 递归同步，将多个源目录同步到目标目录
$ rsync -r source1 source2 destination

# 归档模式，将源目录 source 完整地复制到目标目录 destination 下面，即形成了 destination/source 的目录结构
$ rsync -a source destination

# 归档模式，将源目录 source 里面的内容复制到目标目录 destination
$ rsync -a source/ destination

# 模拟执行
$ rsync -anv source/ destination

# 镜像拷贝（会删除目标目录文件）
$ rsync -av --delete source/ destination

# 忽略文件
$ rsync -av --exclude='*.txt' source/ destination
$ rsync -av --exclude 'dir1/*' source/ destinatio
$ rsync -av --exclude 'file1.txt' --exclude 'dir1/*' source/ destination
$ rsync -av --exclude={'file1.txt','dir1/*'} source/ destination
$ rsync -av --exclude-from='exclude-file.txt' source/ destination

# 远程同步
$ sync -av source/ username@remote_host:destination
$ rsync -av username@remote_host:source/ destination
$ rsync -av -e 'ssh -p 2234' source/ user@remote_host:/destination
```
