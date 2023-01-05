## 系统设置

1. 软件源：[阿里云](https://developer.aliyun.com/mirror/)
2. 安装更新

    ```bash
    $ sudo apt update
    $ sudp apt upgrade
    ```

3. 安装缺失的语言支持

    设置 =》 区域和语言 =》 管理已经安装的语言

## 办公软件

- 输入法：[搜狗输入法](https://pinyin.sogou.com/linux/?r=pinyin)
- 浏览器：[Chrome](https://www.google.com/intl/zh-CN/chrome/)
- Office：[WPS](https://www.wps.cn/product/wpslinux)
- ...

## 编程开发

- 编辑器：[Visual Studio Code](https://code.visualstudio.com/)
- 网络代理：[v2ray](https://www.v2ray.com/chapter_00/install.html)

    - [Linux让终端走Sock5代理](https://blog.csdn.net/chenbetter1996/article/details/86616033)
    - [Mac OSX终端走shadowsocks代理](https://github.com/mrdulin/blog/issues/18)

- 版本管理：[git](https://git-scm.com/)

    ```bash
    $ sudo apt install git
    ```

### 前端

- [nvm](https://github.com/nvm-sh/nvm)

    ```bash
    $ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
    $ source ~/.bashrc
    ```

- [nrm](https://github.com/Pana/nrm)

    ```bash
    $ npm install -g nrm
    $ nrm use taobao
    ```

## 其他

```bash
$ sudo apt install net-tools # ifconfig
$ sudo apt install curl # curl
```
