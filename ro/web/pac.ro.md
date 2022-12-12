{
  "date" : "2021-05-24",
  "keywords" :["pac", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "Configurare automată proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Fișier de configurare automată proxy (PAC)",
  "description":"Aflați despre ce este formatul de fișier PAC și API-urile care pot crea și deschide fișiere PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Ce este un fișier PAC?

Un fișier cu extensia .pac (Proxy Auto-Configuration) este un fișier de configurare care conține reguli care trimit cereri web direct pe internet sau le direcționează printr-un server proxy. Conține o funcție [JavaScript](/ro/web/js/) care direcționează cererile web prin intermediul unui server proxy web în loc să le trimită direct la destinație. Un server proxy este ca un om din mijloc care acceptă cereri de la mai mulți clienți și le servește prin redirecționarea către destinații. Acestea sunt folosite pentru a controla încărcarea traficului de internet. Fișierele PAC pot fi deschise cu orice editor de text, cum ar fi Microsoft Notepad.

## Mai multe informații despre formatul fișierului PAC

Fișierele PAC au fost introduse pentru prima dată în Netscape Navigator în 1990. Fișierele PAC sunt scrise în format text simplu JavaScript și pot fi citite de om. Browserele web au opțiunea de a specifica informațiile URL ale serverului proxy de unde este preluată lista de adrese URL proxy.

Funcția definită în interiorul PAC folosind JavaScript este următoarea:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Exemplu de fișier PAC

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
## Referințe

* [Ce este fișierul PAC?](http://findproxyforurl.com/pac-file-introduction/)

