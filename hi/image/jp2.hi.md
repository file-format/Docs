{
  "date" : "2019-10-11",
  "keywords" :["jp2 फाइल", "jp2 फाइल फॉर्मेट", "jp2 फाइल क्या है", "फाइल", "jp2 उदाहरण", "jp2 फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - छवि फ़ाइल स्वरूप",
  "description":"JP2 फ़ाइल स्वरूप और API के बारे में जानें जो JP2 फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## JP2 फ़ाइल क्या है? ##

JPEG 2000 (**JP2**) एक इमेज कोडिंग सिस्टम और अत्याधुनिक इमेज कंप्रेशन मानक है। दोषरहित सामग्री को एक बार में किसी भी गुणवत्ता में कोडित करने के लिए यह वेवलेट तकनीक का उपयोग करता है। इसके अलावा, कोडिंग दक्षता में किसी भी पर्याप्त दंड के बिना, JPEG 2000 में एक ही सामग्री को विभिन्न प्रकार के अन्य प्रस्तावों और गुणों में प्रभावशाली ढंग से एक्सेस और डिकोड करने की क्षमता है। जेपीईजी 2000 में कोड धाराएं उल्लेखनीय रूप से स्केलेबल हैं, जिसमें रुचि के क्षेत्र हैं जो स्थानिक रैंडम एक्सेस की सुविधा प्रदान करते हैं।

जेपीईजी 2000 सबसे स्केलेबल मानक में से एक है। एक छवि के विभिन्न भागों को विविध गुणों का उपयोग करके संग्रहीत किया जा सकता है। कोड स्ट्रीम को विभिन्न तरीकों से क्रमित करके एक उल्लेखनीय प्रदर्शन वृद्धि प्राप्त की जा सकती है। फिर भी, JP2 को इस लचीलेपन के परिणाम के रूप में जटिल और कम्प्यूटेशनल रूप से चुनौतीपूर्ण एनकोडर/डिकोडर की आवश्यकता होती है। जेपीईजी की तुलना में, जेपीईजी 2000 केवल रिंगिंग कलाकृतियों का उत्पादन करता है जो छवि किनारे के पास रिंग बनाता है और धुंधला हो सकता है, जबकि जेपीईजी 8 × 8 विज़ुअल आर्टिफैक्ट ब्लॉक का उपयोग करता है जो रिंगिंग और ब्लॉकिंग आर्टिफैक्ट दोनों हो सकते हैं। टेरापिक्सल में आयामों के साथ 16384 विविध घटकों को रखना, और सटीकता जो 38 बिट/नमूना के रूप में उच्च हो सकती है।

## इतिहास ##

2000 में, संयुक्त फोटोग्राफिक विशेषज्ञ समूह समिति ने JP2 को इस नए वेवलेट-आधारित पद्धति के साथ अपने स्वयं के असतत कोसाइन ट्रांसफ़ॉर्म-आधारित JPEG मानक में सुधार करने के उद्देश्य से डिज़ाइन किया। JPEG समिति का लक्ष्य उनके आधारभूत तरीकों को लाइसेंस शुल्क से मुक्त करना था। JP2 लाइसेंस प्राप्त करने वाली 20 कंपनियों के बीच प्रतिस्पर्धा में, वे बहुत कम अंतर से जीते। जेपीईजी 2000 को आईएसओ मानक के रूप में घोषित किया गया है, हालांकि अधिकांश वेब ब्राउज़र 2017 से जेपीईजी 2000 को हाथ देने के लिए तैयार नहीं हैं।

## JPEG 2000 इमेज कोडिंग सिस्टम ## के भाग

निम्नलिखित मुख्य भाग हैं जो JPEG 2000 के लिए मानकों के पूर्ण सूट का निर्माण करते हैं।


|भाग|शीर्षक|विवरण|संख्या
---|---|---|---|
|भाग 1|कोर कोडिंग सिस्टम| कोड स्ट्रीम के सिंटैक्स को परिभाषित करता है। जेपीईजी 2000 छवियों को डिकोड करने में शामिल विभिन्न चरण। प्रदान किए जाने वाले मूल फ़ाइल स्वरूप JP2, मेटाडेटा, और IP अधिकारों की व्याख्या करता है।|ISO/IEC 15444-1
|भाग 2|एक्सटेंशन|फ़ाइल स्वरूप कोड स्ट्रीम के लिए एक्सटेंशन को परिभाषित करता है और एचडीआर नमूना प्रदर्शन, रंग स्थान विनिर्देश, क्रॉपिंग, ज्यामितीय रूपांतरण की अनुमति देता है; विविध एनिमेशन, मेटाडेटा, और एकाधिक कोड स्ट्रीम।|ISO/IEC 15444-2
|भाग 3|मोशन जेपीईजी 2000 (एमजे2 या एमजेपी2)|मोशन सीक्वेंस के लिए एक फाइल फॉर्मेट पेश करें, एक स्वतंत्र कोड स्ट्रीम में छवियों को एन्कोडिंग करें।|आईएसओ/आईईसी 15444-3
|भाग 4|अनुरूपता|एन्कोडिंग और डिकोडिंग के लिए परीक्षण तकनीकों को बताता है और दोनों नंगे कोड स्ट्रीम और जेपी2 फाइलों के लिए फाइलों की जांच करता है।|आईएसओ/आईईसी 15444-4
|भाग 5|संदर्भ सॉफ्टवेयर|दो स्रोत कोड पैकेज (जावा, सी) शामिल हैं जो कोर कोडिंग प्रणाली को लागू करते हैं और ओपन-सोर्स लाइसेंस के तहत उपलब्ध हैं।|आईएसओ/आईईसी 15444-5
|भाग 6|मिश्रित छवि फ़ाइल स्वरूप|जेपीएम फ़ाइल प्रारूप को परिभाषित करता है और फ़ैक्स-जैसे अनुप्रयोगों के लिए बहु-पृष्ठ दस्तावेज़ इमेजिंग की अनुमति देता है। JBIG2 और JPEG.|ISO/IEC 15444-6 के उपयोग का समर्थन करता है
|भाग 8|जेपीईजी 2000 सुरक्षित (जेपीएसईसी)|लेन-देन, सामग्री और प्रौद्योगिकियों की सुरक्षा सुनिश्चित करता है, और सुरक्षित जेपीईजी 2000 बिट स्ट्रीम की अनुमति देता है।|आईएसओ/आईईसी 15444-8
|भाग 9|जेपीआईपी|मेटाडेटा और इमेजरी तक पहुंच के लिए एक नेटवर्क वातावरण में उपकरणों को परिभाषित करता है, और इंटरएक्टिव और कुशल प्रोटोकॉल बताता है|आईएसओ/आईईसी 15444-9
|भाग 10|JP3D|भाग 1 का आयतनात्मक विस्तार और Z आयाम का परिचय देता है। टाइल्स, कोड-ब्लॉक, परिसर, और 3डी क्षेत्र-की-रुचि पहुंच योग्यता सुविधाओं की अवधारणा का विस्तार करता है।|ISO/IEC 15444-10
|भाग 11|JPWL|त्रुटि-प्रवण वायरलेस नेटवर्क पर सुव्यवस्थित प्रसारण से संबंधित है। यह एक्सटेंशन डिकोडर्स|ISO/IEC 15444-11 के साथ संगत है
|भाग 13|प्रवेश-स्तर एनकोडर|कोर कोडिंग सिस्टम के प्रवेश स्तर के एनकोडर कार्यान्वयन को परिभाषित करता है।|ISO/IEC 15444-13
|भाग 14|जेपीएक्सएमएल|एक्सएमएल में एक प्रतिनिधित्व और इमेजरी के आंतरिक डेटा तक पहुंचने के लिए मार्कर सेगमेंट और विधियों की व्याख्या करता है।|आईएसओ/आईईसी 15444-14
|भाग 15|HTJ2K (अंडर-डेवलपमेंट)|एक वैकल्पिक ब्लॉक कोडिंग एल्गोरिदम निर्दिष्ट करता है। एल्गोरिथ्म दस गुना बढ़ा हुआ थ्रूपुट और दोषरहित कोडिंग/डिकोडिंग प्रदान करता है

## JP2 फ़ाइल स्वरूप ##

जेपीईजी 2000 फ़ाइल प्रारूप के साथ-साथ कोड स्ट्रीम को जेपीईजी -1 के समान ही परिभाषित करता है। हालाँकि छवि के नमूने विशेष रूप से JPEG 2000 द्वारा वर्णित हैं, फिर भी JPEG-1 में रंग स्थान और छवि को एन्कोड करने के लिए आवश्यक रिज़ॉल्यूशन के बारे में अन्य अतिरिक्त जानकारी शामिल है। यदि छवि को JPEG 2000 फ़ाइल के रूप में संग्रहीत किया जाता है, तो **.jp2** का उपयोग एक्सटेंशन के रूप में किया जाता है। यह फ़ाइल प्रारूप JPEG 2000 पार्ट-2 एक्सटेंशन द्वारा और बेहतर होता है, जो एनीमेशन तंत्र और कई कोड स्ट्रीम के कॉन्फ़िगरेशन को एक ही छवि में परिभाषित करता है। **.jpx** एक्सटेंशन का उपयोग तब किया जाता है जब छवियां इस विस्तारित फ़ाइल-प्रारूप का उपयोग करके सहेजती हैं। चूंकि कोड-स्ट्रीम डेटा को मुख्य रूप से फाइलों में सहेजा नहीं माना जाता है, इसलिए इस उद्देश्य के लिए कोई मानक विस्तार परिभाषित नहीं किया गया है। हालांकि परीक्षण उद्देश्यों के लिए, इसे अक्सर **.jpc** या **.j2k** एक्सटेंशन मिलता है। JPEG-1 के विपरीत, JPEG 2000 XML स्वरूप में मेटाडेटा को एनकोड करने का एक अलग तरीका चुनता है। मानक 12234-1.4 (ISO TC42 समिति द्वारा) का उपयोग Exif टैग और XML घटकों के बीच संदर्भ के रूप में किया जाता है। जेपीईजी 2000 में एक आईएसओ मानक, एक्सएमपी हो सकता है।

### हिस्सा ###
जेपीईजी 2000 फाइलों में लगातार भाग होते हैं। प्रत्येक चंक में 8 बाइट हेडर होता है: 4-बाइट चंक आकार (बिग-एंडियन, हाई बाइट पहले) और 4-बाइट चंक प्रकार - पूर्व-निर्धारित हस्ताक्षरों में से एक: "jP" या "jP2"।

दूसरा चंक "ftyp" प्रकार का होना चाहिए और ऑफ़सेट 8 पर एक उप-प्रकार होना चाहिए। \*.JPA टाइप करें), "jpm" (फ़ाइल प्रकार \*.JPM), "jpx" (फ़ाइल प्रकार \*.JPX)।

जब तक अज्ञात प्रकार का पता नहीं चलता है, तब तक इटरेटिंग चंक्स, हम JPEG 2000 इमेज/वीडियो फ़ाइल बनाते हैं।

### रंग परिवर्तन ###

प्रारंभ में, छवियों को आरजीबी रंग स्थान से दूसरे रंग स्थान में बदलने की आवश्यकता होती है। इस प्रयोजन के लिए, दो तरीके हैं: अपरिवर्तनीय रंग परिवर्तन (आईसीटी) और प्रतिवर्ती रंग परिवर्तन (आरसीटी)। पूर्व में YC,,B,,C,,R,, कलर स्पेस का उपयोग किया जाता है और इसे फिक्स / फ्लोटिंग-पॉइंट में लागू किया जाता है जबकि बाद में एक संशोधित YUV कलर स्पेस और प्रकृति में प्रतिवर्ती .// // RGB मॉडल, JPEG तक सीमित नहीं 2000 भाषा एकाधिक घटक परिवर्तन का उपयोग करती है।

### टाइलिंग ###

जब रंग परिवर्तन किया जाता है, तो छवि आयताकार क्षेत्रों में परिवर्तित हो जाती है जिसे टाइल कहा जाता है जिसे अलग से रूपांतरित और एन्कोड किया जा सकता है। सभी टाइलों का आकार समान होगा या पूरी छवि को एक एकल टाइल के रूप में माना जा सकता है। डिकोडर टाइलिंग का लाभ उठाता है और कम मेमोरी की खपत करता है या कुछ टाइलों को आंशिक रूप से एन्कोड कर सकता है। हालांकि इस तकनीक में तस्वीर की गुणवत्ता में गिरावट का नुकसान है।

### वेवलेट रूपांतरण ###

टाइलिंग के बाद की छवि वेवलेट रूपांतरित है जो या तो अपरिवर्तनीय या प्रतिवर्ती हो सकती है और कनवल्शन या लिफ्टिंग स्कीम का उपयोग करके कार्यान्वित की जा सकती है।

### दबाव अनुपात ###

एक छवि की भौतिक विशेषताओं के आधार पर, 20% का संपीड़न लाभ प्राप्त होता है जेपीईजी 2000 की स्थानिक-अतिरेक भविष्यवाणी संपीड़न प्रक्रिया में एक महत्वपूर्ण भूमिका निभाती है और उच्च रिज़ॉल्यूशन वाली छवियां सबसे अधिक लाभ प्राप्त करती हैं।

## मानक ## द्वारा प्रस्तुत अनुप्रयोग

* फ्रेम-आधारित एचडी वीडियो की रिकॉर्डिंग, संपादन और भंडारण
* मेडिकल इमेजरी और बायोमेट्रिक्स
* सैटेलाइट इमेज, रिमोट सेंसिंग और मोशन डिटेक्शन
* क्लाइंट / सर्वर संचार, नेटवर्क वितरण और भंडारण।
* डिजिटल सिनेमा, लाइव एचडीटीवी फीड योगदान, डिजिटाइज्ड ऑडियो-विजुअल सामान

## संदर्भ ##

* [जेपीईजी 2000 का अवलोकन](https://jpeg.org/jpeg2000/)
* [JPEG 2000 इमेज कोडिंग सिस्टम](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

