- [轻松在 VPS 搭建 Shadowsocks 翻墙 ($5/月 支付宝)](https://www.diycode.cc/topics/738)

- [Shadowsocks 一键安装脚本（四合一）](https://teddysun.com/486.html) / https://github.com/ishen7/Blog/issues/2

    ```shell
    wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
    chmod +x shadowsocks-all.sh
    ./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
    ./shadowsocks-all.sh uninstall
    /etc/init.d/shadowsocks-python start | stop | restart | status
    /etc/init.d/shadowsocks-r start | stop | restart | status
    /etc/init.d/shadowsocks-go start | stop | restart | status
    /etc/init.d/shadowsocks-libev start | stop | restart | status
    # Shadowsocks-Python 版：/etc/shadowsocks-python/config.json
    # ShadowsocksR 版：/etc/shadowsocks-r/config.json
    # Shadowsocks-Go 版：/etc/shadowsocks-go/config.json
    # Shadowsocks-libev 版：/etc/shadowsocks-libev/config.json
    ```

---

- https://www.vultr.com/
- https://www.linode.com/
- https://bwh1.net/index.php
- https://www.digitalocean.com/

---

- [Linux系统中VPN协议PPTP、L2TP、OpenVPN区别](https://my.oschina.net/lionel45/blog/523567)
- [Linux环境下使用pptpd搭建vpn服务器](https://blog.csdn.net/dongdong9223/article/details/80790203)
- [Ubuntu 架设 OpenVPN 实现内网穿透](https://cloud.tencent.com/developer/article/1193252)
- [Ubuntu 16.04搭建OpenVPN服务器以及客户端的使用](https://www.cnblogs.com/EasonJim/p/8339600.html)

---

- [申请Oracle Cloud永久免费服务+300美元试用额度](https://51.ruyo.net/14138.html)
- [申请 Oracle Cloud 永久免费服务 + 300 美元试用额度](https://www.v2ex.com/t/601572)

---

- [那些靠谱有口碑，值得推荐的国内国外 VPS 服务器 (美国香港日本)](https://www.iplaysoft.com/p/vps)

## VPN

### 付费服务

- [Just My Socks](https://justmysocks.net/)
- Lantern

## Proxy

- [关于SS/V2ray/Trojan三种节点的区别以及Trojan节点服务商推荐](https://pincong.rocks/article/9017)
- [V2Ray / Trojan 传输方式哪个好？(原理对比)](https://www.idleleo.com/02/4064.html)
- [V2Ray / SSR 加密方式哪个好? (加密算法对比)](https://www.idleleo.com/09/3058.html)

### Trojan

- https://github.com/trojan-gfw/trojan
- [自建梯子教程 --Trojan版本](https://trojan-tutor.github.io/2019/04/10/p41.html)
- [替代V2Ray？- Trojan搭建教程](https://www.idleleo.com/02/3899.html)

### v2ray

使用教程

- [V2Ray 配置指南](https://toutyrater.github.io/)
- [v2ray新手搭建使用教程](https://blog.sprov.xyz/2019/02/04/v2ray-simple-use/)
- [拯救被墙的IP，CDN + v2ray，安全的科学上网方法](https://blog.sprov.xyz/2019/03/11/cdn-v2ray-safe-proxy/)
- [2020 搭建 V2Ray 服务器最新教程](https://www.idleleo.com/09/2148.html)

安装脚本

- [Jrohy/multi-v2ray](https://github.com/Jrohy/multi-v2ray)
- [233boy/v2ray](https://github.com/233boy/v2ray)

    - [V2Ray一键安装脚本](https://github.com/233boy/v2ray/wiki/V2Ray%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E8%84%9A%E6%9C%AC)
    - [V2Ray搭建详细图文教程](https://github.com/233boy/v2ray/wiki/V2Ray%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E5%9B%BE%E6%96%87%E6%95%99%E7%A8%8B)
    - [V2RayN使用教程](https://github.com/233boy/v2ray/wiki/V2RayN%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)
    - [使用Cloudflare中转V2Ray流量](https://github.com/233boy/v2ray/wiki/%E4%BD%BF%E7%94%A8Cloudflare%E4%B8%AD%E8%BD%ACV2Ray%E6%B5%81%E9%87%8F)

- [支持多协议多用户的 v2ray 面板](https://github.com/sprov065/v2-ui)

客户端

- Android

    - BifrostV
    - [V2RayNG](https://github.com/2dust/v2rayNG)

- Window

    - v2rayW
    - V2RayN

- macOS

    - v2rayX
    - V2RayU

常见问题

- [websocket+tls+nginx+cdn断流严重](https://github.com/v2ray/v2ray-core/issues/1742)

#### CDN 中转


## VPS

### Bandwagon

- https://www.bandwagonhost.net/
- [Block List Check](https://kiwivm.64clouds.com/main-exec.php?mode=blacklistcheck)
- [怎样检查搬瓦工IP被墙](https://www.banwago.com/1265.html)
- [搬瓦工IP被墙后怎么购买新的IP地址](https://www.banwago.com/1407.html)

## CDN

### CloudFlare

- [GoFlyway 进阶教程：免费域名+免费CDN+HTTP伪装=被墙的IP继续做代理](https://doubibackup.com/mc1t27yh.html)
- [Cloudflare 国外免费 CDN 加速注册使用教程](https://www.vpsss.net/2417.html)
- [Cloudflare免费更换节点，加速你的网站](https://zhuanlan.zhihu.com/p/88593810)
- [十个你可能不知道的CloudFlare免费CDN加速技巧-SSL\DDOS\Cache](https://wzfou.com/cloudflare/)
- [CloudFlare免费CDN加速使用方法](https://zhuanlan.zhihu.com/p/29891330)
- [如何用CDN加速你的网站 – Cloudflare免费版详细使用教程](https://www.imhunk.com/cloudflare-tutorials/)
- [2019 Cloudflare 为阿里云域名做免费 CDN 加速，新手图文教程](https://guozh.net/use-cloudflare-speed-site-by-cdn/)
- [新Cloudflare：免费CDN+免费SSL证书轻松搞定https](https://www.4xseo.com/blog/3462/)
- [使用 Cloudflare 免费 DNS 服务器解析域名到搬瓦工 VPS 主机建站教程](https://www.bandwagonhost.net/5986.html)

## Domain

- [如何申请免费域名？](https://www.zhihu.com/question/19835955?sort=created)
- [11个国内外免费域名解析服务](https://yq.aliyun.com/articles/711533)
- [[教程]免费域名注册及域名解析(freenom&cloudflare)](https://zhujitips.com/328)

## TCP

- [谷歌BBR – TCP加速工具](https://blog.sprov.xyz/2019/02/04/bbr-tcp-faster/)
- [VPS 一键安装谷歌 BBR 加速](https://zhuanlan.zhihu.com/p/54655414)
- https://github.com/teddysun/across
