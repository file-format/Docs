
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एबीसी - एक्शनस्क्रिप्ट बाइट कोड फ़ाइल",
  "description":"एबीसी फ़ाइल प्रारूप के बारे में उदाहरण और एपीआई के साथ जानें जो एबीसी फाइलें बना और खोल सकता है।",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## एबीसी फाइल क्या है?

.abc एक्सटेंशन वाली फ़ाइल एक ActionScript बाइट कोड फ़ाइल है जिसे Flash कंपाइलर द्वारा ActionScript स्क्रिप्ट फ़ाइलों को संकलित करने के परिणामस्वरूप बनाया गया है। एबीसी फ़ाइल में निहित बाइट कोड को एक्शनस्क्रिप्ट वर्चुअल मशीन (एवीएम और एवीएम2) द्वारा निष्पादित किया जाता है। बाइट कोड में निरंतर डेटा, AVM2 निर्देश सेट से निर्देश और विभिन्न प्रकार के मेटाडेटा शामिल होते हैं। जब कोई ABC फ़ाइल AVM या AVM2 में लोड की जाती है, तो उसका सत्यापन किया जाता है। यदि यह AVM2 ओवरव्यू के अनुरूप नहीं है, तो इसे अस्वीकार कर दिया जाता है। एबीसी फाइलें एडोब फ्लैश प्लेयर में खोली जा सकती हैं जिन्हें बहुत समय पहले बंद कर दिया गया था।

## एबीसी फ़ाइल स्वरूप - अधिक जानकारी

एबीसी फाइलें बाइनरी फाइल फॉर्मेट में डिस्क में सहेजी जाती हैं जो एवीएम या एवीएम2 वर्चुअल मशीनों द्वारा पठनीय होती हैं। इसकी आंतरिक फ़ाइल संरचना अपने सभी निरंतर डेटा, टाइप डिस्क्रिप्टर, कोड और मेटाडेटा के साथ निष्पादन योग्य कोड ब्लॉक का प्रतिनिधित्व करती है।

## एबीसी फ़ाइल संरचना

एबीसी फ़ाइल संरचना नीचे दिखाया गया है।

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### एबीसी फाइल फील्ड्स

|फ़ील्ड का नाम|विवरण|
---|---|
|minor_version, major_version| major_version और major_version के मान abcFile प्रारूप के प्रमुख और लघु संस्करण संख्याएँ हैं।|
|constant_pool|constant_pool पूर्णांकों, डबल्स, स्ट्रिंग्स, नेमस्पेस, नेमस्पेस सेट, और बहुनामों से बना एक वैरिएबल लेंथ स्ट्रक्चर है।|
|method_count, method|method_count का मान विधि सरणी में प्रविष्टियों की संख्या है। मेथड एरे में प्रत्येक प्रविष्टि एक वेरिएबल लेंथ मेथड_इन्फो स्ट्रक्चर है
|metadata_count, metadata|metadata_count का मान मेटाडेटा सरणी में प्रविष्टियों की संख्या है। प्रत्येक मेटाडेटा प्रविष्टि एक मेटाडेटा_इन्फोस्ट्रक्चर है जो एक नाम को स्ट्रिंग मानों के एक सेट पर मैप करता है। |
|class_count, उदाहरण, वर्ग|class_count का मान उदाहरण और वर्ग सरणियों में प्रविष्टियों की संख्या है। |
|script_count, script|script_count का मान स्क्रिप्ट सरणी में प्रविष्टियों की संख्या है। प्रत्येक स्क्रिप्ट प्रविष्टि एक script_info संरचना है जो इस फ़ाइल में एकल स्क्रिप्ट की विशेषताओं को परिभाषित करती है। |
|method_body_count, method_body|method_body_count का मान, method_body सरणी में प्रविष्टियों की संख्या है। प्रत्येक मेथड_बॉडीएंट्री में एक वेरिएबल लेंथ मेथड_बॉडी_इन्फो स्ट्रक्चर होता है जिसमें एक इंडिविजुअल मेथड या फंक्शन के लिए निर्देश होते हैं।

## संदर्भ

* [मजबूत एबीसी (एक्शनस्क्रिप्ट बाइटकोड) [डिस-]असेंबलर - जीथब](https://github.com/CyberShadow/RABCDAsm)

