{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SIFZ फ़ाइल स्वरूप - Synfig Studio संपीड़ित परियोजना फ़ाइल",
  "description":"SIFZ फ़ाइल स्वरूप और API के बारे में जानें जो SIFZ फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## SIFZ फ़ाइल क्या है?

SIFZ फ़ाइल ओपन सोर्स 2d एनिमेशन निर्माण एप्लिकेशन **Synfig Studio** द्वारा बनाई गई एक gzip संपीड़ित SIF फ़ाइल है। इसमें कई ग्राफिकल तत्व होते हैं जो एनीमेशन के लिए बनाते हैं। समग्र एनीमेशन सामग्री कैनवास के संयोजन का उपयोग करके बनाई गई है जो आकार, ब्रश या पेंसिल स्ट्रोक और टेक्स्ट से भरा है। इन सभी को अपनी-अपनी स्थिति, त्रिज्या, स्पर्शरेखा, कोण, शीर्ष और चौड़ाई के हैंडल पर व्यवस्थित किया गया है। SIFZ फाइलें [Synfig Studio](https://www.synfig.org/) से खोली जा सकती हैं।

## SIFZ फ़ाइल स्वरूप

SIFZ फ़ाइलें संकुचित [ZIP](/hi/compression/zip/) फ़ाइलें होती हैं जिन्हें gzip संपीड़न विधि का उपयोग करके पैक किया जाता है। Synfig का उपयोग वेक्टर और बिटमैप आर्टवर्क का उपयोग करके फिल्म-गुणवत्ता वाले एनिमेशन बनाने के लिए किया जाता है। पुरानी फ़्रेम-दर-फ़्रेम एनीमेशन निर्माण पद्धति के विपरीत, यह आपको कम संसाधनों के साथ उच्च गुणवत्ता वाले 2डी एनिमेशन बनाने देती है।

SIFZ फ़ाइलें, संपीड़ित होने के कारण, असम्पीडित SIF फ़ाइलों से छोटी होती हैं। इससे कम बैंडविड्थ वाले इंटरनेट कनेक्शनों को स्थानांतरित करना भी आसान हो जाता है।

## संदर्भ

* [सिनफिग ओपन सोर्स - जीथब](https://github.com/synfig/synfig/)
* [सिनफिग डॉक्यूमेंटेशन](https://synfig.readthedocs.io/en/latest/index.html)
