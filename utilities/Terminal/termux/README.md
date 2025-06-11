# [Termux](https://termux.com)

- [termux-packages](https://github.com/termux/termux-packages)
- [Termux 入门教程：架设手机 Server 下载文件](http://www.ruanyifeng.com/blog/2019/07/termux-tutorial.html)

## 使用

### 包管理

- 安装包：`pkg install [package name]`
- 卸载软件包：`pkg uninstall [package name]`
- 列出所有软件包：`pkg list-all`
- 列出已安装包：`pkg list-installed`
- 更新源信息：`pkg update`
- 升级所有已安装软件：`pkg upgrade`

ps：pkg 的底层就是 apt，只是运行前会执行一次apt update。

### 镜像源

`termux-change-repo`

### 多窗口

```
pkg install tmux
tmux
# Ctrl+b c 新建窗口
# Ctrl+b n 下一个窗口
# Ctrl+b d detach
```

### 本地存储

- termux-setup-storage

### 持久化

1. 安装 [Termux:Boot 插件](https://f-droid.org/packages/com.termux.boot/)
2. 将启动命令写入 `~/.termux/boot/start.sh`

### 窗口管理

```
pkg install tmux
tmux new -s mysession
# 按下 Ctrl+b 然后按 d 来分离会话。
tmux ls
tmux attach -t mysession
tmux kill-session -t mysession
```

### 子系统管理

ps：基于 proot 技术，在无需 root 权限的情况下模拟 Linux 的 chroot 环境。

- 安装管理器：`pkg install proot-distro`
- 查看可用的子系统列表：`proot-distro list`
- 安装子系统：`proot-distro install ubuntu`
- 进入子系统：`proot-distro login ubuntu`
- 退出子系统：`exit`
- 卸载子系统：`proot-distro remove ubuntu`

### SSH

```
pkg install openssh
passwd
sshd
# ssh -p 8022 username@手机IP
```

### FRP

```
pkg install wget tar
wget https://github.com/fatedier/frp/releases/download/v0.x.x/frp_0.x.x_linux_arm64.tar.gz
tar -zxvf frp_0.x.x_linux_arm64.tar.gz
./frpc -c frpc.ini
```

### ZSH

```
pkg install zsh
chsh -s zsh
pkg install git
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## 子系统

### SSH

```
apt update && apt upgrade -y
apt install openssh-server -y
cat /etc/ssh/sshd_config
/usr/sbin/sshd
# 如果提示 Missing privilege separation directory: /run/sshd，先建一下：
mkdir -p /run/sshd 
ps aux | grep sshd
passwd
netstat -tnlp | grep ssh
ssh username@127.0.0.1 -p 22
```
