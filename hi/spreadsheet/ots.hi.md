{
  "date" : "2019-12-16",
  "keywords" :["ओटीएस", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "एक्सेल", "स्प्रेडशीट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"OTS फ़ाइल स्वरूप और API के बारे में जानें जो OTS फ़ाइलें बना और खोल सकते हैं।",
  "title" :"OTS - OpenDocument स्प्रेडशीट टेम्पलेट फ़ाइल स्वरूप",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## ओटीएस फाइल क्या है?

.ots एक्सटेंशन वाली फ़ाइल एक OpenDocument स्प्रेडशीट टेम्प्लेट फ़ाइल है जिसे Apache OpenOffice में शामिल Calc एप्लिकेशन सॉफ़्टवेयर के साथ बनाया गया है। कैल्क एप्लीकेशन सॉफ्टवेयर माइक्रोसॉफ्ट ऑफिस में उपलब्ध एक्सेल के समान है। ओटीएस फ़ाइल स्वरूप का उपयोग टेम्प्लेट बनाने के लिए किया जाता है जिसमें शैलियों, फ़ॉन्ट, डेटा, स्प्रेडशीट लेआउट और स्वरूपण से संबंधित पूर्वनिर्धारित सेटिंग्स होती हैं। ओटीएफ फाइलों में 'माइम-टाइप एप्लिकेशन/vnd.oasis.opendocument.spreadsheet-template' होता है। [ODS फ़ाइल स्वरूप](/hi/spreadsheet/ods/) में सहेजी गई वास्तविक डेटा फ़ाइलों को उत्पन्न करने और सहेजने के लिए इन टेम्प्लेट फ़ाइलों का उपयोग शुरुआती बिंदु के रूप में किया जा सकता है। OTS फ़ाइलों का उपयोग OpenOffice और LibreOffice जैसे अनुप्रयोगों के साथ किया जा सकता है।

## ओटीएस फ़ाइल स्वरूप

OTS फ़ाइलें OASIS के OpenDocument XML-आधारित फ़ाइल स्वरूप में सहेजी जाती हैं, जिसमें [ZIP](/hi/compression/zip/) संग्रह के रूप में एक पैकेज के साथ कई उप-दस्तावेज़ों का संग्रह शामिल होता है। प्रत्येक ज़िप संग्रह संपूर्ण दस्तावेज़ का हिस्सा संग्रहीत करता है और प्रत्येक उप-दस्तावेज़ दस्तावेज़ के एक विशेष पहलू को संग्रहीत करता है। उदाहरण के लिए, एक उप-दस्तावेज़ में शैली की जानकारी होती है और दूसरे उप-दस्तावेज़ में दस्तावेज़ की सामग्री होती है। एक विशिष्ट ओडीएफ दस्तावेज़ में निम्नलिखित घटक होते हैं:

### ओटीएस कंटेंट.एक्सएमएल

Content.xml फ़ाइल में दस्तावेज़ की वास्तविक सामग्री होती है। हालांकि इसमें छवियों जैसे बाइनरी डेटा शामिल नहीं हैं।
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### OTS फ़ाइल स्वरूप की Styles.xml

Styles.xml फ़ाइल में स्टाइलिंग जानकारी होती है और इसका उपयोग फ़ॉर्मेटिंग और लेआउट के लिए भारी मात्रा में किया जाता है। शैलियों के प्रकारों में शामिल हैं:

* अनुच्छेद शैलियों
* पृष्ठ शैलियाँ
* चरित्र शैली
* फ्रेम शैलियों
* सूची शैलियों

### मेटा.एक्सएमएल

मेटा.एक्सएमएल फ़ाइल में फ़ाइल मेटाडेटा जैसे लेखक, अंतिम संशोधित तिथि आदि के बारे में जानकारी होती है।
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### सेटिंग्स.xml

`सेटिंग्स.एक्सएमएल` फ़ाइल में दस्तावेज़ स्तर की सेटिंग्स जैसे ज़ूम कारक और कर्सर की स्थिति शामिल है।

## संदर्भ ##

* [OpenDocument 1.2 विशिष्टता](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/OpenDocument)

