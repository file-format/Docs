{
  "date" : "2021-05-24",
  "keywords" :["pac", "Файл", "Розширення", "Формат файлу", "Розширення файлу", "Автоконфігурація проксі"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - файл автоконфігурації проксі (PAC)",
  "description":"Дізнайтеся, що таке формат файлу PAC та API, які можуть створювати та відкривати файли PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Що таке файл PAC?

Файл із розширенням .pac (автоконфігурація проксі-сервера) — це файл конфігурації, який містить правила надсилання веб-запитів безпосередньо до Інтернету або маршрутизації через проксі-сервер. Він містить функцію [JavaScript](/uk/web/js/), яка направляє веб-запити через певний веб-проксі-сервер замість того, щоб надсилати їх безпосередньо до місця призначення. Проксі-сервер схожий на людину посередині, яка приймає запити від кількох клієнтів і обслуговує їх, пересилаючи до місць призначення. Вони використовуються для контролю навантаження на інтернет-трафік. Файли PAC можна відкрити будь-яким текстовим редактором, наприклад Microsoft Notepad.

## Додаткова інформація про формат файлу PAC

Файли PAC були вперше представлені в Netscape Navigator у 1990 році. Файли PAC записані у звичайному текстовому форматі JavaScript і їх читає людина. Веб-браузери мають можливість вказати інформацію про URL-адресу проксі-сервера, звідки буде отримано список URL-адрес проксі-сервера.

Функція, визначена в PAC за допомогою JavaScript, така:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Приклад файлу PAC

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
## Список літератури

* [Що таке файл PAC?](https://findproxyforurl.com/)

