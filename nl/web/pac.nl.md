{
  "date" : "2021-05-24",
  "keywords" :["pac", "Bestand", "Extensie", "Bestandsindeling", "Bestandsextensie", "Automatische proxyconfiguratie"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Proxy Auto-Configuration (PAC)-bestand",
  "description":"Meer informatie over wat PAC-bestandsindeling is en API's die PAC-bestanden kunnen maken en openen.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Wat is een PAC-bestand?

Een bestand met de extensie .pac (Proxy Auto-Configuration) is een configuratiebestand dat regels bevat die webverzoeken rechtstreeks naar internet sturen of deze via een proxyserver routeren. Het bevat een [JavaScript](/nl/web/js/)-functie die de webverzoeken via een webproxyserver stuurt in plaats van deze rechtstreeks naar de bestemming te sturen. Een proxyserver is als een man-in-the-middle die verzoeken van meerdere clients accepteert en deze doorstuurt naar bestemmingen. Deze worden gebruikt om de belasting van het internetverkeer te beheersen. PAC-bestanden kunnen worden geopend met elke teksteditor zoals Microsoft Notepad.

## Meer informatie over PAC-bestandsindeling

PAC-bestanden werden voor het eerst geïntroduceerd in Netscape Navigator in 1990. PAC-bestanden zijn geschreven in gewoon JavaScript-tekstformaat en zijn door mensen leesbaar. Webbrowsers hebben de mogelijkheid om de proxyserver-URL-informatie op te geven van waaruit de lijst met proxy-URL's wordt opgehaald.

De functie die is gedefinieerd in de PAC met behulp van JavaScript is als volgt:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Voorbeeld PAC-bestand

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
## Referenties

* [Wat is PAC-bestand?](https://findproxyforurl.com/)

