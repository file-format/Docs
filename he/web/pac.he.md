{
  "date" : "2021-05-24",
  "keywords" :["pac", "קובץ", "הרחבה", "פורמט קובץ", "הרחבת קובץ", "תצורה אוטומטית של פרוקסי"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - קובץ פרוקסי אוטומטי (PAC)",
  "description":"למד מה זה פורמט קובץ PAC וממשקי API שיכולים ליצור ולפתוח קובצי PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## מהו קובץ PAC?

קובץ עם סיומת .pac (Proxy Auto-Configuration) הוא קובץ תצורה המכיל כללים השולחים בקשות אינטרנט ישירות לאינטרנט או מנתבים אותן דרך שרת proxy. הוא מכיל פונקציה [JavaScript](/he/web/js/) המנתבת את בקשות האינטרנט דרך שרת פרוקסי אינטרנט כלשהו במקום לשלוח אותן ישירות ליעד. שרת פרוקסי הוא כמו אדם באמצע שמקבל בקשות ממספר לקוחות ומשרת אותם על ידי העברה ליעדים. אלה משמשים לשליטה בעומס על תעבורת האינטרנט. ניתן לפתוח קבצי PAC עם כל עורך טקסט כגון Microsoft Notepad.

## מידע נוסף על פורמט קובץ PAC

קובצי PAC הוצגו לראשונה ב-Netscape Navigator בשנת 1990. קובצי PAC נכתבים בפורמט טקסט JavaScript רגיל וניתנים לקריאה אנושית. לדפדפני אינטרנט יש אפשרות לציין את פרטי כתובת ה-URL של שרת ה-Proxy שממנו נשלפת רשימת כתובות ה-Proxy.

הפונקציה המוגדרת בתוך ה-PAC באמצעות JavaScript היא כדלקמן:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### קובץ PAC לדוגמה

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
## הפניות

* [מהו קובץ PAC?](http://findproxyforurl.com/pac-file-introduction/)

