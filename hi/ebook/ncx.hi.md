{
  "date" : "2021-03-23",
  "keywords" :[ "एनसीएक्स", "ईपीयूबी नेविगेशन कंट्रोल एक्सएमएल फाइल", "एक्सटेंशन", "फॉर्मेट", "ई-बुक", "टीओसी", "डेज़ी कंसोर्टियम"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"EPUB नेविगेशन कंट्रोल XML फ़ाइल (NCX) फ़ाइल स्वरूप और API के बारे में जानें जो NCX फ़ाइलें बना और खोल सकते हैं।",
  "title" :"एनसीएक्स - ईपीयूबी नेविगेशन कंट्रोल एक्सएमएल फाइल",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## एनसीएक्स फाइल क्या है? ##

NCX फ़ाइल को XML के लिए नेविगेशन कंट्रोल फ़ाइल के रूप में संक्षिप्त किया जाता है, जिसे आमतौर पर toc.ncx नाम दिया जाता है। इस फ़ाइल में EPUB फ़ाइल के लिए सामग्री की श्रेणीबद्ध तालिका शामिल है। एनसीएक्स के लिए विनिर्देश डिजिटल टॉकिंग बुक (डीटीबी) के लिए विकसित किया गया था और यह फ़ाइल प्रारूप **डेज़ी कंसोर्टियम** द्वारा बनाए रखा गया है और यह ईपीयूबी विनिर्देश का हिस्सा नहीं है। NCX फ़ाइल में एक माइम-प्रकार का **application/x-dtbncx+xml** शामिल है।

## एनसीएक्स विशिष्टता ##

NCX फ़ाइल में विभिन्न प्रकार के XML टैग होते हैं। आईडी का उल्लेख करने के लिए मेटा टैग जैसे `मेटा नाम = "डीटीबी: यूआईडी" का उपयोग किया जाता है। `मेटा नाम = "dtb: गहराई"` तत्व `navMap` टैग तत्व की गहराई के बराबर सेट है। सामग्री की एक श्रेणीबद्ध तालिका बनाने के लिए `नेवपॉइंट` तत्वों को नेस्ट किया जा सकता है। `navLabel` की सामग्री वह पाठ है जो .ncx का उपयोग करने वाले रीडिंग सिस्टम द्वारा उत्पन्न सामग्री की तालिका में दिखाई देता है। `नेवपॉइंट` तत्व की सामग्री मेनिफेस्ट में सूचीबद्ध सामग्री दस्तावेज़ की ओर इशारा करती है और इसमें एक तत्व पहचानकर्ता भी शामिल हो सकता है

ईपीयूबी में उपयोग किए गए एनसीएक्स विनिर्देश के कुछ अपवादों का विवरण। यहां आप एनसीएक्स फ़ाइल का उदाहरण देख सकते हैं:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## संदर्भ ##

* [विकिपीडिया से EPUB](https://en.wikipedia.org/wiki/EPUB)
* [toc.ncx में कौन सी फाइलें शामिल करें](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

