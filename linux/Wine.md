# Wine

- [Wine](http://wiki.ubuntu.org.cn/Wine)

## 安装

- 有安装来自其他仓库的 wine，需要清除该安装包和依赖它的安装包：wine，wine-mono、wine-gecko、winetricks
- 开启 32 bit 架构支持

    ```bash
    sudo dpkg --add-architecture i386
    ```

- 添加仓库密钥

   ```bash
    wget -nc https://dl.winehq.org/wine-builds/winehq.key
    sudo apt-key add winehq.key
    ```

- 添加仓库

    - Ubuntu 18.10：`sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ cosmic main'`
    - Ubuntu 18.04 / Linux Mint 19.x：`sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ bionic main'`
    - Ubuntu 16.04 / Linux Mint 18.x：`sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ xenial main'`
    - Ubuntu 14.04 / Linux Mint 17.x：`sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ trusty main'`

- 更新包

    ```bash
    sudo apt update
    ```

- 安装包

    - 稳定分支：`sudo apt install --install-recommends winehq-stable`
    - 开发分支：`sudo apt install --install-recommends winehq-devel`
    - Staging 分支：`sudo apt install --install-recommends winehq-staging`

- 检查安装是否成功：`wine --version`

参考文献

- https://wiki.winehq.org/Download_zhcn
- [安装 WineHQ 安装包](https://wiki.winehq.org/Ubuntu_zhcn)

## Winetricks

- [winetricks](https://github.com/Winetricks/winetricks)
- [Winetricks](http://wiki.ubuntu.org.cn/Winetricks)
- [winetricks-zh](https://github.com/hillwoodroc/winetricks-zh)
