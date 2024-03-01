{
  "date": "2021-05-24",
  "keywords": [
"pac",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"Välityspalvelimen automaattinen määritys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PAC - Välityspalvelimen automaattinen määritystiedosto (PAC).",
  "description": "Opi, mikä on PAC-tiedostomuoto ja API:t, jotka voivat luoda ja avata PAC-tiedostoja.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pa-fic"
}
},
  "lastmod": "2021-06-17"
}

## Mikä on PAC-tiedosto?

Tiedosto, jonka laajennus on .pac (Proxy Auto-Configuration), on määritystiedosto, joka sisältää säännöt, jotka lähettävät verkkopyyntöjä suoraan Internetiin tai reitittävät ne välityspalvelimen kautta. Se sisältää {{HYPERLINKKI}}-toiminnon, joka reitittää verkkopyynnöt jonkin web-välityspalvelimen kautta sen sijaan, että lähettäisi ne suoraan kohteeseen. Välityspalvelin on kuin välimies, joka hyväksyy pyynnöt useilta asiakkailta ja palvelee niitä välittämällä niitä kohteisiin. Näitä käytetään hallitsemaan Internet-liikenteen kuormitusta. PAC-tiedostoja voidaan avata millä tahansa tekstieditorilla, kuten Microsoft Notepadilla.

## Lisätietoja PAC-tiedostomuodosta

PAC files were first introduced into Netscape Navigator in 1990. PAC-tiedostot on kirjoitettu tavallisessa JavaScript-tekstimuodossa ja ovat ihmisen luettavissa. Web-selaimet voivat määrittää välityspalvelimen URL-tiedot, josta välityspalvelimen URL-osoitteiden luettelo haetaan.

PAC:n sisällä JavaScriptin avulla määritetty toiminto on seuraava:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Esimerkki PAC-tiedostosta

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
## Viitteet

* [Mikä on PAC-tiedosto?](https://findproxyforurl.com/)


