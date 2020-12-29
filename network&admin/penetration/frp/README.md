# [FRP](https://github.com/fatedier/frp/)

frp 是一个可用于**内网穿透**的高性能的反向代理应用，支持 **tcp**, **udp** 协议，为 http 和 https 应用协议提供了额外的能力，且尝试性支持了点对点穿透。

应用场景

- 对外提供 Web 访问服务

    ```
    [http]
    type = tcp
    local_ip = 127.0.0.1
    local_port = 6000
    remote_port = 6000
    ```

- 通过 ssh 访问公司内网机器

    ```
    [ssh]
    type = tcp
    local_ip = 127.0.0.1
    local_port = 22
    remote_port = 6000
    ```

- 对外提供简单的文件访问服务

    ```
    [test_static_file]
    type = tcp
    remote_port = 6000
    plugin = static_file
    # 要对外暴露的文件目录
    plugin_local_path = /tmp/file
    # 访问 url 中会被去除的前缀，保留的内容即为要访问的文件路径
    plugin_strip_prefix = static
    plugin_http_user = abc
    plugin_http_passwd = abc
    ```

## 安装使用

```bash
$ wget https://github.com/fatedier/frp/releases/download/v0.34.1/frp_0.34.1_linux_amd64.tar.gz
$ tar -zxvf ./frp_0.34.1_linux_amd64.tar.gz
$ sudo cp -r ./frp_0.34.1_linux_amd64.tar.gz /etc/frp
$ sudo cp /etc/frp/frps /usr/bin/frps
$ sudo cp /etc/frp/frpc /usr/bin/frpc
$ sudo cp /etc/frp/systemd/frpc.service /etc/systemd/system
$ sudo cp /etc/frp/systemd/frps.service /etc/systemd/system
$ sudo systemctl enable frpc
$ sudo systemctl start frpc
$ sudo systemctl status frpc
$ sudo systemctl stop frpc
```

## 参考文献

- [FRP 简单入门安装配置教程 - 开源免费内网穿透工具，无公网 IP 远程访问](https://www.iplaysoft.com/frp.html)
- [使用frp内网穿透工具结合nginx实现内网web服务和tcp的转发](https://www.jianshu.com/p/0c49556e8e15)
- [FRP 简单入门安装配置教程 - 开源免费内网穿透工具，无公网 IP 远程访问](https://www.iplaysoft.com/frp.html)
- [一款很好用的内网穿透工具--FRP](https://www.jianshu.com/p/00c79df1aaf0)
- [frp后台运行和停止](https://segmentfault.com/a/1190000017911165)
