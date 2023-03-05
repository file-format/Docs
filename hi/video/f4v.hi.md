---
date: 2019-10-11
keywords: f4v, .f4v, f4v फ़ाइल स्वरूप, .f4v फ़ाइल स्वरूप, .f4v विस्तार, f4v विस्तार, f4v वीडियो प्रारूप, f4v फ़ाइलें कैसे खोलें, f4v फ़ाइलें क्या हैं
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "F4V फ़ाइल स्वरूप और API के बारे में जानें जो F4V फ़ाइलें बना और खोल सकते हैं"
title: F4V फ़ाइल स्वरूप
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## F4V फ़ाइल क्या है? ##

F4V (फ़्लैश MP4 वीडियो फ़ाइल) एक वीडियो फ़ाइल है जिसे .f4v एक्सटेंशन के साथ सहेजा गया है। यह ISO बेस मीडिया फाइल फॉर्मेट (MPEG-4 पार्ट 12) पर आधारित है। यह [MP4](/hi/video/mp4/) के समान है, इसलिए इसे अनौपचारिक रूप से फ्लैश MP4 भी कहा जाता है। [FLV](/hi/video/flv/) की H.264/ACC सामग्री को स्ट्रीम करने की सीमाएँ थीं, जिसके परिणामस्वरूप Adobe सिस्टम्स ने नया F4V प्रारूप तैयार किया। फ़्लैश प्लेयर 9 अपडेट 3 के रिलीज़ होने के बाद से फ़्लैश प्लेयर F4V फ़ाइलें चला सकता है।

## F4V फाइलों की संरचना ##

F4V फ़ाइल स्वरूप ISO बेस मीडिया फ़ाइल स्वरूप (MPEG-4 भाग 12) पर आधारित है और MP4 प्रारूप के समान है। संरचना के बारे में विवरण के लिए, कृपया [MP4](/hi/video/mp4/) पृष्ठ देखें। F4V और MP4 के बीच प्रमुख अंतर मेटाडेटा प्रारूप है जिसे F4V स्टोर कर सकता है। F4V प्रारूप द्वारा समर्थित मेटाडेटा प्रारूपों की सूची नीचे दी गई है।

- **टैग बॉक्स**: मूवी (मूव) बॉक्स के भीतर अतिरिक्त चार वैकल्पिक टैग बॉक्स (प्रमाणीकरण, शीर्षक, डीएससीपी, सीपीआरटी)।
- **XMP मेटाडेटा बॉक्स**: यह बॉक्स मूवी (moov) बॉक्स के ठीक बाद आता है। इसके साथ, फ़ाइल एक्शनस्क्रिप्ट के माध्यम से एक्सएमपी मेटाडेटा को एक एसडब्ल्यूएफ मूवी में संचार कर सकती है।
- **इलस्ट बॉक्स**: यह बॉक्स मेटा (मेटा) बॉक्स के अंदर होता है और इसमें कई मेटाडेटा टैग हो सकते हैं। समर्थित डेटा प्रकार नीचे दिए गए हैं।
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **टेक्स्ट ट्रैक मेटाडेटा बॉक्स**: मीडिया डेटाबॉक्स (mdat) के अंदर टेक्स्ट सैंपल (टेक्स्ट या tx3g)। इसमें निम्नलिखित मेटाडेटा बॉक्स हो सकते हैं।
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## संदर्भ ##

- [फ्लैश वीडियो - विकिपीडिया](https://en.wikipedia.org/wiki/Flash_Video)

