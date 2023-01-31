{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"फिट फ़ाइल प्रारूप- गार्मिन गतिविधि फ़ाइल",
  "description":"FIT फ़ाइल स्वरूप और API के बारे में जानें जो FIT फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## एक फिट फाइल क्या है?

FIT फ़ाइल Garmin स्पोर्ट्स वियरेबल डिवाइसेस द्वारा बनाई गई GIS फ़ाइल है। इसका उपयोग व्यक्ति की गतिविधियों को रिकॉर्ड करने के लिए किया जाता है जब वह इन उपकरणों को पहनकर चलता है। गतिविधि डेटा में GPS डिवाइस द्वारा रिकॉर्ड किए गए स्थान और समय शामिल होते हैं। एफआईटी फाइलों का उपयोग वेब एपीआई का उपयोग करके रिकॉर्ड किए गए गतिविधि डेटा को स्थानांतरित करने के लिए भी किया जाता है। यही कारण है कि फिटनेस डेटा को अन्य फिटनेस प्लेटफॉर्म के साथ साझा करने के लिए एफआईटी फाइलें सबसे अधिक इस्तेमाल की जाने वाली फाइल फॉर्मेट हैं। अन्य सामान्य फ़ाइल स्वरूपों में [GPX](/hi/gis/gpx/), TCX, और [KML](/hi/gis/kml/) शामिल हैं।

## फिट फ़ाइल प्रारूप - अधिक जानकारी

गतिविधि के लिए Garmin उपकरणों द्वारा दर्ज की गई जानकारी के साथ FIT फ़ाइलों को बाइनरी फ़ाइलों के रूप में डिस्क में सहेजा जाता है। एक FIT फ़ाइल के अंदर संग्रहीत जानकारी में शामिल हैं:

* दिनांक और समय
*खेल प्रकार
* गोद और विभाजित डेटा
* जीपीएस ट्रैक
* सेंसर डेटा
* सक्रिय सत्र के लिए कार्यक्रम

गतिविधि डेटा को वास्तविक समय में फ़ाइल में रिकॉर्ड किया जा सकता है या गतिविधि रिकॉर्डिंग पूर्ण होने के बाद निर्यात किया जा सकता है।

### फिट गतिविधि संदेश

एक FIT गतिविधि फ़ाइल में कुछ आवश्यक संदेश प्रकार शामिल हो सकते हैं। गतिविधि फ़ाइल के लिए आवश्यक संदेश निम्नलिखित हैं।

|संदेश|उद्देश्य|
---|---|
|फाइल आईडी| फ़ाइल आईडी संदेश सभी FIT फ़ाइल प्रकारों के लिए आवश्यक है और फ़ाइल में पहला संदेश होने की उम्मीद है। गतिविधि फ़ाइलों के लिए, प्रकार संपत्ति को 4.| . पर सेट किया जाना चाहिए
|गतिविधि| FIT गतिविधि फ़ाइल में एकल गतिविधि संदेश की आवश्यकता होती है। गतिविधि संदेश में शामिल स्थानीय टाइमस्टैम्प और सत्र गणना गुण हैं। स्थानीय टाइमस्टैम्प का उपयोग उस समय क्षेत्र ऑफ़सेट को निर्धारित करने के लिए किया जाता है जिसे फ़ाइल में सभी टाइमस्टैम्प पर लागू किया जा सकता है। अधिकांश डिवाइस वास्तविक समय में FIT फ़ाइलों को रिकॉर्ड करते हैं और रिकॉर्डिंग के अंत तक सत्र की संख्या अज्ञात रहेगी। इस वजह से, गतिविधि संदेश अक्सर फ़ाइल में अंतिम संदेश होगा।|
|सत्र| गतिविधि फ़ाइलों में एक या अधिक सत्र संदेश होंगे। एक सत्र संदेश एक सारांश संदेश प्रकार है। सभी सारांश संदेशों के लिए प्रारंभ समय, कुल बीता हुआ समय, कुल टाइमर समय और टाइमस्टैम्प आवश्यक फ़ील्ड हैं
|गोद| लैप संदेश सत्र के भीतर अंतराल या अंतराल का प्रतिनिधित्व करते हैं। लैप संदेश एक सारांश संदेश प्रकार है। सभी सारांश संदेशों के लिए प्रारंभ समय, कुल बीता हुआ समय, कुल टाइमर समय और टाइमस्टैम्प आवश्यक फ़ील्ड हैं
|रिकॉर्ड| रिकॉर्ड संदेशों में GPS निर्देशांक, गति, दूरी, हृदय गति, शक्ति, आदि शामिल हैं|

## फिट फ़ाइल उपयोगी संसाधन

* [फिट गतिविधि फ़ाइलों को डिकोड करना](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [एफ़आईटी गतिविधि फ़ाइलें एन्कोडिंग](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## संदर्भ ##

* [फिट गतिविधि फ़ाइल](https://developer.garmin.com/fit/file-types/activity/)
