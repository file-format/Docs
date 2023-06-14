{
  "date" : "2021-05-24",
  "keywords" :["pac" , "ملف" , "امتداد" , "تنسيق الملف" , "امتداد الملف" , "التكوين التلقائي للخادم الوكيل"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - ملف التكوين التلقائي للخادم الوكيل (PAC)" ,
  "description":"تعرف على ما هو تنسيق ملف PAC وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PAC وفتحها." ,
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-06-17"
}

## ما هو ملف PAC؟

الملف بامتداد .pac (التهيئة التلقائية للوكيل) هو ملف تكوين يحتوي على قواعد إرسال طلبات الويب مباشرة إلى الإنترنت أو توجيهها عبر خادم وكيل. يحتوي على وظيفة [JavaScript](/ar/ web / js /) التي توجه طلبات الويب عبر بعض خادم وكيل الويب بدلاً من إرسالها مباشرةً إلى الوجهة. يشبه الخادم الوكيل رجل في الوسط يقبل الطلبات من عملاء متعددين ويقدمها عن طريق إعادة التوجيه إلى الوجهات. تستخدم هذه للتحكم في الحمل على حركة المرور على الإنترنت. يمكن فتح ملفات PAC باستخدام أي محرر نصوص مثل Microsoft Notepad.

## مزيد من المعلومات حول تنسيق ملف PAC

تم تقديم ملفات PAC لأول مرة في Netscape Navigator في عام 1990. تتم كتابة ملفات PAC بتنسيق نصي عادي JavaScript ويمكن قراءتها من قبل الإنسان. متصفحات الويب لديها خيار تحديد معلومات عنوان URL للخادم الوكيل من حيث يتم جلب قائمة عناوين URL للخادم الوكيل.

الوظيفة المحددة داخل مسوغ الوصول المحمي باستخدام جافا سكريبت هي كما يلي:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### مثال على ملف PAC

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
## مراجع

* [ما هو ملف PAC؟](https://findproxyforurl.com/)

