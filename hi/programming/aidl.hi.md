{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL फ़ाइल - Android इंटरफ़ेस परिभाषा भाषा फ़ाइल",
  "description":"एआईडीएल फ़ाइल प्रारूप क्या है, उदाहरण और एपीआई के बारे में जानें जो एआईडीएल फाइलें बना और खोल सकते हैं।",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## एआईडीएल फाइल क्या है?

एक एआईडीएल (एंड्रॉइड इंटरफेस डेफिनिशन लैंग्वेज) फ़ाइल एंड्रॉइड डेवलपर्स को विभिन्न ऐप्स के बीच संचार स्थापित करने की अनुमति देती है। प्रोग्रामिंग इंटरफेस के आधार पर, ग्राहक और सेवा दोनों इंटरप्रोसेस संचार (आईपीसी) का उपयोग कर संवाद करने के लिए सहमत हैं। एआईडीएल फ़ाइल में इन इंटरफेस को परिभाषित करने के लिए [जावा](/hi/ प्रोग्रामिंग/जावा/) स्रोत कोड और ऐप्स के बीच संचार के लिए अनुबंध शामिल हैं।

आप Google Android Studio या Microsoft Notepad और Notepad++ जैसे किसी टेक्स्ट एडिटर के साथ AIDL फाइलें खोल सकते हैं।

## एआईडीएल फ़ाइल स्वरूप - अधिक जानकारी

एआईडीएल टेक्स्ट फाइलें हैं जिनमें ऐप्स के बीच संचार के लिए इंटरफेस होते हैं। Android OS एक प्रक्रिया को दूसरी प्रक्रिया की मेमोरी तक पहुँचने की अनुमति नहीं देता है। यह अंतर्निहित ऑपरेटिंग सिस्टम को समझने और डेवलपर के लिए संचार संरचनाओं की प्रक्रिया स्थापित करने के लिए प्रक्रियाओं को उनकी वस्तुओं को आदिम में विभाजित करने की ओर ले जाता है।

### एआईडीएल द्वारा किस डेटा प्रकार का समर्थन किया जाता है?

एआईडीएल डिफ़ॉल्ट रूप से निम्नलिखित डेटा प्रकारों का समर्थन करता है।

* जावा प्रोग्रामिंग भाषा में सभी आदिम प्रकार (जैसे int, long, char, boolean, और इसी तरह)
* डोरी
* चार अनुक्रम
* सूची
* नक्शा

## एआईडीएल फ़ाइल उदाहरण

निम्नलिखित उदाहरण एआईडीएल फ़ाइल है।

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## संदर्भ

* [एंड्रॉइड इंटरफेस डेफिनिशन लैंग्वेज (एआईडीएल)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

