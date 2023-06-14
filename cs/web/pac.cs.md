{
  "date" : "2021-05-24",
  "keywords" :["pac", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "Automatická konfigurace proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - soubor automatické konfigurace proxy (PAC)",
  "description":"Zjistěte, co je formát souboru PAC a rozhraní API, která mohou vytvářet a otevírat soubory PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Co je soubor PAC?

Soubor s příponou .pac (Proxy Auto-Configuration) je konfigurační soubor, který obsahuje pravidla odesílající webové požadavky přímo na internet nebo je směrovat přes proxy server. Obsahuje funkci [JavaScript](/cs/web/js/), která směruje webové požadavky přes nějaký webový proxy server, místo aby je posílala přímo na místo určení. Proxy server je jako man-in-the-middle, který přijímá požadavky od více klientů a obsluhuje je přesměrováním na místa určení. Ty se používají ke kontrole zatížení internetového provozu. Soubory PAC lze otevřít pomocí libovolného textového editoru, jako je Microsoft Notepad.

## Další informace o formátu souboru PAC

Soubory PAC byly poprvé zavedeny do Netscape Navigatoru v roce 1990. Soubory PAC jsou psány v prostém textovém formátu JavaScript a jsou čitelné pro člověka. Webové prohlížeče mají možnost zadat informace o adrese URL serveru proxy, odkud se načítá seznam adres URL proxy.

Funkce definovaná uvnitř PAC pomocí JavaScriptu je následující:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Příklad souboru PAC

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
## Reference

* [Co je soubor PAC?](https://findproxyforurl.com/)

