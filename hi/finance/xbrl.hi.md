{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "xbrl फ़ाइल", "xbrl फ़ाइल स्वरूप", "xbrl फ़ाइल प्रकार", "फ़ाइल", "प्रकार", "xbrl फ़ाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - व्यापार और वित्तीय रिपोर्टिंग फ़ाइल स्वरूप",
  "description":"XBRL फ़ाइल स्वरूप और API के बारे में जानें जो XBRL फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## एक्सबीआरएल फाइल क्या है?

.xbrl (एक्स्टेंसिबल बिजनेस रिपोर्टिंग लैंग्वेज) एक्सटेंशन वाली फाइल व्यावसायिक सूचनाओं के आदान-प्रदान के लिए एक स्वतंत्र रूप से उपलब्ध और वैश्विक ढांचा है। यह अब व्यापक रूप से एक मानक प्रारूप के रूप में उपयोग किया जाता है जिसने पुराने पेपर-आधारित रिपोर्टों को अधिक उपयोगी और सटीक डिजिटल रिकॉर्ड के साथ बदल दिया है। एक्सबीआरएल फाइलों का उपयोग करके आदान-प्रदान किए गए डेटा में बहीखाता, वित्तीय विवरण और बैलेंस शीट शामिल हैं। यह डेटा टैग का समर्थन करता है जो डेटा प्रोसेसिंग को सभी प्रकार की व्यावसायिक जानकारी के विश्लेषण चरण तक तैयार करने की अनुमति देता है। XBRL फाइलें Rivet Software Dragon View XBRL Viewer और APIs [Aspose.Finance](https://products.aspose.com/finance) जैसे सॉफ़्टवेयर का उपयोग करके खोली जा सकती हैं।

## एक्सबीआरएल फ़ाइल प्रारूप

एक्सबीआरएल डिजिटल व्यापार रिपोर्टिंग के लिए एक खुला अंतरराष्ट्रीय मानक है जिसका व्यापक रूप से विश्व स्तर पर उपयोग किया जाता है। यह एक [XML](/hi/web/xml/) आधारित भाषा है जो रिपोर्ट सॉर्टिंग और विश्लेषण के लिए डेटा तैयार करने के लिए व्यावसायिक डेटा के प्रत्येक आइटम का वर्णन करने के लिए XBRL तत्वों का उपयोग करती है, जिन्हें टैग के रूप में जाना जाता है। XBRL फ़ाइल प्रारूप विनिर्देशों को वर्तमान में [XBRL संस्करण 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) के साथ एक्सबीआरएल इंटरनेशनल, इंक द्वारा विकसित और प्रकाशित किया गया है। उपयोगकर्ताओं के लिए उपलब्ध है।

### एक्सबीआरएल दस्तावेज़ संरचना

[XBRL 2.1 टैग] के बारे में पूरी जानकारी (https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) को प्रोग्रामर्स द्वारा इस फाइल फॉर्मेट में काम करने के लिए एप्लीकेशन लिखने के लिए रेफर किया जा सकता है। एक एक्सबीआरएल में एक एक्सबीआरएल इंस्टेंस और टैक्सोनॉमी का एक संग्रह होता है।

**`एक्सबीआरएल इंस्टेंस'** - एक्सबीआरएल इंस्टेंस की शुरुआत होती है<xbrl> मूल तत्व। एक बड़े XML दस्तावेज़ में एक से अधिक XBRL इंस्टेंस शामिल हो सकते हैं।

**`XBRL टैक्सोनॉमी`** - [XBRL टैक्सोनॉमी](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +rected-errata-2013-02-20.html#_5) को XML स्कीमा संरचना के रूप में परिभाषित किया गया है और सीधे संदर्भित बाहरी लिंक तत्व का सेट है। लिंकबेस संदर्भों को दर्शाने वाला एक स्केलेबल टैक्सोनॉमी स्कीमा इस प्रकार है।

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## संदर्भ ##

* [एक्सबीआरएल - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/XBRL)
* [एक्सटेंसिबल बिजनेस रिपोर्टिंग लैंग्वेज (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- इरेटा-2013-02-20.html)

