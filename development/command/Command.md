# 命令行

## 网络

### HTTP

- curl
    - [curl 的用法指南](http://www.ruanyifeng.com/blog/2019/09/curl-reference.html)
    - [21 个 curl 命令练习](https://zhuanlan.zhihu.com/p/95745653)

### SSH

- 安装
    - [ubuntu开启SSH服务远程登录](https://blog.csdn.net/jackghq/article/details/54974141)

- 登录
    - [设置 SSH 通过密钥登录](https://hyjk2000.github.io/2012/03/16/how-to-set-up-ssh-keys/)

## 系统

- [LINUX 查看硬件配置命令](https://linux.cn/article-861-1.html)

### 进程

#### 守护进程

- [Linux 守护进程的启动方法](http://www.ruanyifeng.com/blog/2016/02/linux-daemon.html)
- [Systemd 入门教程：命令篇](http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-commands.html)

### 命令管理

- 查找命令

    - [Windows中查找命令的路径 (类似Linux中的which命令)](https://blog.csdn.net/sforiz/article/details/80540625)

## 文件

- 查找文件内容

    ```shell
    # 从文件内容查找匹配指定字符串的行
    grep "被查找的字符串" 文件名
    grep –i "被查找的字符串" 文件名 # 区分大小写

    # 从文件内容查找与正则表达式匹配的行
    grep –e "正则表达式" 文件名

    # 查找匹配的行数
    grep -c "被查找的字符串" 文件名

    # 从文件内容查找不匹配指定字符串的行
    grep –v "被查找的字符串" 文件名
    

    # 从指定目录开始查找所有扩展名为 .log 的文本文件，并找出包含 "ERROR" 的行
    find 目录名 -type f -name "*.log" | xargs grep "ERROR"
    ```

    [Linux里利用grep和find查找文件内容](https://blog.csdn.net/JiaJunLee/article/details/50470643)
