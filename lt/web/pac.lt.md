{
  "date": "2021-05-24",
  "keywords": [
"pac",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"Tarpinio serverio automatinė konfigūracija"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PAC – tarpinio serverio automatinės konfigūracijos (PAC) failas",
  "description": "Sužinokite, kas yra PAC failo formatas ir API, kurios gali kurti ir atidaryti PAC failus.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pa-ltc"
}
},
  "lastmod": "2021-06-17"
}

## Kas yra PAC failas?

Failas su plėtiniu .pac (tarpinio serverio automatinė konfigūracija) yra konfigūracijos failas, kuriame yra taisyklės, siunčiančios žiniatinklio užklausas tiesiai į internetą arba nukreipiančios jas per tarpinį serverį. Jame yra funkcija [JavaScript](/web/js/), kuri nukreipia žiniatinklio užklausas per tam tikrą žiniatinklio tarpinį serverį, o ne siunčia jas tiesiai į paskirties vietą. Įgaliotasis serveris yra tarsi tarpininkas, kuris priima užklausas iš kelių klientų ir aptarnauja jas persiųsdamas į paskirties vietas. Jie naudojami interneto srauto apkrovai valdyti. PAC failus galima atidaryti naudojant bet kurį teksto rengyklę, pvz., Microsoft Notepad.

## Daugiau informacijos apie PAC failo formatą

PAC files were first introduced into Netscape Navigator in 1990. PAC failai parašyti paprastu JavaScript teksto formatu ir yra skaitomi žmonėms. Žiniatinklio naršyklės turi galimybę nurodyti įgaliotojo serverio URL informaciją, iš kurios gaunamas įgaliotojo serverio URL sąrašas.

Funkcija, apibrėžta PAC viduje naudojant JavaScript, yra tokia:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### PAC failo pavyzdys

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
## Nuorodos

* [Kas yra PAC failas?](https://findproxyforurl.com/)


