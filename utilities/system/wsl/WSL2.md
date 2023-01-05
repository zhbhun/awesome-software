# WSL2

## 教程

### 访问网络

- Window 访问 Linux 网络应用

    WSL2 可以直接试用 localhost 访问 Linux 网络应用，但要求 Window 版本必须大于 Build 18945，否则需要通过 Linux IP 地址来访问。

    ```bash
    $ ip addr | grep eth0
    ```

- Linux 访问 Window 网络应用

    Linux 必须采用 Window IP 地址的方式来访问网络应用。

    ```bash
    # 获取 Window IP 地址（nameserver），然后通过这个 IP 地址访问。
    $ cat /etc/resolv.conf
    ```

    ps：由于防火墙的问题需要做特殊配置，参考 [WSL2 中访问宿主机 Windows 的代理](https://zinglix.xyz/2020/04/18/wsl2-proxy/)

- 局域网访问 Linux 网络应用

    ```bash
    # 获取 WSL2 IP
    $ wsl -- hostname -I
    # 172.23.232.213

    # Windows 监听 8080，转发到 WSL2 8080
    $ netsh interface portproxy add v4tov4 listenport=8080 connectaddress=172.23.232.213 connectport=8080

    # 查看端口转发规则
    $ netsh interface portproxy show v4tov4

    # 删除端口转发规则
    $ netsh interface portproxy delete v4tov4 listenport=8080
    ```

    命令行函数

    ```bash
    # Powershell 命令向配置文件中写入了函数定义
    $ @"
    function Add-WSLPortProxy (`$Port = '8080', `$Protocol = 'TCP') {
        `$wslIP = wsl -- hostname -I
        `$wslIP = `$wslIP.Trim()
        netsh interface portproxy add v4tov4 listenport=`$Port connectaddress=`$wslIP connectport=`$Port
        New-NetFirewallRule -DisplayName "Allow `${Protocol} Inbound Port `${Port}" -Direction Inbound -Action Allow -Protocol `$Protocol -LocalPort `$Port
    }

    function Remove-WSLPortProxy (`$Port = '8080', `$Protocol = 'TCP') {
        netsh interface portproxy delete v4tov4 listenport=`$Port
        Remove-NetFirewallRule -DisplayName "Allow `${Protocol} Inbound Port `${Port}"
    }
    "@ | Out-File -FilePath $PROFILE -Append -Encoding ascii -Force

    # 重载配置，如重新打开 Powershell 则自动加载
    $ . $PROFILE

    # 无参调用，默认转发 TCP 8080 端口
    $ Add-WSLPortProxy

    # 无参调用删除函数，默认取消 TCP 8080
    $ Remove-WSLPortProxy

    # 指定其他端口，默认 TCP
    $ Add-WSLPortProxy 3306

    # 指定端口和协议
    $ Add-WSLPortProxy 3306 UDP

    # 根据端口删除，默认 TCP
    $ Remove-WSLPortProxy 3306

    # 指定端口和协议删除
    $ Remove-WSLPortProxy 3306 UDP
    ```



参考文献

- [Accessing network applications](https://docs.microsoft.com/en-us/windows/wsl/compare-versions#accessing-network-applications)
- [Win10 与 WSL2 间的网络和文件互访](https://logi.im/script/achieving-access-to-files-and-resources-on-the-network-between-win10-and-wsl2.html)

### TODO

- [WSL2 的几个使用技巧](https://zinglix.xyz/2020/04/18/wsl2-setting/)
- [升级 WSL2 Ubuntu 至 20.04 LTS](https://zinglix.xyz/2020/06/23/upgrade-wsl2/)
