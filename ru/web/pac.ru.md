{
  "date" : "2021-05-24",
  "keywords" :["pac", "Файл", "Расширение", "Формат файла", "Расширение файла", "Автоконфигурация прокси"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC — файл автоматической настройки прокси-сервера (PAC)",
  "description":"Узнайте, что такое формат файла PAC и API, которые могут создавать и открывать файлы PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## .PAC вариант №

Файл с расширением .pac (Proxy Auto-Configuration) — это файл конфигурации, который содержит правила отправки веб-запросов непосредственно в Интернет или маршрутизации их через прокси-сервер. Он содержит функцию [JavaScript](/ru/web/js/), которая направляет веб-запросы через какой-либо веб-прокси-сервер вместо того, чтобы отправлять их напрямую в пункт назначения. Прокси-сервер подобен посреднику, который принимает запросы от нескольких клиентов и обслуживает их, перенаправляя по назначению. Они используются для контроля нагрузки на интернет-трафик. Файлы PAC можно открыть в любом текстовом редакторе, например в Блокноте Microsoft.

## Дополнительная информация о формате файла PAC

Файлы PAC были впервые представлены в Netscape Navigator в 1990 году. Файлы PAC записываются в текстовом формате JavaScript и удобочитаемы для человека. Веб-браузеры имеют возможность указать информацию об URL-адресе прокси-сервера, откуда извлекается список URL-адресов прокси-сервера.

Функция, определенная внутри PAC с помощью JavaScript, выглядит следующим образом:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Пример файла PAC

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
## использованная литература

* [Что такое файл PAC?] (http://findproxyforurl.com/pac-file-introduction/)

