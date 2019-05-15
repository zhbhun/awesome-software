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

### 定时任务

- [Linux/UNIX 定时任务 cron 详解](https://linux.cn/article-7513-1.html)
- [Linux crontab命令](https://www.runoob.com/linux/linux-comm-crontab.html)

### 会话管理

- screen

    - [screen 命令使用及示例](https://linux.cn/article-8215-1.html)
    - [Linux screen命令](https://www.runoob.com/linux/linux-comm-screen.html)
