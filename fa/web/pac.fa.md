{
  "date": "2021-05-24",
  "keywords": [
"pac",
"فایل",
"افزونه",
"فرمت فایل",
"فرمت فایل",
"پیکربندی خودکار پروکسی"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "PAC - فایل پیکربندی خودکار پروکسی (PAC).",
  "description": "در مورد فرمت فایل PAC و APIهایی که می توانند فایل های PAC را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pa-fac"
}
}،
  "lastmod": "2021-06-17"
}

## فایل PAC چیست؟

یک فایل با پسوند pac. (پیکربندی خودکار پروکسی) یک فایل پیکربندی است که حاوی قوانینی است که درخواست‌های وب را مستقیماً به اینترنت ارسال می‌کند یا آنها را از طریق یک سرور پراکسی هدایت می‌کند. این شامل یک تابع [JavaScript](/web/js/) است که درخواست های وب را به جای ارسال مستقیم به مقصد، از طریق برخی از سرورهای پروکسی وب هدایت می کند. یک سرور پروکسی مانند یک مرد میانی است که درخواست‌های چندین مشتری را می‌پذیرد و آنها را با ارسال به مقصد ارائه می‌کند. اینها برای کنترل بار ترافیک اینترنت استفاده می شوند. فایل های PAC را می توان با هر ویرایشگر متنی مانند Microsoft Notepad باز کرد.

## اطلاعات بیشتر در مورد فرمت فایل PAC

PAC files were first introduced into Netscape Navigator in 1990. فایل های PAC با فرمت متنی ساده جاوا اسکریپت نوشته می شوند و قابل خواندن توسط انسان هستند. مرورگرهای وب این گزینه را دارند که اطلاعات URL سرور پروکسی را از جایی که لیست URL های پراکسی واکشی می شود، مشخص کنند.

تابع تعریف شده در داخل PAC با استفاده از جاوا اسکریپت به شرح زیر است:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### نمونه فایل PAC

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
## منابع

* [فایل PAC چیست؟](https://findproxyforurl.com/)


