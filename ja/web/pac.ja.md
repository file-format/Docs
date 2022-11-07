{
  "date" : "2021-05-24",
  "keywords" :["pac","ファイル","拡張子","ファイル形式","ファイル拡張子","プロキシ自動構成"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - プロキシ自動構成 (PAC) ファイル",
  "description":"PAC ファイル形式とは何か,および PAC ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## .PAC オプション番号

.pac (Proxy Auto-Configuration) 拡張子を持つファイルは、Web 要求をインターネットに直接送信するか、プロキシ サーバー経由でこれらをルーティングするルールを含む構成ファイルです。 [JavaScript](/web/js/) 関数が含まれており、Web 要求を宛先に直接送信するのではなく、Web プロキシ サーバー経由でルーティングします。プロキシ サーバーは、複数のクライアントからの要求を受け取り、宛先に転送することで要求を処理する中間者のようなものです。これらは、インターネット トラフィックの負荷を制御するために使用されます。 PAC ファイルは、Microsoft メモ帳などの任意のテキスト エディターで開くことができます。

## PAC ファイル形式の詳細

PAC ファイルは、1990 年に Netscape Navigator に初めて導入されました。PAC ファイルはプレーンな JavaScript テキスト形式で書かれており、人間が読むことができます。 Web ブラウザーには、プロキシー URL リストがフェッチされるプロキシー・サーバー URL 情報を指定するオプションがあります。

JavaScript を使用して PAC 内で定義された関数は次のとおりです。

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### PAC ファイルの例

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
## 参考文献

※【PACファイルとは】(http://findproxyforurl.com/pac-file-introduction/)

