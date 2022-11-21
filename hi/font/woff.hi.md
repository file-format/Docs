{
  "date" : "2020-08-20",
  "keywords" :[ "woff फ़ाइल", "woff फ़ाइल स्वरूप", "woff फ़ाइल क्या है", "फ़ाइल", "woff उदाहरण", "woff फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - वेब ओपन फाइल फॉर्मेट",
  "description":"WOFF फाइल वेब ओपन फॉन्ट फॉर्मेट में बनाया गया एक ओपन फॉन्ट फॉर्मेट है।",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## WOFF फ़ाइल क्या है?

.woff एक्सटेंशन वाली फाइल वेब ओपन फॉन्ट फॉर्मेट (WOFF) पर आधारित एक वेब फॉन्ट फाइल होती है। इसमें ट्रू टाइप (.TTF) या ओपन टाइप (.OTT) फ़ॉन्ट प्रकारों के आधार पर प्रारूप-विशिष्ट संपीड़ित कंटेनर है। WOFF को डेस्कटॉप अनुप्रयोगों में उपयोग की जाने वाली फ़ॉन्ट फ़ाइलों से वेब फोंट को अलग करने के उद्देश्य से पेश किया गया था। इसके अलावा, नेटवर्क पर सर्वर से क्लाइंट के कंप्यूटर पर फोंट ट्रांसफर की विलंबता को कम करने के लिए लक्षित प्रारूप। कई उपकरण उपलब्ध हैं जो WOFF फ़ाइलों को TTF और अन्य फ़ॉन्ट फ़ाइल स्वरूपों में परिवर्तित कर सकते हैं।

## **WOFF फ़ाइल स्वरूप**

WOFF फ़ॉन्ट प्रारूप विभिन्न फ़ॉन्ट प्रकारों जैसे ट्रू टाइप, ओपन टाइप, और ओपन फॉन्ट फॉर्मेट में उपयोग किए जाने वाले टेबल-आधारित एसएफएनटी संरचनाओं के फ़ॉन्ट डेटा टेबल को संपीड़ित करता है। यह इन फ़ॉन्ट प्रकारों के लिए एक कंटेनर की तरह है और इसमें कंटेनर में शामिल किए जाने वाले फ़ॉन्ट के मेटाडेटा और निजी उपयोग के डेटा को शामिल करने के लिए जगह भी है। कन्वर्टर sfnt फ़ाइलों का उपयोग WOFF स्वरूपित फ़ाइल में करते हैं और उपयोगकर्ता एजेंट वेब दस्तावेज़ के साथ उपयोग के लिए एन्कोडेड फ़ाइल को पुनर्स्थापित करते हैं। यह ध्यान दिया जाना चाहिए कि पुनर्स्थापित फ़ॉन्ट डेटा सभी पहलुओं से इनपुट फ़ॉन्ट प्रारूप से बिल्कुल मेल खाता है।

WOFF फ़ाइल उपयोगिताओं में अक्सर अतिरिक्त सुविधाएँ होती हैं जैसे कि ग्लिफ़ सबसेटिंग, सत्यापन या फ़ॉन्ट सुविधा परिवर्धन लेकिन यह आवश्यक नहीं है। निर्माता और उपयोग एजेंट दोनों को यह सुनिश्चित करना चाहिए कि अंतर्निहित फ़ॉन्ट डेटा की वैधता संरक्षित है।

### WOFF फ़ाइल संरचना

WOFF file structure is similar to that of sfnt fonts. It is based on a table directory that contains the lengths and offsets to each font data tables. All the tables are followed after this initial information. The file contains font database that are the same as in the original fonts. The order of the tables are also the same but each may be compressed. WOFF table directory replaces the original table directory though.


A WOFF file consists of following:


* WOFFHeader - मेटाडेटा और निजी डेटा ब्लॉक के ऑफसेट के साथ मूल फ़ॉन्ट प्रकार और संस्करण के साथ फ़ाइल हेडर।
 * TableDirectory -	Directory of font tables, indicating the original size, compressed size and location of each table within the WOFF file.

* FontTables - इनपुट sfnt फ़ॉन्ट से फ़ॉन्ट डेटा टेबल, बैंडविड्थ आवश्यकताओं को कम करने के लिए संकुचित।
* ExtendedMetadata - विस्तारित मेटाडेटा का एक वैकल्पिक ब्लॉक, XML प्रारूप में दर्शाया गया है और WOFF फ़ाइल में भंडारण के लिए संकुचित है।
* PrivateData- उपयोग करने के लिए फ़ॉन्ट डिज़ाइनर, फ़ाउंड्री या विक्रेता के लिए निजी डेटा का एक वैकल्पिक ब्लॉक।

### WOFF हैडर
The WOFF header comprises of an identifying signature which indicates the the kind of data included in the file. The WOFF header along with its fields is as follow.


|प्रकार|फ़ील्ड का नाम|विवरण|
---|---|---|
|UInt32|हस्ताक्षर |0x774F4646 'wOFF' |
|UInt32|	flavor	|The "sfnt version" of the input font.|

|यूइंट32| लंबाई |WOFF फ़ाइल का कुल आकार।|
|यूइंट16| numTables |फ़ॉन्ट टेबल की निर्देशिका में प्रविष्टियों की संख्या।|
|यूइंट16| आरक्षित |आरक्षित; शून्य पर सेट।|
|यूइंट32| TotalSfntSize | असम्पीडित फ़ॉन्ट डेटा के लिए आवश्यक कुल आकार, जिसमें sfnt शीर्षलेख, निर्देशिका और फ़ॉन्ट तालिकाएं (पैडिंग सहित) शामिल हैं।
|यूइंट16| प्रमुख संस्करण |WOFF फ़ाइल का प्रमुख संस्करण।|
|यूइंट16| माइनर वर्जन |WOFF फाइल का माइनर वर्जन।|
|यूइंट32| मेटाऑफ़सेट |WOFF फ़ाइल की शुरुआत से मेटाडेटा ब्लॉक के लिए ऑफसेट।|
|यूइंट32| metaLength |संपीड़ित मेटाडेटा ब्लॉक की लंबाई।|
|यूइंट32| metaOrigLength |मेटाडेटा ब्लॉक का असम्पीडित आकार।|
|यूइंट32| privOffset | WOFF फ़ाइल की शुरुआत से निजी डेटा ब्लॉक में ऑफसेट
|यूइंट32| privLength |निजी डेटा ब्लॉक की लंबाई।|


## **संदर्भ**
* [w3 WOFF फाइल फॉर्मेट](https://www.w3.org/TR/WOFF/)

