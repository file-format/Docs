{
  "date" : "2021-03-10",
  "keywords" :["वीपी8", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "वीडियो फॉर्मेट", "ट्रूमोशन वीडियो", "वेबआरटीसी", "वेबएम"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP8 - ट्रूमोशन वीडियो फ़ाइल",
  "description":"VP8 फ़ाइल स्वरूप और API के बारे में जानें जो VP8 फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "VP8",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## VP8 फ़ाइल क्या है?

Google द्वारा VP8 को सर्वश्रेष्ठ चित्र गुणवत्ता डेटा दर और एन्कोडिंग गति वाले सर्वश्रेष्ठ वीडियो प्रारूपों में से एक के रूप में घोषित किया गया है। VP8 का सबसे अच्छा लाभ यह है कि यह H.264 का रॉयल्टी-मुक्त विकल्प है। यह फ़ाइल या बिटस्ट्रीम के रूप में उच्च-गुणवत्ता वाले वीडियो को एन्कोडिंग और डिकोड करने के लिए एक विशिष्ट प्रारूप है। यह मुफ़्त है क्योंकि Google ने रॉयल्टी-मुक्त सार्वजनिक लाइसेंस के तहत सभी VP8 पेटेंट जारी किए हैं। लगभग 90% या अधिक सभी WebRTC वीडियो सत्र VP8 का उपयोग करते हैं।

## VP8 फ़ाइल स्वरूप

VP8 को 2008 में On2 Technologies द्वारा विकसित किया गया था और बाद में 2010 में Google के स्वामित्व में आ गया। VP8 वीडियो कोडेक का मुख्य लाभ यह है कि यह मुफ़्त लाइसेंस के तहत रॉयल्टी से मुक्त है। इसे वेब और मोबाइल उपकरणों के लिए उच्च-गुणवत्ता वाला वीडियो प्रदान करने के लिए डिज़ाइन किया गया है। VP8 के लिए पहला ऑडियो-वीडियो कंटेनर WebM था और इस कोडेक को 2011 में WebRTC वीडियो कोडेक के रूप में चुना गया था। इस प्रारूप को HTML5, वेब रियल-टाइम कम्युनिकेशन और विभिन्न ब्राउज़रों में वीडियो प्लेबैक जैसे कई औद्योगिक अनुप्रयोगों में स्वीकार किया जा रहा है। फुल-एचडी रिजॉल्यूशन पर इस फॉर्मेट को सपोर्ट करने की पूरी बाजार मांग है। इसका उपयोग वीडियो कॉन्फ्रेंसिंग, वीडियो प्रसारण और मोबाइल उपकरणों से रिकॉर्डिंग जैसे विभिन्न उद्देश्यों के लिए किया जाता है।

## विशेष विवरण ##

### VP8 की विशेषताएं
 



* मुफ्त वीडियो कोडेक
* सबसे प्रगतिशील वीडियो फ़ाइल स्वरूप
* फ्रेम हानि के लिए बेहतर प्रतिरोध
* हाई-स्पीड वीडियो डिकोडिंग
* हार्डवेयर प्लेटफॉर्म पर युक्ति बनाना आसान
* इसमें एक शुद्ध परिचय मोड की विशेषता है, यानी वीडियो संपादन जैसे अनुप्रयोगों में यादृच्छिक पहुंच को सक्षम करने के लिए अनुक्रमिक भविष्यवाणी के बिना केवल व्यक्तिगत रूप से कोडित फ्रेम का उपयोग करना
* libvpx एकमात्र सॉफ्टवेयर लाइब्रेरी है जो VP8 वीडियो स्ट्रीम को एनकोड करने में कुशल है
* VP8 को स्पष्ट रूप से मुख्य रूप से एक गुणवत्ता श्रेणी में संचालित करने के लिए डिज़ाइन किया गया था

* वेब से जुड़े क्लाइंट हार्डवेयर की एक विस्तृत श्रृंखला है, जो कम शक्ति वाले मोबाइल और प्रत्यारोपित उपकरणों से लेकर कई प्रोसेसर कोर वाले सबसे उन्नत डेस्कटॉप कंप्यूटरों तक फैली हुई है।
* 420 कलर सैंपलिंग, 8 बिट प्रति चैनल कलर डेप्थ, प्रोग्रेसिव स्कैन, और इमेज डाइमेंशन्स उच्चतम 16383x16383 पिक्सल्स इमेज फॉर्मेट के माध्यम से आसानी से संचालित किए जा सकते हैं
* इन डिज़ाइन बस्तियों के नीचे संपीड़न क्षमता और डिकोडर सादगी के लिए आवेग अन्य स्वीकृत वीडियो संपीड़न प्रारूपों की तुलना में VP8 में कई अनूठी तकनीकी विशेषताओं का कारण बना
* VP8 तीन संदर्भ फ़्रेमों का उपयोग करता है, अन्य प्रारूपों में देखी गई कई संदर्भ गति क्षतिपूर्ति योजना से
* VP8 फ़्रेम दर या डेटा दर तक सीमित नहीं है। यह चौड़ाई और ऊंचाई दोनों के लिए 14 बिट्स का उपयोग करता है, जो उच्चतम रिज़ॉल्यूशन 16384x16384 पिक्सेल बनाता है

### VP8 की सीमाएं

रिज़ॉल्यूशन, डेटा दर और फ़्रेम दर के संदर्भ में VP8 की सीमाएँ इस प्रकार हैं:

* VP8 16384x16384 पिक्सेल के अधिकतम रिज़ॉल्यूशन के लिए चौड़ाई और ऊंचाई के लिए 14 बिट्स का अभ्यास करता है
* VP9 65536x65536 पिक्सेल के अधिकतम रिज़ॉल्यूशन के लिए चौड़ाई और ऊंचाई के लिए 16 बिट्स का उपयोग करता है
* फ्रैमरेट या डेटा दर पर कोई प्रतिबंध नहीं है
 



 



## संदर्भ

* [VP8 विकिपीडिया](https://en.wikipedia.org/wiki/VP8#:~:text=VP8%20was%20first%20released%20by,%2C%20replacing%20its%20predcessor%2C%20VP7.&text= %20मई%2019%2C%20at%20इसकी,एक%20अपरिवर्तनीय%20मुक्त%20पेटेंट%20लाइसेंस)
* [स्प्रिंगर लिंक](https://link.springer.com/chapter/10.1007/978-81-322-1157-0_32)
