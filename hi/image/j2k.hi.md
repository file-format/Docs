{
  "date" : "2019-10-11",
  "keywords" :[ "j2k फ़ाइल", "j2k फ़ाइल स्वरूप", "j2k फ़ाइल क्या है", "फ़ाइल", "j2k उदाहरण", "j2k फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"जे2के",
  "description":"J2K फ़ाइल स्वरूप और API के बारे में जानें जो J2K फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## J2K फ़ाइल क्या है?

A **J2K** फ़ाइल एक छवि है जिसे DCT संपीड़न के बजाय तरंगिका संपीड़न का उपयोग करके संपीड़ित किया जाता है। इस फ़ाइल स्वरूप का उपयोग संयुक्त फ़ोटोग्राफ़िक विशेषज्ञ समूह (JPEG) 2000 फ़ाइलों द्वारा किया जाता है। J2K फ़ाइलें XML में छवि फ़ाइल के बारे में मेटाडेटा जानकारी संग्रहीत करती हैं, .jpeg या .jpg के विपरीत जो इस उद्देश्य के लिए EXIF प्रारूप का उपयोग करती हैं। J2K फाइलें 15-बिट रंग, अल्फा पारदर्शिता और दोषरहित संपीड़न का समर्थन करती हैं। JPEG 2000 छवियों जैसे J2K-Codec को डिकोड करने के लिए कई वाणिज्यिक API मौजूद हैं। मानक छवि दर्शकों का उपयोग करके Windows OS पर एक J2K फ़ाइल खोली जा सकती है।

## J2K फ़ाइल स्वरूप ##

J2K फ़ाइल स्वरूप JPEG 2000 के समान है जिसे अक्सर .jp2 और .jpc के रूप में सहेजा जाता है। यह J2K फ़ाइलों को XML प्रारूप में मेटाडेटा एन्कोडिंग के समान दृष्टिकोण का पालन करता है जहां मानक 12234-1 का उपयोग Exif टैग और XML घटकों के बीच संदर्भ के रूप में किया जाता है। इसे JPEG 2000 पार्ट-2 एक्सटेंशन द्वारा और बेहतर बनाया गया है जो एनीमेशन तंत्र और कोड स्ट्रीम कॉन्फ़िगरेशन को एक सिंगल इमेज में जोड़ता है। ऐसी विस्तारित फ़ाइल-प्रारूप फ़ाइलें .jpx के रूप में सहेजी जाती हैं।

### JPEG2000 फ़ाइल का लेआउट ###

JPEG2000 एक्स्टेंसिबल फ़ाइल स्वरूपों के अनुरूपता के आधार पर विभिन्न प्रकार के अनुप्रयोगों का समर्थन करता है। हालांकि सबसे सरल प्रकार में एक ही छवि हो सकती है, अधिक जटिल प्रकारों में छवियों की एक श्रृंखला शामिल हो सकती है, जो एक दूसरे के ऊपर खड़ी होती हैं या समय-आधारित अनुक्रमित होती हैं।

#### JP2 बॉक्स ####
यह JP2 फ़ाइल स्वरूप का शीर्ष-स्तरीय बिल्डिंग ब्लॉक है और इसमें हेडर में एक प्रकार और लंबाई फ़ील्ड और डेटा सेक्टन शामिल हैं। सबसे उल्लेखनीय प्रकार का बॉक्स सन्निहित कोडस्ट्रीम बॉक्स है। यह बॉक्स अपने डेटा सेक्शन JPEG2000 कोडस्ट्रीम में स्टोर करता है।

#### JPEG2000 कोडस्ट्रीम ####

JPEG2000 कोडस्ट्रीम बाइट्स का एक अनुक्रम है जो JPEG2000 संपीड़ित छवि को डिकोड करने के लिए आवश्यक है। यदि फ़ाइल में इस कोडस्ट्रीम के अलावा और कुछ नहीं है, तो इसे रॉ कोडस्ट्रीम फ़ाइल कहा जाता है। आमतौर पर एक JPEG कोडस्ट्रीम एक छवि पर JPEG2000 कम्प्रेशन एल्गोरिथम का अनुप्रयोग है, हालांकि यह एकमात्र तरीका नहीं है।

#### टाइल के पुर्जे ####

JPEG2000 एन्कोडेड छवि डेटा इकाइयों का एक संग्रह है जिसे पैकेट कहा जाता है। इन पैकेटों को टाइल-पार्ट्स कहे जाने वाले पैकेट समूहों के अंदर कोडस्ट्रीम में रखा जाता है। किसी छवि को एन्कोड करने से पहले, एनकोडर छवि को ब्लॉकों के एक आयताकार ग्रिड में विभाजित करता है, जिसे टाइल कहा जाता है, जहां प्रत्येक टाइल को अन्य टाइलों के बावजूद अलग से एन्कोड किया जाता है।

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 फ़ाइल स्वरूप" >}}

## J2K संपीड़न ##
JPEG 2000 वेवलेट कम्प्रेशन तकनीक का उपयोग करता है जो इसे इस तथ्य के आधार पर तेज़ बनाता है कि दर्शक जिस भी व्यूपोर्ट या विंडो में छवि प्रदर्शित करता है उसमें अपेक्षाकृत कुछ पिक्सेल दिखाए जाते हैं। इसे इस तथ्य से बल दिया जा सकता है कि बहुत बड़े आकार की छवियों (गीगाबाइट्स में) के लिए स्क्रीन पर केवल कुछ मेगाबाइट पिक्सेल दिखाई देंगे। यह छवि डेटा के केवल उस हिस्से को तेज़ी से लाने और प्रस्तुत करने में मदद करता है जो डिस्प्ले पिक्सेल को पॉप्युलेट करने के लिए आवश्यक है। फ्लाई पर आवश्यक इमेजरी बनाने के लिए छवि लाने के तंत्र को तेज करने के लिए उच्च गति डीकंप्रेसन तकनीक की भी आवश्यकता होती है।

J2K तेजी से विसंपीड़न का लाभ उठाता है और पिक्सेल डेटा के लिए स्क्रीन पर जल्दी से दिखाई देने वाली छवियों का हिस्सा प्रस्तुत करने के लिए केवल आवश्यक जानकारी प्राप्त करता है। J2K मुख्य रूप से डेटा को देखने और इसे संपादित करने के लिए डिज़ाइन किया गया है।

## J2K पहचान ##
जेपीईजी 2000 फाइलों में हस्ताक्षर बाइट्स 6ए 50 20 20 हैं।

### माइम प्रकार ###
जेपीईजी 2000 फाइलों के लिए पंजीकृत माइम प्रकार में शामिल हैं:
* छवि/जेपी2
* इमेज/जेपीएक्स
* छवि/जेपीएम
* वीडियो/mj2

## जेपीईजी मानक ## में सुधार
जेपीईजी मानक में सुधारों में शामिल हैं:
* सुपीरियर संपीड़न प्रदर्शन
* एकाधिक संकल्प प्रतिनिधित्व
* पिक्सेल और संकल्प सटीकता द्वारा प्रगतिशील संचरण
* दोषरहित या हानिपूर्ण संपीड़न का विकल्प
* त्रुटि लचीलापन, लचीला फ़ाइल स्वरूप
* उच्च गतिशील रेंज समर्थन
* साइड चैनल स्थानिक जानकारी

## संदर्भ ##
* [तौबमन, डेविड; मार्सेलिन, माइकल (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)
