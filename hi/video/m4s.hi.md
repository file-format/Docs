{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S फ़ाइल - M4S फ़ाइल क्या है?",
  "description":"M4S फ़ाइल स्वरूप और API के बारे में जानें जो M4S फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## M4S फ़ाइल क्या है?

एक M4S फ़ाइल एक वीडियो का एक छोटा सा खंड है जिसे **MPEG-DASH** स्ट्रीमिंग तकनीक का उपयोग करके इंटरनेट पर स्ट्रीम किया जाता है। इसमें बाइनरी डेटा के रूप में एक वीडियो सेगमेंट होता है। प्राप्त करने वाला एप्लिकेशन (आमतौर पर एक वेब ब्राउज़र या मीडिया प्लेयर) इन सेगमेंट को प्राप्त होने के क्रम में चलाता है। पहले M4S खंड की पहचान आरंभीकरण डेटा द्वारा की जाती है जिसमें यह शामिल है। **सारांश** में, M4S फ़ाइलें एक पूर्ण फ़ाइल के छोटे व्यक्तिगत मीडिया खंड हैं।

## M4S फ़ाइल स्वरूप

M4S फ़ाइलें [ISO बेस मीडिया फ़ाइल (ISOBMFF) फ़ॉर्मैट](https://www.w3.org/TR/mse-byte-stream-format-isobmff/) पर आधारित होती हैं। बड़ी फ़ाइल के इन छोटे खंडों को HTTP के माध्यम से स्वतंत्र रूप से डाउनलोड किया जा सकता है। इस प्रकार, यदि आपके पास एक बड़ी [MP4](/hi/video/mp4/) मूवी फ़ाइल है, तो इसे MPEG-DASH (डायनेमिक अडैप्टिव स्ट्रीमिंग ओवर HTTP) तकनीक का उपयोग करके इसे M4S सेगमेंट फ़ाइलों के रूप में विभाजित करके स्ट्रीम किया जा सकता है। यदि इस बड़ी मूवी फ़ाइल को M4S के रूप में डिस्क में डाउनलोड किया जाता है, तो एकाधिक M4S फ़ाइलें डाउनलोड की जाती हैं। यदि इन सभी .m4s खंडों को जोड़ा जाता है, तो एक पूर्ण खेलने योग्य फ़ाइल तैयार की जाती है। मीडिया प्लेयर फ़ाइल को तब तक नहीं चला सकते जब तक कि फ़ाइल के साथ पहला इनिशियलाइज़ेशन सेगमेंट भी उपलब्ध न हो।

## एमपीईजी-डैश स्ट्रीमिंग के बारे में

MPEG-DASH अनुकूली बिटरेट स्ट्रीमिंग तकनीक का उपयोग करता है जो इंटरनेट पर उच्च गुणवत्ता वाली मीडिया सामग्री को स्ट्रीम करना संभव बनाता है। यह सामग्री को छोटे खंडों के अनुक्रम में विभाजित करके किया जाता है जो HTTP पर प्रवाहित होते हैं। मूवी, पॉडकास्ट, या किसी स्पोर्ट्स इवेंट के लाइव प्रसारण जैसी बड़ी मीडिया फ़ाइलों को इस तरह से स्ट्रीम किया जा सकता है। ये खंड अलग-अलग बिट दरों पर एन्कोड किए गए हैं। एमपीईजी-डीएएसएच सक्षम मीडिया प्लेयर स्वचालित रूप से बिट दर अनुकूलन एल्गोरिदम का उपयोग करके उच्चतम बिट दर वाले सेगमेंट का चयन करता है। यह प्लेबैक में घटनाओं को रोकने या फिर से बफ़र करने से बचता है।

### एम4एस फाइलों के लिए ओपन-सोर्स एपीआई

ऐसे ओपन सोर्स एपीआई उपलब्ध हैं जिनका उपयोग M4S फाइलों को पढ़ने और बदलने के लिए किया जा सकता है।

* [libdash](https://github.com/bitmovin/libdash) - M4S फ़ाइलों के लिए .NET API
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - M4S फ़ाइल के लिए Javascript क्लाइंट
* [डैश फ़ाइलें बनाने के लिए लाइब्रेरी पर जाएं](https://github.com/zencoder/go-dash)

### एम4एस को एमपी4 में बदलने के लिए ओपन-सोर्स एपीआई

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## संदर्भ ###

* [ISO बेस मीडिया फ़ाइल (ISOBMFF) फ़ॉर्मैट](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [एचटीटीपी पर गतिशील अनुकूली स्ट्रीमिंग - एमपीईजी-डीएएसएच] (https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)
