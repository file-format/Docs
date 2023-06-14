{
  "date" : "2021-05-24",
  "keywords" :["pac","文件","扩展名","文件格式","文件扩展名","代理自动配置"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - 代理自动配置 (PAC) 文件",
  "description":"了解什么是 PAC 文件格式以及可以创建和打开 PAC 文件的 API。",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## 什么是一 .pac 文件？

带有 .pac（代理自动配置）扩展名的文件是一个配置文件，其中包含将 Web 请求直接发送到 Internet 或通过代理服务器路由这些规则的规则。它包含一个 [JavaScript](/zh/web/js/) 函数，该函数通过一些 Web 代理服务器路由 Web 请求，而不是将这些请求直接发送到目的地。代理服务器就像一个中间人，它接受来自多个客户端的请求并通过转发到目的地来服务这些请求。这些用于控制互联网流量的负载。 PAC 文件可以使用任何文本编辑器（例如 Microsoft 记事本）打开。

## 有关 PAC 文件格式的更多信息

PAC 文件于 1990 年首次引入 Netscape Navigator。PAC 文件以纯 JavaScript 文本格式编写，可供人类阅读。 Web 浏览器可以选择指定从中获取代理 URL 列表的代理服务器 URL 信息。

PAC 内部使用 JavaScript 定义的函数如下：

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### 示例 PAC 文件

```JavaScript
function FindProxyForURL(url, host) {

// If the hostname matches, send direct.
	if (dnsDomainIs(host, "intranet.domain.com") ||
		shExpMatch(host, "(*.abcdomain.com|abcdomain.com)"))
		return "DIRECT";

// If the protocol or URL matches, send direct.
	if (url.substring(0, 4)=="ftp:" ||
		shExpMatch(url, "http://abcdomain.com/folder/*"))
		return "DIRECT";

// If the requested website is hosted within the internal network, send direct.
	if (isPlainHostName(host) ||
		shExpMatch(host, "*.local") ||
		isInNet(dnsResolve(host), "10.0.0.0", "255.0.0.0") ||
		isInNet(dnsResolve(host), "172.16.0.0",  "255.240.0.0") ||
		isInNet(dnsResolve(host), "192.168.0.0",  "255.255.0.0") ||
		isInNet(dnsResolve(host), "127.0.0.0", "255.255.255.0"))
		return "DIRECT";

// If the IP address of the local machine is within a defined
// subnet, send to a specific proxy.
	if (isInNet(myIpAddress(), "10.10.5.0", "255.255.255.0"))
		return "PROXY 1.2.3.4:8080";

// DEFAULT RULE: All other traffic, use below proxies, in fail-over order.
	return "PROXY 4.5.6.7:8080; PROXY 7.8.9.10:8080";

}
```
## 参考

* [什么是 PAC 文件？](https://findproxyforurl.com/)

