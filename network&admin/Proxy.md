# Proxy

## Mobile

- [phuedx/pinc](https://github.com/phuedx/pinc)
- [Stream](https://apps.apple.com/us/app/stream-network-debug-tool/id1312141691) - Network Debug Tool on the App Store
- [HttpCanary ](https://apkpure.com/httpcanary-%E2%80%94-http-sniffer-capture-analysis/com.guoshi.httpcanary) - HTTP Sniffer/Capture/Analysis

## Command

- [WPO-Foundation/tsproxy](https://github.com/WPO-Foundation/tsproxy)
- [squid](http://www.squid-cache.org/)
- [Privoxy](https://www.privoxy.org/)

    [Privoxy 教程](https://blog.zfanw.com/privoxy-tutorial/)

- [TooTallNate/proxy](https://github.com/TooTallNate/proxy)

## [Charles](https://www.charlesproxy.com)

### 证书

- [小米手机如何安装 Charles 证书](https://testerhome.com/topics/9445)

    1. chls.pro/ssl下载证书
    2. 进入到设置-wifi，点击高级，安装证书

    或者

    1. 把证书(即 crt 文件)传到手机存储，注意不要通过小米自带的浏览器上传 crt 文件
    2. 设置---更多设置---系统安全---加密与凭据---从存储设备安装--选择文件

- [在安卓手机上安装Charles证书](https://cosmeapp.github.io/2017/09/26/install-charles-certificate-android/)

## Linux

### 终端代理

- [Unix/Linux终端下代理快速设置](http://sunisdown.me/unixlinuxzhong-duan-xia-dai-li-kuai-su-she-zhi.html)

```shell
export PROXY_HOST="socks5://127.0.0.1:10808"
function proxy() {
  export HTTP_PROXY="$PROXY_HOST"
  export HTTPS_PROXY="$PROXY_HOST"
  export ALL_PROXY="$PROXY_HOST"
}
function unproxy () {
  unset HTTP_PROXY
  unset HTTPS_PROXY
  unset ALL_PROXY
}
```

## Mac

### 终端代理

- [Mac OSX终端走shadowsocks代理](https://github.com/mrdulin/blog/issues/18)
