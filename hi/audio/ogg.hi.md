---
date: 2019-12-13
keywords: ogg, ogg फ़ाइल स्वरूप, .ogg एक्सटेंशन, ogg ऑडियो प्रारूप
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "OGG फ़ाइल स्वरूप और API के बारे में जानें जो OGG फ़ाइलें बना और खोल सकते हैं।"
title: OGG फ़ाइल - Ogg Vorbis ऑडियो फ़ाइल
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## ओजीजी फाइल क्या है?

OGG एक Ogg Vorbis संपीड़ित ऑडियो फ़ाइल है जिसे .ogg एक्सटेंशन के साथ सहेजा जाता है। OGG फ़ाइलें ऑडियो डेटा संग्रहीत करने के लिए उपयोग की जाती हैं और इसमें कलाकार और ट्रैक जानकारी और मेटाडेटा भी शामिल हो सकते हैं। OGG एक स्वतंत्र और खुला कंटेनर प्रारूप है जिसका रखरखाव Xiph.Org Foundation द्वारा किया जाता है।

## ओजीजी फ़ाइल प्रारूप का संक्षिप्त इतिहास

Ogg प्रोजेक्ट 1993 में एक बड़े प्रोजेक्ट के एक हिस्से के रूप में शुरू हुआ और इसका नाम स्क्विश रखा गया लेकिन एक मौजूदा ट्रेडमार्क के कारण, इसका नाम बदलकर OggSquish कर दिया गया। इसे आधुनिक ऑडियो अनुप्रयोगों के लिए एक लचीला संपीड़ित ऑडियो प्रारूप बनाने के प्रयास के रूप में वर्णित किया गया था। ओजीजी संदर्भ 2 सितंबर 2000 को वोरबिस से अलग किया गया था।

ओजीजी में औपचारिक वीडियो समर्थन की कमी के कारण 2002 में ओजीएम बनाया गया था। इसने माइक्रोसॉफ्ट डायरेक्टशो फ्रेमवर्क से वीडियो को ओजीजी-आधारित रैपर में एम्बेड करने की अनुमति दी। 2006 तक, OGG को कई वीडियो गेम इंजनों द्वारा समर्थित किया गया था और आमतौर पर इसका उपयोग मुफ्त सामग्री को एन्कोड करने के लिए किया जाता था। एमपी3 के बेहतर विकल्प के रूप में वोरबिस के उपयोग को बढ़ाने के लिए फ्री सॉफ्टवेयर फाउंडेशन ने 15 मई, 2007 को एक अभियान शुरू किया। 30 जून 2009 तक, OGG एकमात्र कंटेनर प्रारूप था जो Firefox 3.5 के HTML5 कार्यान्वयन द्वारा समर्थित था।

## ओजीजी फ़ाइल प्रारूप

OGG प्रारूप में डेटा के टुकड़े होते हैं। प्रत्येक खंड को ओग पृष्ठ कहा जाता है। प्रत्येक पृष्ठ Ogg प्रारूप की पहचान करने के लिए "OggS" से शुरू होता है। शीर्षलेख में क्रमांक और पृष्ठ संख्या होती है जो प्रत्येक पृष्ठ को एक श्रृंखला के एक भाग के रूप में पहचानती है। पृष्ठ में निम्नलिखित घटक होते हैं।

- **पेज हैडर**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| बिट | मूल्य | विवरण |
| --- | --- | --- |
| 0 | 0x01 | इंगित करता है कि पृष्ठ का पहला पैकेट तार्किक बिटस्ट्रीम में पिछले पैकेट की निरंतरता है। |
| 1 | 0x02 | इंगित करता है कि यह पृष्ठ तार्किक बिटस्ट्रीम में पहला है। |
| 2 | 0x04 | इंगित करता है कि यह पृष्ठ तार्किक बिटस्ट्रीम में अंतिम है। |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **मेटाडेटा**: VorbisComment मेटाडेटा को संग्रहीत करने के लिए सबसे व्यापक रूप से समर्थित तंत्र है। अन्य तंत्रों में निम्नलिखित शामिल हैं:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## संदर्भ ##

- [ओजीजी - विकिपीडिया](https://en.wikipedia.org/wiki/Ogg)

