{
  "date": "2021-05-24",
  "keywords": [
"pac",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"Proxy Auto-konfiguration"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PAC - Proxy Auto-Configuration (PAC) fil",
  "description": "Lær om, hvad der er PAC-filformat og API'er, der kan oprette og åbne PAC-filer.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pa-dac"
}
},
  "lastmod": "2021-06-17"
}

## Hvad er en PAC fil?

En fil med filtypenavnet .pac (Proxy Auto-Configuration) er en konfigurationsfil, der indeholder regler, der sender webanmodninger direkte til internettet eller dirigerer disse via en proxyserver. Den indeholder en [JavaScript](/web/js/) funktion, der dirigerer webanmodningerne via en webproxyserver i stedet for at sende disse direkte til destinationen. En proxyserver er som en mand-i-midten, der accepterer anmodninger fra flere klienter og betjener disse ved at videresende til destinationer. Disse bruges til at styre belastningen af internettrafik. PAC-filer kan åbnes med en hvilken som helst teksteditor, såsom Microsoft Notesblok.

## Flere oplysninger om PAC-filformat

PAC files were first introduced into Netscape Navigator in 1990. PAC-filer er skrevet i almindeligt JavaScript-tekstformat og kan læses af mennesker. Webbrowsere har mulighed for at angive proxyserverens URL-oplysninger, hvorfra proxy-URL-listen hentes.

Funktionen defineret inde i PAC ved hjælp af JavaScript er som følger:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Eksempel PAC-fil

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
## Referencer

* [Hvad er PAC-fil?](https://findproxyforurl.com/)


