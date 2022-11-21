---
date: 2022-07-30
लेखक:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP फ़ाइल स्वरूप - JNP फ़ाइल क्या है?
linktitle: JNLP
description: "JNLP फ़ाइल स्वरूप और API के बारे में जानें जो JNLP फ़ाइलें बना और खोल सकते हैं।"
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## जेएनएलपी फाइल क्या है?

JNLP फ़ाइल एक जावा वेब स्टार्ट (JWS) फ़ाइल है जिसमें नेटवर्क पर जावा प्रोग्राम लॉन्च करने के लिए XML जानकारी होती है। यह जावा नेटवर्क लॉन्चिंग प्रोटोकॉल (जेएनएलपी) प्रारूप में सहेजा गया है। इसका उपयोग जावा वेब स्टार्ट (JWS) तकनीक द्वारा किया जाता है जो एक एप्लिकेशन को डाउनलोड करने और चलाने के लिए एक एप्लिकेशन परिनियोजन तकनीक है। एक जेएनएलपी फ़ाइल में सर्वर का दूरस्थ पता होता है जिससे प्रोग्राम डाउनलोड किया जाता है और स्थानीय मशीन पर लॉन्च किया जाता है।

## JNLP फ़ाइल स्वरूप - अधिक जानकारी

JNLP फ़ाइलें **[XML](/hi/web/xml/)** फ़ाइलों के रूप में सहेजी जाती हैं जो मानव-पठनीय पाठ प्रारूप में संग्रहीत होती हैं। XML फ़ाइल में वह जानकारी होती है जिसका उपयोग नेटवर्क पर जावा एप्लिकेशन को लॉन्च करने और निष्पादित करने के लिए किया जाता है। JWS आपको वेब पेज लिंक पर क्लिक करके एप्लिकेशन लॉन्च करने देता है। एप्लिकेशन को उपयोगकर्ता के कंप्यूटर पर पहले से डाउनलोड नहीं होने की स्थिति में डाउनलोड किया जाता है।

Java Platform Standard Edition (JSE) 9 की रिलीज़ के साथ Oracle ने JWS को पदावनत कर दिया। इसके साथ, JNLP फाइलें अब समर्थित नहीं हैं।

### जेएनएलपी फाइलें कैसे खोलें?

जो एप्लिकेशन **JNLP फ़ाइलें खोल सकते हैं** उनमें शामिल हैं **Microsoft विज़ुअल स्टूडियो कोड**, **नोटपैड**, **नोटपैड++**, **Oracle Java Web Start**, **Karakun OpenWebStart**, और * * गिटहब एटम **।

### जेएनएलपी फ़ाइल उदाहरण

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**उपयोग**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## जेएनएलपी फाइलें कैसे चलाएं?

JWS के बहिष्करण के साथ, JWS तकनीक पर आधारित एप्लिकेशन को Java के नवीनतम संस्करण के साथ नहीं चलाया जा सकता है। हालाँकि, ये JNLP आधारित प्रोग्राम OpenWebStart का उपयोग करके चलाए जा सकते हैं जो कि Java Web Start तकनीक का एक ओपन सोर्स रीइम्प्लीमेंटेशन है। यह जावा के नवीनतम संस्करण के समानांतर स्थापित होता है और जावा वेब स्टार्ट और जेएनएलपी मानक की सबसे अधिक उपयोग की जाने वाली सुविधाएँ प्रदान करता है।

## संदर्भ ##

* [जावा वेब स्टार्ट क्या है और इसे कैसे लॉन्च किया जाता है?](https://www.java.com/en/download/help/java_webstart.html)
* [जावा के नवीनतम संस्करण के साथ जेएनएलपी चलाएं] (https://openwebstart.com/)
* [जावा वेब स्टार्ट - विकिपीडिया] (https://en.wikipedia.org/wiki/Java_Web_Start)

