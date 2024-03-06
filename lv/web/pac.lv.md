{
  "date": "2021-05-24",
  "keywords": [
"pac",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"Starpniekservera automātiskā konfigurācija"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PAC — starpniekservera automātiskās konfigurācijas (PAC) fails",
  "description": "Uzziniet, kas ir PAC faila formāts un API, kas var izveidot un atvērt PAC failus.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pa-lvc"
}
},
  "lastmod": "2021-06-17"
}

## Kas ir PAC fails?

Fails ar paplašinājumu .pac (starpniekservera automātiskā konfigurācija) ir konfigurācijas fails, kurā ir ietverti noteikumi, kas nosūta tīmekļa pieprasījumus tieši uz internetu vai maršrutē tos caur starpniekserveri. Tā satur funkciju [JavaScript](/web/js/), kas novirza tīmekļa pieprasījumus caur kādu tīmekļa starpniekserveri, nevis sūta tos tieši uz galamērķi. Starpniekserveris ir kā starpnieks, kas pieņem pieprasījumus no vairākiem klientiem un apkalpo tos, pārsūtot uz galamērķiem. Tos izmanto, lai kontrolētu interneta trafika slodzi. PAC failus var atvērt ar jebkuru teksta redaktoru, piemēram, Microsoft Notepad.

## Plašāka informācija par PAC faila formātu

PAC files were first introduced into Netscape Navigator in 1990. PAC faili ir rakstīti vienkāršā JavaScript teksta formātā un ir cilvēka lasāmi. Tīmekļa pārlūkprogrammām ir iespēja norādīt starpniekservera URL informāciju, no kuras tiek iegūts starpniekservera vietrāžu URL saraksts.

Funkcija, kas definēta PAC, izmantojot JavaScript, ir šāda:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### PAC faila piemērs

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
## Atsauces

* [Kas ir PAC fails?](https://findproxyforurl.com/)


