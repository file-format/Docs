{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "एक्सटेंशन", "फाइल", "फाइल फॉर्मेट", "डेटाबेस फाइल टाइप", "डेटाबेस फाइल फॉर्मेट", "डेटा टियर एप्लिकेशंस पैकेज"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DACPAC फ़ाइल स्वरूप और API के बारे में जानें जो DACPAC फ़ाइलें बना और खोल सकते हैं।",
  "title" :"DACPAC - डेटा टियर एप्लिकेशन पैकेज",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## DACPAC फ़ाइल क्या है?

.dacpac (डेटा टियर एप्लीकेशन पैकेज के लिए खड़ा है) एक्सटेंशन वाली एक फ़ाइल एक डेटाबेस फ़ाइल है, जिसे Microsoft SQL सर्वर डेटा टियर एप्लिकेशन के साथ बनाया गया है, जिसमें डेटाबेस ऑब्जेक्ट के प्रतिनिधित्व के लिए डेटाबेस मॉडल शामिल है। चूंकि इसमें डेटाबेस का पूरा मॉडल होता है, इसलिए इसका उपयोग मॉडल में उपलब्ध विवरण से डेटाबेस को पुनर्स्थापित करने के लिए किया जाता है। DACPAC फाइलें आमतौर पर डेटाबेस को पुनर्स्थापित करने के लिए ग्राहक के परिसर में स्थापना के लिए तैनाती टीमों को सौंप दी जाती हैं। इन्हें के साथ खोला जा सकता है
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019) के बारे में।

## DACPAC फ़ाइल स्वरूप - अधिक जानकारी

DACPAC डेटा पैकेज फ़ाइलें वास्तव में संपीड़ित ज़िप फ़ाइलें होती हैं जिनमें कई [XML](/hi/web/xml/) फ़ाइलें होती हैं जिनमें डेटाबेस मॉडल के बारे में जानकारी होती है, जैसे कि टेबल और दृश्य, जिनका उपयोग डेटाबेस को पुनर्स्थापित करने के लिए किया जाता है। DACPAC फ़ाइलों की सामग्री को देखने के लिए, .dacpac से [.zip](/hi/compression/zip/) फ़ाइलों का नाम बदलें और किसी भी डीकंप्रेसन उपयोगिता का उपयोग करके ज़िप संग्रह को निकालें।

निम्नलिखित कुछ फाइलें हैं जो एक DACPAC फ़ाइल के अंदर पाई जाती हैं।

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>सीआरएम</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* उत्पत्ति.एक्सएमएल

* मॉडल.एक्सएमएल

यह ध्यान दिया जाना चाहिए कि DACPAC में डेटा और अन्य सर्वर-स्तरीय ऑब्जेक्ट शामिल नहीं हैं। फ़ाइल में सभी ऑब्जेक्ट प्रकार हो सकते हैं जिन्हें SSDT प्रोजेक्ट में रखा जा सकता है।

## संदर्भ

* [डेटा टियर एप्लिकेशन - लाभ](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [डेटा टियर एप्लिकेशन की तैनाती - माइक्रोसॉफ्ट](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [DACPAC फ़ाइल कैसे बनाएं?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)

