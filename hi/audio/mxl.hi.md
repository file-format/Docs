---
date: 2022-03-20
keywords: mxl, Musepack फ़ाइल स्वरूप, .mxl एक्सटेंशन
लेखक:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "MXL फ़ाइल स्वरूप और API के बारे में जानें जो MXL फ़ाइलें बना और खोल सकते हैं।"
title: MXL फ़ाइल स्वरूप - संपीड़ित MusicXML फ़ाइल
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## एमएक्सएल फाइल क्या है?

एक MXL फ़ाइल MusicXML फ़ाइल स्वरूप का संकुचित रूप है जो डिजिटल शीट संगीत के आदान-प्रदान के लिए एक खुला मानक प्रारूप है। सादा पाठ MusicXML फ़ाइलें आकार में बड़ी होती हैं और शीट वितरण प्रारूप के रूप में ऐसी फ़ाइलों का उपयोग बड़े फ़ाइल आकार से प्रभावित होता है। इस समस्या का समाधान [MusicXML](https://www.musicxml.com/) 2.0 के साथ MXL फ़ाइल स्वरूप की शुरुआत करके किया गया था जो फ़ाइलों को मूल MIDI फ़ाइलों के समान फ़ाइल आकार को कम करने के लिए पर्याप्त रूप से संपीड़ित करता है। एमएक्सएल फाइलों के लिए अनुशंसित मीडिया प्रकार application/vnd.recordare.musicxml है।

## एमएक्सएल फ़ाइल प्रारूप

MXL फाइलें [ZIP](/hi/compression/zip/) कंप्रेस्ड [XML](/hi/web/xml/) फाइलों के रूप में .mxl फाइल एक्सटेंशन के साथ स्टोर की जाती हैं। MXL फ़ाइलें [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt) में निर्दिष्ट के अनुसार DEFLATE एल्गोरिथम के साथ संपीड़ित होती हैं।

### एमएक्सएल फ़ाइल संरचना

प्रत्येक MXL फ़ाइल में एक ज़िप-आधारित XML प्रारूप होता है जिसमें एक META-INF/container.xml फ़ाइल होनी चाहिए जो फ़ाइल के MusicXML संस्करण के शुरुआती बिंदु का वर्णन करती है। MXL फ़ाइल स्वरूप के लिए परिभाषित कोई संगत .xsd फ़ाइल नहीं है।

एक साधारण कंटेनर.एक्सएमएल फ़ाइल में सामग्री इस प्रकार है। यह उदाहरण MakeMusic वेब साइट पर उपलब्ध Dichterliebe01.mxl फ़ाइल से लिया गया है।

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
इस उदाहरण में,<container> तत्व दस्तावेज़ तत्व है।<rootfiles> तत्व में एक या अधिक हो सकते हैं<rootfile> तत्वों, पहले . के साथ<rootfile> MusicXML रूट का वर्णन करने वाला तत्व। एक MusicXML फ़ाइल का उपयोग a . के रूप में किया जाता है<rootfile> हो सकता है<score-partwise> ,<score-timewise> , या<opus> इसके दस्तावेज़ तत्व के रूप में।

## संदर्भ

* [संपीड़ित MXL फ़ाइलें](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [आरएफसी 1951](https://www.ietf.org/rfc/rfc1951.txt)

