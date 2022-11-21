{
  "date" : "2021-06-28",
  "keywords" :["सीजीआई फाइल", "एक सीजीआई फाइल क्या है", "फाइल", "सीजीआई उदाहरण", "सीजीआई फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"सीजीआई फ़ाइल प्रारूप और एपीआई के बारे में जानें जो सीजीआई फाइलें बना और खोल सकते हैं।",
  "title" :"सीजीआई - कॉमन गेटवे इंटरफेस स्क्रिप्ट फाइल",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## सीजीआई फाइल क्या है?
एक CGI फ़ाइल को एक सामान्य गेटवे इंटरफ़ेस स्क्रिप्ट के रूप में जाना जाता है जिसका उपयोग वेब सर्वर द्वारा उपयोगकर्ता अनुरोधों को संसाधित करने के लिए बाहरी प्रोग्राम चलाने के लिए किया जाता है। .cgi एक्सटेंशन वाली फ़ाइल में सहेजी गई स्क्रिप्ट आमतौर पर C या पर्ल प्रोग्रामिंग भाषाओं में लिखी जाती है। वेब के शुरुआती दिनों से पेश किया गया था, जब वेब डेवलपर्स डेटाबेस को अपने वेब सर्वर से जोड़ना चाहते थे। एक सर्वर जो वेब सर्वर और डेटाबेस के बीच एक सामान्य गेटवे का समर्थन करता है, सीजीआई कोड को निष्पादित करने के लिए उपयुक्त था।

## सीजीआई फ़ाइल प्रारूप
CGI स्क्रिप्ट का उपयोग वेब सर्वर द्वारा स्वामी को यह कॉन्फ़िगर करने की सुविधा के लिए किया जाता है कि URL को कैसे संभाला जाएगा। प्रक्रिया आमतौर पर एक नई निर्देशिका (जहां दस्तावेज़ मुख्य रूप से स्थित हैं) को सीजीआई स्क्रिप्ट वाले के रूप में चिह्नित करके की जाती है; इसका सामान्य रूप से ज्ञात नाम cgi-bin है। उदाहरण के लिए, /usr/local/apache/htdocs/cgi-bin को वेब सर्वर पर CGI निर्देशिका के रूप में चुना जा सकता है। जब कोई वेब ब्राउज़र किसी ऐसे URL का अनुरोध करता है जो CGI निर्देशिका में किसी फ़ाइल को इंगित करता है, तो उस फ़ाइल (/hi/usr/local/apache/htdocs/cgi-bin/printenv.pl) को वेब ब्राउज़र पर भेजने के बजाय, HTTP सर्वर निर्दिष्ट स्क्रिप्ट को निष्पादित करता है और स्क्रिप्ट के आउटपुट को वेब ब्राउज़र पर लौटाता है। संक्षेप में, सीजीआई स्क्रिप्ट को मानक आउटपुट में भेजा जाने वाला कुछ भी विंडो के टर्मिनल में दिखाए जाने के बजाय वेब क्लाइंट को स्थानांतरित कर दिया जाता है।

### सीजीआई उदाहरण

पर्ल में लिखी गई सीजीआई स्क्रिप्ट के बाद जो वेब सर्वर द्वारा पारित सभी पर्यावरण चर दिखाती है:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

आउटपुट निम्न की तरह होगा:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## सीजीआई लिपियों का उपयोग
सीजीआई लिपियों वाली सीजीआई फाइलें आमतौर पर उपयोगकर्ता से इनपुट डेटा को संसाधित करने और प्रासंगिक आउटपुट डेटा का उत्पादन करने के लिए उपयोग की जाती हैं। विकी को लागू करना सीजीआई कार्यक्रम के उदाहरणों में से एक है। यदि उपयोगकर्ता एजेंट किसी प्रविष्टि के नाम के लिए अनुरोध भेजता है, तो वेब सर्वर CGI प्रोग्राम चलाता है। CGI प्रोग्राम उस प्रविष्टि के पृष्ठ का स्रोत प्राप्त करता है, उसे HTML में परिवर्तित करता है, और परिणाम को प्रिंट करता है। वेब सर्वर सीजीआई प्रोग्राम से आउटपुट प्राप्त करता है और इसे यूजर एजेंट को लौटाता है। फिर, यदि उपयोगकर्ता एजेंट "पृष्ठ संपादित करें" बटन पर क्लिक करके संपादन फ़ंक्शन को कॉल करता है, तो सीजीआई प्रोग्राम पृष्ठ की सामग्री के साथ एक HTML टेक्स्ट क्षेत्र या अन्य संपादन नियंत्रण दिखाता है। अंत में, यदि उपयोगकर्ता एजेंट "पृष्ठ प्रकाशित करें" बटन पर क्लिक करता है, तो CGI प्रोग्राम अपडेट किए गए HTML को उस प्रविष्टि के पृष्ठ के स्रोत में परिवर्तित करता है और इसे सहेजता है।



## संदर्भ

* [कॉमन गेटवे इंटरफेस - विकिपीडिया द्वारा] (https://en.wikipedia.org/wiki/Common_Gateway_Interface)

