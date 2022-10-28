{
  "date" : "2021-05-24",
  "keywords" :["pac", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "Automatische Proxy-Konfiguration"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Proxy-Autokonfigurationsdatei (PAC)",
  "description":"Erfahren Sie mehr über das PAC-Dateiformat und die APIs, die PAC-Dateien erstellen und öffnen können.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Was ist eine PAC-Datei?

Eine Datei mit der Erweiterung .pac (Proxy Auto-Configuration) ist eine Konfigurationsdatei, die Regeln enthält, die Webanfragen direkt an das Internet senden oder diese über einen Proxy-Server weiterleiten. Es enthält eine [JavaScript](/de/web/js/)-Funktion, die die Webanfragen über einen Webproxyserver leitet, anstatt sie direkt an das Ziel zu senden. Ein Proxy-Server ist wie ein Man-in-the-Middle, der Anfragen von mehreren Clients entgegennimmt und diese durch Weiterleitung an Ziele bedient. Diese werden verwendet, um die Belastung des Internetverkehrs zu steuern. PAC-Dateien können mit jedem Texteditor wie Microsoft Notepad geöffnet werden.

## Weitere Informationen zum PAC-Dateiformat

PAC-Dateien wurden erstmals 1990 in Netscape Navigator eingeführt. PAC-Dateien sind im reinen JavaScript-Textformat geschrieben und für Menschen lesbar. Webbrowser haben die Möglichkeit, die Proxyserver-URL-Informationen anzugeben, von denen die Proxy-URL-Liste abgerufen wird.

Die im PAC mit JavaScript definierte Funktion lautet wie folgt:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Beispiel-PAC-Datei

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
## Verweise

* [Was ist eine PAC-Datei?](http://findproxyforurl.com/pac-file-introduction/)

