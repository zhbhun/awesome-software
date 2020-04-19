# SSH

## 实现

### [Win32-OpenSSH](https://github.com/PowerShell/Win32-OpenSSH)

常见问题

- `warning: agent returned different signature type ssh-rsa (expected rsa-sha2-512).`

    - 问题描述：在 window 通过 ssh 登录 Mac OS 系统时，遇到错误提示 `warning: agent returned different signature type ssh-rsa (expected rsa-sha2-512).`
    - 解决办法：OpenSSH 7.x 存在该问题，升级至 8.x 后解决
    - 参考文献

        [ssh-agent: agent returned different signature type](https://github.com/PowerShell/Win32-OpenSSH/issues/1263)

## 客户端

### putty

常见问题

- 如何设置自动登录

    1. 创建 Session: 打开 PuTTY，Session 选项卡中填写 Host Name，Port，Saved Sessions（假定名称为"session_name"）；
    2. 创建快捷方式：桌面右键，新建快捷方式，目标位置输入如下参数：

        putty -load "session_name" -l "username" -pw "password"

        ps：session_name, username, password 替换为自己的账号信息。

    [PuTTY 的自动登录设置](https://segmentfault.com/a/1190000000639516)

## 常见问题

- 如何通过代理来访问不可访问的服务器？

    使用 ssh 的 ProxyCommand 配合 nc 可以让 ssh 通过你设置的代理访问服务器

    ```bash
    $ ssh -o ProxyCommand="nc -X 5 -x 127.0.0.1:1080 %h %p" root@server
    ```

    nc命令的常用参数：-X 是指定代理协议：4 是 socks4 协议、5 是 socks5 协议；-x 是指定代理服务器和端口。

    - [让你的SSH通过HTTP代理或者SOCKS5代理](https://kanda.me/2019/07/01/ssh-over-http-or-socks/)
    - [ssh通过代理登录远程主机及穿越跳板机](https://www.xiebruce.top/650.html)

- 如何设置自动登录？

    ```bash
    $ apt install sshpass
    # 默认端口
    $ sshpass -p "YOUR_PASSWORD" ssh -o StrictHostKeyChecking=no YOUR_USERNAME@SOME_SITE.COM
    # 制定端口
    $ sshpass -p "YOUR_PASSWORD" ssh -o StrictHostKeyChecking=no YOUR_USERNAME@SOME_SITE.COM -p PORT
    ```

    ps：另外可以通过 SSH Key 来免密码登录。

    - [How to automate SSH login with password?](https://serverfault.com/questions/241588/how-to-automate-ssh-login-with-password)
    - [Automatically enter SSH password with script](https://stackoverflow.com/questions/12202587/automatically-enter-ssh-password-with-script)
