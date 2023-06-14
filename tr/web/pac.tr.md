{
  "date" : "2021-05-24",
  "keywords" :["pac", "Dosya", "Uzantı", "Dosya Biçimi", "Dosya Uzantısı", "Proxy Otomatik Yapılandırma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Proxy Otomatik Yapılandırma (PAC) dosyası",
  "description":"PAC dosya biçiminin ne olduğunu ve PAC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## .pac dosyası nedir?

.pac (Proxy Auto-Configuration) uzantılı bir dosya, web isteklerini doğrudan internete gönderen veya bunları bir proxy sunucusu aracılığıyla yönlendiren kuralları içeren bir yapılandırma dosyasıdır. Web isteklerini doğrudan hedefe göndermek yerine bazı web proxy sunucuları aracılığıyla yönlendiren bir [JavaScript](/tr/web/js/) işlevi içerir. Proxy sunucusu, birden çok istemciden gelen istekleri kabul eden ve bunları hedeflere ileterek sunan bir ortadaki adam gibidir. Bunlar internet trafiğindeki yükü kontrol etmek için kullanılır. PAC dosyaları, Microsoft Notepad gibi herhangi bir metin düzenleyiciyle açılabilir.

## PAC Dosya Formatı hakkında daha fazla bilgi

PAC dosyaları ilk olarak 1990 yılında Netscape Navigator'a tanıtıldı. PAC dosyaları düz JavaScript metin biçiminde yazılır ve insanlar tarafından okunabilir. Web tarayıcıları, proxy URL'leri listesinin getirildiği yerden proxy sunucusu URL bilgilerini belirtme seçeneğine sahiptir.

PAC içinde JavaScript kullanılarak tanımlanan fonksiyon aşağıdaki gibidir:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Örnek PAC Dosyası

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
## Referanslar

* [PAC dosyası nedir?](https://findproxyforurl.com/)

