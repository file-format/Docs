
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एपीकेएस फाइल - एपीके सेट आर्काइव",
  "description":"एपीकेएस फ़ाइल क्या है, इसके बारे में जानें?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## एपीकेएस फाइल क्या है?

.apks एक्सटेंशन वाली फ़ाइल एक आर्काइव फ़ाइल है जो Android पैकेज **APK** फ़ाइलों का एक संग्रह है। एपीकेएस फ़ाइल में प्रत्येक व्यक्तिगत एपीके फ़ाइल उपकरणों के विभिन्न पहलुओं को ध्यान में रखते हुए उत्पन्न होती है। इनमें आर्किटेक्चर, भाषा, स्क्रीन डेंसिटी और डिवाइस की अन्य विशेषताएं शामिल हैं। एपीकेएस फाइलें **बंडलटूल** द्वारा उत्पन्न की जाती हैं। इसका उपयोग एंड्रॉइड ऐप बंडल बनाने और डिवाइस पर तैनाती के लिए ऐप बंडल को अलग-अलग एपीके में बदलने के लिए किया जाता है।

## APKS फ़ाइल स्वरूप - अधिक जानकारी

APKS फ़ाइलें [ZIP](/hi/compression/zip/) फ़ाइल स्वरूप का उपयोग करके संपीड़ित फ़ाइलों के रूप में सहेजी जाती हैं।

## एपीकेएस फाइल कैसे जनरेट करें?

जब Android ऐप बंडल (AAB) तैयार हो जाता है, तो Google Play स्टोर पर उसके व्यवहार का किसी डिवाइस पर परिनियोजन के लिए परीक्षण किया जा सकता है। इस उद्देश्य के लिए, एएबी फाइलों से एपीकेएस फाइलें उत्पन्न की जा सकती हैं और Google के एंड्रॉइड [बंडलटूल] (https://developer.android.com/studio/command-line/bundletool) का उपयोग करके परीक्षण उपकरणों पर स्थापित की जा सकती हैं। यह निम्नलिखित कमांड का उपयोग करके एपीके से एपीकेएस आर्काइव फ़ाइल बनाने के लिए कमांड लाइन टूल प्रदान करता है।

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

एपीके को डिवाइस पर तैनात करने के लिए, एपीकेएस फ़ाइल को डिवाइस हस्ताक्षर जानकारी के साथ निम्नानुसार हस्ताक्षरित किया जा सकता है।

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## संदर्भ

* [बंडलटूल - कमांडलाइन] (https://developer.android.com/studio/command-line/bundletool)

