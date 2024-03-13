{
  "date": "2021-05-24",
  "keywords": [
"pac",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"Proksi Avtomatik Konfiqurasiya"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PAC - Proksi Avtomatik Konfiqurasiya (PAC) faylı",
  "description": "PAC fayl formatı və PAC fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pa-azc"
}
},
  "lastmod": "2021-06-17"
}

## PAC faylı nədir?

.pac (Proksi Avtomatik Konfiqurasiya) uzantısı olan fayl veb sorğularını birbaşa internetə göndərən və ya onları proxy server vasitəsilə yönləndirən qaydaları ehtiva edən konfiqurasiya faylıdır. O, veb sorğularını birbaşa təyinat yerinə göndərmək əvəzinə bəzi veb proksi server vasitəsilə yönləndirən [JavaScript](/web/js/) funksiyasını ehtiva edir. Proksi server birdən çox müştəridən gələn sorğuları qəbul edən və təyinat yerinə yönləndirməklə onlara xidmət göstərən ortada olan adam kimidir. Bunlar internet trafikindəki yükü idarə etmək üçün istifadə olunur. PAC faylları Microsoft Notepad kimi istənilən mətn redaktoru ilə açıla bilər.

## PAC fayl formatı haqqında ətraflı məlumat

PAC files were first introduced into Netscape Navigator in 1990. PAC faylları düz JavaScript mətn formatında yazılır və insanlar tərəfindən oxuna bilər. Veb-brauzerlərdə proksi-server URL-lər siyahısının alındığı yerdən proksi server URL məlumatını təyin etmək imkanı var.

JavaScript istifadə edərək PAC daxilində müəyyən edilmiş funksiya aşağıdakı kimidir:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Nümunə PAC Faylı

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
## İstinadlar

* [PAC faylı nədir?](https://findproxyforurl.com/)


