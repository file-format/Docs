{
  "date" : "2021-05-24",
  "keywords" :["पीएसी", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "फाइल एक्सटेंशन", "प्रॉक्सी ऑटो-कॉन्फ़िगरेशन"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"पीएसी - प्रॉक्सी ऑटो-कॉन्फ़िगरेशन (पीएसी) फ़ाइल",
  "description":"पीएसी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो पीएसी फाइलें बना और खोल सकते हैं।",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## पीएसी फाइल क्या है?

.pac (प्रॉक्सी ऑटो-कॉन्फ़िगरेशन) एक्सटेंशन वाली फ़ाइल एक कॉन्फ़िगरेशन फ़ाइल है जिसमें वेब अनुरोध सीधे इंटरनेट पर भेजने या प्रॉक्सी सर्वर के माध्यम से रूट करने के नियम शामिल हैं। इसमें एक [javascript](/hi/web/js/) फ़ंक्शन शामिल है जो वेब अनुरोधों को सीधे गंतव्य पर भेजने के बजाय कुछ वेब प्रॉक्सी सर्वर के माध्यम से रूट करता है। एक प्रॉक्सी सर्वर एक मैन-इन-द-बीच की तरह है जो कई ग्राहकों से अनुरोध स्वीकार करता है और इन्हें गंतव्यों पर अग्रेषित करके सेवा प्रदान करता है। इनका उपयोग इंटरनेट ट्रैफिक पर लोड को नियंत्रित करने के लिए किया जाता है। PAC फाइलें किसी भी टेक्स्ट एडिटर जैसे Microsoft नोटपैड के साथ खोली जा सकती हैं।

## पीएसी फ़ाइल स्वरूप के बारे में अधिक जानकारी

पीएसी फाइलें पहली बार 1990 में नेटस्केप नेविगेटर में पेश की गई थीं। पीएसी फाइलें सादे जावास्क्रिप्ट पाठ प्रारूप में लिखी गई हैं और मानव पठनीय हैं। वेब ब्राउज़र के पास प्रॉक्सी सर्वर URL जानकारी निर्दिष्ट करने का विकल्प होता है जहाँ से प्रॉक्सी URL सूची प्राप्त की जाती है।

जावास्क्रिप्ट का उपयोग करते हुए पीएसी के अंदर परिभाषित कार्य इस प्रकार है:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### उदाहरण पीएसी फ़ाइल

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
## संदर्भ

* [पीएसी फ़ाइल क्या है?](https://findproxyforurl.com/)

