---
date: 2019-12-13
keywords: flac, flac फ़ाइल स्वरूप, .flac एक्सटेंशन, flac फ़ाइल, flac बनाम mp3
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLAC फ़ाइल स्वरूप और API के बारे में जानें जो FLAC फ़ाइलें बना और खोल सकते हैं।"
title: एफएलएसी फ़ाइल प्रारूप
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## एफ़एलएसी फ़ाइल क्या है?

FLAC (फ्री लॉसलेस ऑडियो कोडेक) Xiph.Org Foundation द्वारा विकसित एक दोषरहित संपीड़न ऑडियो कोडिंग प्रारूप है। FLAC एक रॉयल्टी-मुक्त खुला प्रारूप है जिसे .flac एक्सटेंशन के साथ सहेजा जाता है। FLAC एल्गोरिथम का उपयोग करके संपीड़ित डिजिटल ऑडियो आमतौर पर आकार में 50 से 70 प्रतिशत तक कम हो जाता है। FLAC फाइलों को मूल ऑडियो फाइलों की एक समान कॉपी में डीकंप्रेस किया जा सकता है।

## एफएलएसी फ़ाइल प्रारूप

यह FLAC बिटस्ट्रीम का एक सिंहावलोकन है।

- **fLaC मार्कर**: यह मार्कर स्ट्रीम की शुरुआत में जोड़ा जाता है। इसके बाद एक या अधिक मेटाडेटा ब्लॉक होते हैं।
- **मेटाडेटा ब्लॉक**: 128 प्रकार के मेटाडेटा ब्लॉक FLAC द्वारा समर्थित हैं; वर्तमान में निम्नलिखित परिभाषित हैं।
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **फ्रेम**: ऑडियो डेटा एक या अधिक ऑडियो फ्रेम से बना होता है।
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## FLAC फ़ाइल स्वरूप का संक्षिप्त इतिहास

जोश कोलसन ने 2000 में FLAC का विकास शुरू किया। FLAC का पहला संस्करण 20 जुलाई 2001 को जारी किया गया था। FLAC को Xiph.Org ध्वज के तहत 20 जनवरी 2003 को शामिल किया गया था। FLAC के विकास को Xiph.Org git रिपॉजिटरी में स्थानांतरित कर दिया गया था। 26 मार्च 2013 को संस्करण 1.3.0 का विमोचन।

## एफएलएसी परियोजना की संरचना

FLAC परियोजना में निम्नलिखित शामिल हैं:

- स्ट्रीम प्रारूप।
- स्ट्रीम के लिए सरल कंटेनर प्रारूप (FLAC)।
- libFLAC: संदर्भ एन्कोडर, डिकोडर और मेटाडेटा इंटरफ़ेस की एक लाइब्रेरी।
- libFLAC++: libFLAC के लिए एक वस्तु-उन्मुख आवरण।
- flac: FLAC धाराओं को एन्कोड और डिकोड करने के लिए एक कमांड-लाइन प्रोग्राम।
- मेटाफ्लेक: FLAC के लिए एक कमांड-लाइन मेटाडेटा संपादक।
- Winamp, XMMX, आदि जैसे संगीत खिलाड़ियों के लिए इनपुट प्लगइन्स।
- Ogg कंटेनर प्रारूप (Ogg FLAC)।

## एफएलएसी डिजाइन

संगीत के घनत्व और आयाम के आधार पर, संपीड़ित फ़ाइल का आकार मूल फ़ाइल से 80% कम हो सकता है।

### स्रोत एनकोडर ###

- यह केवल पूर्णांक नमूनों का समर्थन करता है न कि फ़्लोटिंग-पॉइंट का। यह पीसीएम बिट रेजोल्यूशन को 4 से 32 बिट प्रति नमूना और नमूना दर 1 हर्ट्ज से 65,535 हर्ट्ज तक संभाल सकता है। FLAC एन्कोडिंग प्रति नमूना 24 बिट तक सीमित है।
- संपीड़न बढ़ाने के लिए इंटरचैनल सहसंबंधों का लाभ उठाने के लिए चैनलों को समूहीकृत किया जा सकता है।
- CRC चेकसम का उपयोग दूषित फ़्रेमों की पहचान करने के लिए किया जाता है।
- ऑडियो नमूनों के रूपांतरण के लिए, FLAC रैखिक पूर्वानुमान का उपयोग करता है।

### मेटाडेटा ###

- FLAC रिप्लेगैन का समर्थन करता है (ऑडियो में लाउडनेस को समझने और सामान्य करने के लिए उपयोग किया जाता है)।
- एफएलएसी उसी प्रणाली का उपयोग करता है जिसका उपयोग वोरबिस टिप्पणियों में टैगिंग के लिए किया जाता है।
- libFLAC का उपयोग अधिकांश FLAC एप्लिकेशन द्वारा एन्कोडिंग/डिकोडिंग के लिए किया जाता है।
- libFLAC API को बेस FLAC बिटस्ट्रीम से एब्स्ट्रैक्शन बढ़ाने के लिए स्ट्रीम, सीकेबल स्ट्रीम और फाइलों में व्यवस्थित किया गया है।

### संपीड़न ###

libFLAC 0 से 8 तक संपीड़न स्तरों का उपयोग करता है जहां 0 सबसे तेज़ है और 8 सबसे धीमा संपीड़न स्तर है। संपीड़ित फ़ाइलें हमेशा दोषरहित होती हैं, हालांकि ट्रेडऑफ़ गति और आकार के बीच होती है।

## एफएलएसी बनाम एमपी3
MP3 एक हानिपूर्ण संपीड़न प्रारूप है जिसका अर्थ है कि यह संपीड़न लागू करने के बाद अपने आकार को कम करने के लिए ऑडियो के कुछ हिस्से को काट सकता है। जबकि, FLAC एक दोषरहित फ़ाइल स्वरूप है जिसका अर्थ है कि आप ऑडियो को उसके शुद्धतम रूप में सुनने में सक्षम हैं। पहले दोषरहित फ़ाइल स्वरूप CDA या WAV थे जो FLAC की तरह अधिक स्थान कुशल नहीं थे। निम्न तालिका कुछ महत्वपूर्ण शब्दों के लिए इन दो प्रारूपों के बीच तुलना दिखाएगी:

|टर्म|FLAC|MP3|
---|---|---|
|**डेटा गुणवत्ता**|ऑडियो डेटा का कोई नुकसान नहीं| ऑडियो डेटा को संपीड़ित करते समय कुछ डेटा खो सकता है|
|**आकार**|हानिकारक प्रारूपों की तुलना में बड़ा फ़ाइल आकार। तो बड़ी भंडारण क्षमता की जरूरत है| छोटे फ़ाइल आकार, छोटे भंडारण स्थान के साथ कॉम्पैक्ट ऑडियो उपकरणों पर चलाने के लिए उपयुक्त |
|**हार्डवेयर आवश्यकताएं**| उच्च गुणवत्ता वाले ऑडियो गियर और विशाल भंडारण क्षमता की आवश्यकता है। विशाल ऑडियो पुस्तकालयों को एक छोटे भंडारण स्थान में सहेजा जा सकता है। ऑडियो प्लेयर या मोबाइल फोन जैसे हैंडहेल्ड डिवाइस के लिए उपयुक्त|
|**इंटरनेट पर वितरण**|बड़े फ़ाइल आकार के कारण इंटरनेट पर आसानी से वितरित नहीं किया जा सकता |कॉम्पैक्ट फ़ाइल आकार इंटरनेट पर वितरित करना आसान बनाता है|
|**संगतता**|सबसे लोकप्रिय संगीत और ऑडियो सुनने वाला कोडेक जो ग्रह पर हर डिवाइस के साथ काफी संगत है, नई पीढ़ी के पीसी, फोन, एवी रिसीवर, ब्लू-रे प्लेयर, स्ट्रीमिंग डिवाइस जैसे रोकू या फायर टीवी के साथ संगत है|

## संदर्भ ##

- [एफएलएसी - विकिपीडिया](https://en.wikipedia.org/wiki/FLAC)
