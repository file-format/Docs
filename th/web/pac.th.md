{
  "date" : "2021-05-24",
  "keywords" :["pac", "File", "Extension", "File Format", "File Extension", "Proxy Auto-Configuration"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ PAC - ไฟล์การกำหนดค่าพร็อกซีอัตโนมัติ (PAC)",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PAC และ API ที่สามารถสร้างและเปิดไฟล์ PAC ได้",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## ไฟล์ PAC คืออะไร??

ไฟล์ที่มีนามสกุล .pac (การกำหนดค่าพร็อกซีอัตโนมัติ) เป็นไฟล์การกำหนดค่าที่มีกฎที่ส่งคำขอเว็บไปยังอินเทอร์เน็ตโดยตรงหรือกำหนดเส้นทางเหล่านี้ผ่านพร็อกซีเซิร์ฟเวอร์ ประกอบด้วยฟังก์ชัน [JavaScript](/th/web/js/) ที่กำหนดเส้นทางคำขอเว็บผ่านพร็อกซีเซิร์ฟเวอร์ของเว็บแทนที่จะส่งโดยตรงไปยังปลายทาง พร็อกซีเซิร์ฟเวอร์เป็นเหมือนคนกลางที่รับคำขอจากไคลเอ็นต์หลายเครื่องและให้บริการเหล่านี้โดยการส่งต่อไปยังปลายทาง สิ่งเหล่านี้ใช้เพื่อควบคุมโหลดการรับส่งข้อมูลทางอินเทอร์เน็ต ไฟล์ PAC สามารถเปิดได้ด้วยโปรแกรมแก้ไขข้อความใดๆ เช่น Microsoft Notepad

## ข้อมูลเพิ่มเติมเกี่ยวกับรูปแบบไฟล์ PAC

ไฟล์ PAC ถูกนำมาใช้ครั้งแรกใน Netscape Navigator ในปี 1990 ไฟล์ PAC เขียนในรูปแบบข้อความ JavaScript ธรรมดาและสามารถอ่านได้ เว็บเบราว์เซอร์มีตัวเลือกในการระบุข้อมูล URL ของพร็อกซีเซิร์ฟเวอร์จากตำแหน่งที่ดึงรายการ URL ของพร็อกซี

ฟังก์ชันที่กำหนดภายใน PAC โดยใช้ JavaScript มีดังนี้:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### ตัวอย่างไฟล์ PAC

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
## อ้างอิง

* [ไฟล์ PAC คืออะไร](http://findproxyforurl.com/pac-file-introduction/)

