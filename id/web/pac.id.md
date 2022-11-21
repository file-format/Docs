{
  "date" : "2021-05-24",
  "keywords" :["pac", "File", "Extension", "File Format", "File Extension", "Proxy Auto-Configuration"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - File Konfigurasi Otomatis Proxy (PAC)",
  "description":"Pelajari tentang apa itu format file PAC dan API yang dapat membuat dan membuka file PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Apa itu file PAC?

File dengan ekstensi .pac (Proxy Auto-Configuration) adalah file konfigurasi yang berisi aturan pengiriman permintaan web langsung ke internet atau merutekannya melalui server proxy. Ini berisi fungsi [JavaScript](/id/web/js/) yang merutekan permintaan web melalui beberapa server proxy web alih-alih mengirimkannya langsung ke tujuan. Server proxy seperti man-in-the-middle yang menerima permintaan dari banyak klien dan melayaninya dengan meneruskannya ke tujuan. Ini digunakan untuk mengontrol beban lalu lintas internet. File PAC dapat dibuka dengan editor teks apa pun seperti Microsoft Notepad.

## Informasi Lebih Lanjut tentang Format File PAC

File PAC pertama kali diperkenalkan ke Netscape Navigator pada tahun 1990. File PAC ditulis dalam format teks JavaScript biasa dan dapat dibaca manusia. Browser web memiliki opsi untuk menentukan informasi URL server proxy dari mana daftar URL proxy diambil.

Fungsi yang didefinisikan di dalam PAC menggunakan JavaScript adalah sebagai berikut:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Contoh File PAC

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
## Referensi

* [Apa itu file PAC?](http://findproxyforurl.com/pac-file-introduction/)

