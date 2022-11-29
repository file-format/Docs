{
  "date" : "2021-05-24",
  "keywords" :["pac", "Fil", "Tillägg", "Filformat", "Filtillägg", "Automatisk proxykonfiguration"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Proxy Auto-Configuration (PAC) fil",
  "description":"Läs mer om vad som är PAC-filformat och API:er som kan skapa och öppna PAC-filer.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Vad är en PAC fil?

En fil med tillägget .pac (Proxy Auto-Configuration) är en konfigurationsfil som innehåller regler som skickar webbförfrågningar direkt till internet eller dirigerar dessa via en proxyserver. Den innehåller en [JavaScript](/sv/web/js/) funktion som dirigerar webbförfrågningarna via någon webbproxyserver istället för att skicka dessa direkt till destinationen. En proxyserver är som en man-i-mitten som accepterar förfrågningar från flera klienter och betjänar dessa genom att vidarebefordra till destinationer. Dessa används för att styra belastningen på internettrafik. PAC-filer kan öppnas med vilken textredigerare som helst som Microsoft Notepad.

## Mer information om PAC-filformat

PAC-filer introducerades först i Netscape Navigator 1990. PAC-filer är skrivna i vanligt JavaScript-textformat och är läsbara för människor. Webbläsare har möjlighet att ange proxyserverns URL-information varifrån proxy-URL-listan hämtas.

Funktionen som definieras inuti PAC med JavaScript är följande:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Exempel PAC-fil

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
## Referenser

* [Vad är PAC-fil?](http://findproxyforurl.com/pac-file-introduction/)

