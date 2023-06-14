{
  "date" : "2021-05-24",
  "keywords" :["pac", "File", "Extension", "File Format", "File Extension", "Proxy Auto-Configuration"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Proxy automatikus konfigurációs (PAC) fájl",
  "description":"További információ arról, hogy mi az a PAC-fájlformátum és az API-k, amelyek PAC-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Mi az a PAC fájl?

A .pac (Proxy Auto-Configuration) kiterjesztésű fájl olyan konfigurációs fájl, amely szabályokat tartalmaz, amelyek webes kéréseket közvetlenül az internetre küldenek, vagy ezeket egy proxyszerveren keresztül irányítják. Tartalmaz egy [JavaScript](/hu/web/js/) függvényt, amely a webes kéréseket valamilyen webproxyszerveren keresztül irányítja ahelyett, hogy közvetlenül a célállomásra küldené. A proxyszerver olyan, mint egy köztes ember, amely több klienstől is fogadja a kéréseket, és ezeket a célállomásoknak történő továbbítással szolgálja ki. Ezeket az internetes forgalom terhelésének szabályozására használják. A PAC fájlok bármely szövegszerkesztővel megnyithatók, például a Microsoft Notepaddal.

## További információ a PAC fájlformátumról

A PAC fájlokat először 1990-ben vezették be a Netscape Navigatorba. A PAC fájlok sima JavaScript szöveges formátumban készültek, és ember által olvashatók. A webböngészőknek lehetőségük van megadni a proxykiszolgáló URL-információit, ahonnan a proxy URL-ek listája lekérésre kerül.

A PAC-ban JavaScript használatával definiált függvény a következő:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### PAC-fájl példa

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
## Hivatkozások

* [Mi az a PAC-fájl?](https://findproxyforurl.com/)

