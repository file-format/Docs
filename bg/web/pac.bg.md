{
  "date" : "2021-05-24",
  "keywords" :["pac", "Файл", "Разширение", "Файлов формат", "Разширение на файл", "Автоматично конфигуриране на прокси"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - файл за автоматично конфигуриране на прокси (PAC)",
  "description":"Научете какво е PAC файлов формат и API, които могат да създават и отварят PAC файлове.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Какво е PAC файл?

Файл с разширение .pac (Proxy Auto-Configuration) е конфигурационен файл, който съдържа правила, изпращащи уеб заявки директно към интернет или маршрутизиращи ги през прокси сървър. Той съдържа функция [JavaScript](/bg/web/js/), която насочва уеб заявките през някакъв уеб прокси сървър, вместо да ги изпраща директно до дестинацията. Прокси сървърът е като човек по средата, който приема заявки от множество клиенти и ги обслужва чрез препращане към дестинации. Те се използват за контролиране на натоварването на интернет трафика. PAC файловете могат да се отварят с всеки текстов редактор като Microsoft Notepad.

## Повече информация за файловия формат PAC

PAC файловете са въведени за първи път в Netscape Navigator през 1990 г. PAC файловете са написани в обикновен текстов формат на JavaScript и са четими от хора. Уеб браузърите имат опцията да посочат информацията за URL адреса на прокси сървъра, откъдето се извлича списъкът с URL адреси на прокси сървъра.

Функцията, дефинирана в PAC с помощта на JavaScript, е следната:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Примерен PAC файл

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
## Препратки

* [Какво е PAC файл?](https://findproxyforurl.com/)

