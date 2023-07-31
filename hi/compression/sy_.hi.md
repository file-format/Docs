{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ फ़ाइल स्वरूप - संपीड़ित SYS फ़ाइल",
  "description":"SY_ फ़ाइल स्वरूप और API के बारे में जानें जो SY_ फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## SY_ फ़ाइल क्या है?

एक SY_ फ़ाइल एक संपीड़ित .sys फ़ाइल है जिसका उपयोग सॉफ़्टवेयर इंस्टॉलर द्वारा इंस्टॉलर के अंदर पैक की गई स्थापना फ़ाइलों के आकार को कम करने के लिए किया जाता है। यह इंस्टॉलर के समग्र आकार को कम करता है। SY_ फ़ाइलों को Microsoft विस्तृत कमांड लाइन उपयोगिता का उपयोग करके विस्तारित किया जा सकता है जो एक या अधिक संपीड़ित फ़ाइलों का विस्तार करती है।

## SY_ फ़ाइल स्वरूप - अधिक जानकारी

SY_ फ़ाइलें संपीड़ित बाइनरी फ़ाइलों के रूप में डिस्क में सहेजी जाती हैं। हालाँकि, उनका आंतरिक फ़ाइल स्वरूप सार्वजनिक रूप से उपलब्ध नहीं है। Microsoft विस्तृत करें कमांड लाइन उपयोगिता निम्न कमांड लाइनों में से किसी एक का उपयोग करके SY_ फ़ाइलों का विस्तार कर सकती है।

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
विस्तारित होने पर, SY_ फ़ाइलें [SYS](https://docs.fileformat.com/system/sys/) फ़ाइल में बदल जाती हैं।

SY_ फ़ाइलें EX_ और DL_ फ़ाइलों के समान हैं।

## संदर्भ

* [StuffIt - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/StuffIt)
* [माइक्रोसॉफ्ट एक्सपैंड](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

