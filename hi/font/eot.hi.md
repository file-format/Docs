{
  "date" : "2020-08-20",
  "keywords" :["ईओटी फाइल", "ईओटी फाइल फॉर्मेट", "ईओटी फाइल क्या है", "फाइल", "ईओटी उदाहरण", "ईओटी फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ईओटी - ट्रू टाइप फ़ॉन्ट फ़ाइल स्वरूप",
  "description":"ईओटी फाइल बनाने और खोलने के लिए ईओटी फाइल फॉर्मेट और एपीआई के बारे में जानें।",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## ईओटी फाइल क्या है?

.eot एक्सटेंशन वाली फ़ाइल एक ओपन टाइप फ़ॉन्ट है जो एक दस्तावेज़ में एम्बेड किया गया है। इनका उपयोग ज्यादातर वेब फाइलों जैसे वेब पेज में किया जाता है। यह Microsoft द्वारा बनाया गया था और PowerPoint प्रस्तुति [.pps](/hi/presentation/pps) फ़ाइल सहित Microsoft उत्पादों द्वारा समर्थित है। फ़ाइल प्राथमिक उपयोग की नहीं है और मुख्य दस्तावेज़ या वेब पेज के साथ संलग्न दस्तावेज़ की तरह है। ओटीएफ फोंट के समान, ईओटी ग्लिफ़ के लिए पोस्टस्क्रिप्ट और ट्रू टाइप दोनों रूपरेखाओं का समर्थन करता है। ईओटी फाइलें आकार में छोटी होती हैं क्योंकि वे एलजेड संपीड़न का उपयोग करके संकुचित होती हैं। EOT मौजूदा TTF/OTF फ़ॉन्ट से फ़ॉन्ट बनाने के लिए Microsoft टूल का उपयोग करता है।

## संक्षिप्त इतिहास

EOT फॉन्ट को 2007 में CSS3 के हिस्से के रूप में W3C को सबमिट किया गया था, लेकिन रिमोट सिस्टम पर स्थायी रूप से स्थापित होने की इसकी आवश्यकताओं के कारण इसकी अस्वीकृति का कारण बन गया। इसे मार्च 2008 में फिर से सबमिट किया गया था, लेकिन W3C ने अंततः [वेब फॉन्ट फॉर्मेट](/hi/font/woff/) (WOFF) को चुना जिसे तब मानकीकृत किया गया था।

## ईओटी फ़ाइल प्रारूप

EOT फ़ाइल प्रारूप विवरण [W3 सबमिशन पृष्ठ](https://www.w3.org/Submission/EOT/#FileFormat) पर पाया जा सकता है और इस फ़ॉन्ट प्रारूप द्वारा उपयोग की जाने वाली संरचना को विस्तृत करता है। EOT में एक एकल EMBEDDEDFONT संरचना होती है जो hte फ़ॉन्ट नाम और समर्थित वर्णों के बारे में पर्याप्त बुनियादी जानकारी प्रदान करती है। इस जानकारी की पैकिंग उपयोगकर्ता एजेंटों को मशीन पर पहले से मौजूद होने पर फ़ॉन्ट को अनपैकिंग, डीकंप्रेसिंग या इंस्टॉल करने से बचने देती है।

### एम्बेडेड फ़ॉन्ट संरचना
प्रत्येक संशोधन के साथ संरचना के अंत में अतिरिक्त डेटा के अतिरिक्त, EMBEDDEDFONT संरचना में तीन संशोधन हुए हैं। EMBEDDEDFONT संरचना का अंतिम संशोधन नीचे दर्शाया गया है।

|डेटा प्रकार|प्रविष्टि का नाम|विवरण|
---|---|---|
|unsigned long|EOTSize|बाइट्स में कुल संरचना लंबाई (स्ट्रिंग और फ़ॉन्ट डेटा सहित)|
|अहस्ताक्षरित लंबा|FontDataSize|बाइट्स में ओपन टाइप फ़ॉन्ट (FontData) की लंबाई|
|अहस्ताक्षरित लंबा|संस्करण|इस प्रारूप का संस्करण संख्या - 0x00020002|
|अहस्ताक्षरित लंबा|झंडे|प्रसंस्करण झंडे|
|बाइट[10]|FontPANOSE|इस फ़ॉन्ट के लिए पैनोज़ मान - देखें http://www.microsoft.com/typography/otspec/os2.htm#pan|
|बाइट|चारसेट|विंडोज में यह TEXTMETRIC.tmCharSet से लिया गया है। यह मान फ़ॉन्ट के वर्ण सेट को निर्दिष्ट करता है। DEFAULT_CHARSET (0x01) कोई वरीयता नहीं दर्शाता है। - देखें http://msdn2.microsoft.com/en-us/library/ms534202.aspx|
|बाइट|इटैलिक|यदि ITALIC के लिए बिट OS/2.fsSelection में सेट है, तो मान 0x01 होगा - देखें http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|इस फ़ॉन्ट के लिए वजन मान - देखें http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|अहस्ताक्षरित लघु|fsType|फ्लैग टाइप करें जो एम्बेडिंग अनुमतियों के बारे में जानकारी प्रदान करते हैं - देखें http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|EOT फाइल के लिए मैजिक नंबर - 0x504C। डेटा भ्रष्टाचार की जांच के लिए उपयोग किया जाता है।|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (बिट्स 0-31) - देखें http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (बिट्स 32-63) - देखें http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (बिट्स 64-95) - देखें http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (बिट्स 96-127) - देखें http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (बिट्स 0-31) - देखें http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (बिट्स 32-63) - देखें http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - देखें http://www.microsoft.com/typography/otspec/head.htm|
|unsigned long|Reserved1|आरक्षित - 0 होना चाहिए|
|unsigned long|Reserved2|आरक्षित - 0 होना चाहिए|
|unsigned long|Reserved3|आरक्षित - 0 होना चाहिए|
|अहस्ताक्षरित लंबा|आरक्षित4|आरक्षित - 0 होना चाहिए|
| अहस्ताक्षरित लघु | पैडिंग 1 | लंबे संरेखण को बनाए रखने के लिए पैडिंग। पैडिंग मान हमेशा 0x0000 पर सेट होना चाहिए।|
|अहस्ताक्षरित लघु|FamilyNameSize|FamilyName सरणी द्वारा उपयोग किए जाने वाले बाइट्स की संख्या|
|बाइट|FamilyName[FamilyNameSize]|UTF-16 वर्णों की सरणी, FamilyNameSize बाइट्स की लंबाई। यह अंग्रेजी भाषा की फॉन्ट फैमिली स्ट्रिंग है जो फॉन्ट की नेम टेबल में पाई जाती है (नाम आईडी = 1) - देखें http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|Padding मान हमेशा 0x0000 पर सेट होना चाहिए।
|अहस्ताक्षरित लघु|StyleNameSize|StyleName द्वारा उपयोग किए गए बाइट्स की संख्या|
|बाइट|StyleName[StyleNameSize]|UTF-16 वर्णों की सरणी StyleNameSize बाइट्स की लंबाई है। यह अंग्रेजी भाषा का फॉन्ट सबफ़ैमिली स्ट्रिंग है जो फ़ॉन्ट की नाम तालिका में पाया जाता है (नाम आईडी = 2) - देखें http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|Padding मान हमेशा 0x0000 पर सेट होना चाहिए।
|unsigned short|VersionNameSize|VersionName द्वारा उपयोग किए गए बाइट्स की संख्या|
|bytes|VersionName[VersionNameSize]|UTF-16 वर्णों की सरणी, VersionNameSize बाइट्स की लंबाई। यह अंग्रेजी भाषा की संस्करण स्ट्रिंग है जो फ़ॉन्ट की नाम तालिका में पाई जाती है (नाम आईडी = 5) - देखें http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|Padding मान हमेशा 0x0000 पर सेट होना चाहिए।
|unsigned short|FullNameSize|FullName द्वारा उपयोग किए गए बाइट्स की संख्या|
|byte|FullName[FullNameSize]|UTF-16 वर्णों की सरणी FullNameSize बाइट्स की लंबाई है। यह अंग्रेजी भाषा का पूरा नाम स्ट्रिंग है जो फ़ॉन्ट की नाम तालिका में पाया जाता है (नाम आईडी = 4) - देखें http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|Padding मान हमेशा 0x0000 पर सेट होना चाहिए।
|अहस्ताक्षरित लघु|रूटस्ट्रिंगसाइज|रूटस्ट्रिंग सरणी द्वारा उपयोग किए जाने वाले बाइट्स की संख्या|
|बाइट|रूटस्ट्रिंग[रूटस्ट्रिंगसाइज]|यूटीएफ-16 वर्णों की सरणी रूटस्ट्रिंगसाइज बाइट्स की लंबाई।
|अहस्ताक्षरित लंबा|रूटस्ट्रिंगचेकसम|रूटस्ट्रिंग चेकसम मूल्य। नीचे रूटस्ट्रिंगचेकसम को संसाधित करने के लिए एल्गोरिदम देखें
|unsigned long|EUDCCodePage|EUDC फ़ॉन्ट समर्थन के लिए आवश्यक कोडपेज मान।|
|unsigned short|Padding6|Padding मान हमेशा 0x0000 पर सेट होना चाहिए।
|unsigned short|SignatureSize|Signature array द्वारा उपयोग किए जाने वाले बाइट्स की संख्या। वर्तमान में आरक्षित है और इसे 0x0000 पर सेट किया जाना चाहिए
|बाइट|हस्ताक्षर[हस्ताक्षर आकार]|वर्तमान में आरक्षित। अगर सिग्नेचर साइज 0x0000 है तो इस ऐरे की कोई लंबाई नहीं है
|अहस्ताक्षरित लंबा|EUDCFlags|ईयूडीसी फ़ॉन्ट के लिए प्रसंस्करण झंडे। विशिष्ट मान TTEMBED_XORENCRYPTDATA और TTEMBED_TTCOMPRESSED हो सकते हैं।
|unsigned long|EUDCFontSize|हस्ताक्षर सरणी द्वारा उपयोग किए गए बाइट्स की संख्या।|
|बाइट|EUDCFontData[EUDCFontSize]|ईयूडीसी फ़ॉन्ट डेटा के लिए प्रयुक्त बाइट्स की संख्या। यदि EUDCFontSize 0x00000000 है तो इस सरणी की कोई लंबाई नहीं है
|बाइट|FontData[FontDataSize]|इस ईओटी फ़ाइल के लिए फ़ॉन्ट डेटा। डेटा को संपीड़ित या XOR एन्क्रिप्टेड किया जा सकता है जैसा कि प्रसंस्करण झंडे द्वारा इंगित किया गया है

## संदर्भ

* [ईओटी फ़ाइल प्रारूप](https://www.w3.org/Submission/EOT/)
* [एम्बेडेड ओपन टाइप](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [फ़ॉन्ट एम्बेडिंग](https://en.wikipedia.org/wiki/Font_embedding)

