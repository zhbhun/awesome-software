# 内网穿透

- [frp](https://github.com/fatedier/frp)
- [ngrok](https://ngrok.com/) / [inconshreveable/ngrok](https://github.com/inconshreveable/ngrok)

    - [learn-ngrok](https://github.com/dwyl/learn-ngrok)
    - [ngrok搭建指南](https://luozm.github.io/ngrok)
    - https://github.com/wernight/docker-ngrok

- [nps](https://github.com/cnlh/nps)
- [lanproxy](https://github.com/ffay/lanproxy)
- [花生壳](https://hsk.oray.com)

## FRP

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


参考文献

- [FRP 简单入门安装配置教程 - 开源免费内网穿透工具，无公网 IP 远程访问](https://www.iplaysoft.com/frp.html)

## 参考文献

- [使用frp内网穿透工具结合nginx实现内网web服务和tcp的转发](https://www.jianshu.com/p/0c49556e8e15)
- [FRP 简单入门安装配置教程 - 开源免费内网穿透工具，无公网 IP 远程访问](https://www.iplaysoft.com/frp.html)
- [一款很好用的内网穿透工具--FRP](https://www.jianshu.com/p/00c79df1aaf0)
- [frp后台运行和停止](https://segmentfault.com/a/1190000017911165)
