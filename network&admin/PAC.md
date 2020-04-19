# PAC

PAC(Proxy Auto Config)，代理自动设置。一个 PAC 文件包含一个 JavaScript 形式的函数 “FindProxyForURL(url, host)”。这个函数返回一个包含一个或多个访问规则的字符串。用户代理根据这些规则适用一个特定的代理器或者直接访问。当一个代理服务器无法响应的时候，多个访问规则提供了其他的后备访问方法。浏览器在访问其他页面以前，首先访问这个PAC文件。

示例 1：指定所有流量一律走代理 172.18.104.54:8888，如果代理挂了，则直接连接不走代理。

```js
function FindProxyForURL(url, host) {
  return "PROXY 172.18.104.54:8888; DIRECT"; // HTTP 代理
  // return "SOCKS 172.18.104.54:8888; DIRECT"; // socks5 代理
}
```

示例 2：www.mydomain.com 的流量直接走，不走代理；www.mydomain.com 以外的流量默认走代理，先走 myproxy:80 代理，如果超时那就再走 myotherproxy:8080；如果这个还走不通，就直连。

```js
function FindProxyForURL(url, host) {
  if (host == "www.mydomain.com") {
    return "DIRECT";
  }
  return "PROXY myproxy:80; PROXY myotherproxy:8080; DIRECT";
}
```

## 常见问题

- Android 和 iOS 原生不支持 Socks5 代理

    - [为什么Android和iOS都不原生支持Socks5代理？](https://www.zhihu.com/question/23857102)
    - [Socks proxy in android](https://stackoverflow.com/questions/18485807/socks-proxy-in-android)

## 参考文献

- [PAC 百科](https://zh.wikipedia.org/wiki/%E4%BB%A3%E7%90%86%E8%87%AA%E5%8A%A8%E9%85%8D%E7%BD%AE)
- [Android 代理自动配置PAC研究](https://juejin.im/post/5a93cfebf265da4e951908af)
- [详解代理自动配置 PAC](https://zhuanlan.zhihu.com/p/22166179)
