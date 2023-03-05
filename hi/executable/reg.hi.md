{
  "date" : "2021-08-02",
  "keywords" :[ "reg फ़ाइल", "reg फ़ाइल स्वरूप", "एक reg फ़ाइल क्या है", "फ़ाइल", "reg उदाहरण", "reg फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"REG फ़ाइल स्वरूप और API के बारे में जानें जो REG फ़ाइलें बना और खोल सकते हैं।",
  "title" :"आरईजी - विंडोज रजिस्ट्री फाइल",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## एक आरईजी फाइल क्या है?
एक REG फ़ाइल केवल .reg एक्सटेंशन वाली एक टेक्स्ट फ़ाइल है। ये फ़ाइलें आमतौर पर रजिस्ट्री से विशिष्ट कुंजियों को निर्यात करके बनाई जाती हैं। इन फ़ाइलों का उपयोग रजिस्ट्री के बैकअप के रूप में भी किया जा सकता है (विशेषकर परिवर्तन करने से पहले यह चरण महत्वपूर्ण है!) आप देख सकते हैं कि कुछ ने उन्हें उन्हीं साइटों पर डाउनलोड करने योग्य फ़ाइलों के रूप में उपलब्ध कराया जो आपको रजिस्ट्री हैक करने का तरीका दिखाती हैं। एक REG फ़ाइल रजिस्ट्री में मैन्युअल परिवर्तन करने और उन परिवर्तनों को निर्यात करने में उपयोगी होती है। बस फ़ाइल को थोड़ा सा साफ़ करें और फिर इसे दूसरों के साथ साझा करें।

## आरईजी फ़ाइल प्रारूप
REG फ़ाइल स्वरूप को INI-आधारित सिंटैक्स का उपयोग करके Windows रजिस्ट्री के कुछ हिस्सों को निर्यात और आयात करने के लिए डिज़ाइन किया गया था। विंडोज रजिस्ट्री एक रिलेशनल या पदानुक्रमित डेटाबेस है जो माइक्रोसॉफ्ट विंडोज ऑपरेटिंग सिस्टम और विंडोज रजिस्ट्री का उपयोग करने वाले अन्य अनुप्रयोगों के लिए निम्न-स्तरीय सेटिंग्स रखता है। अल्टरनेटिवली, हम कह सकते हैं, रजिस्ट्री या विंडोज रजिस्ट्री में माइक्रोसॉफ्ट विंडोज ऑपरेटिंग सिस्टम के सभी संस्करणों पर स्थापित प्रोग्राम और हार्डवेयर के लिए जानकारी, विकल्प, सेटिंग्स और अन्य मान शामिल हैं।
### REG फ़ाइल का सिंटैक्स
REG फ़ाइल सिंटैक्स के भाग के रूप में यहाँ कुछ प्रमुख तत्व दिए गए हैं:
- **RegistryEditorVersion**: जैसे "Windows रजिस्ट्री संपादक संस्करण 5.00" Windows 2000, Windows XP और Windows Server 2003 के लिए।
- **ब्लैंक लाइन**: एक नए रजिस्ट्री पथ की शुरुआत की पहचान करता है।
- **RegistryPathx**: उपकुंजी का पथ जिसमें आपके द्वारा आयात किया जा रहा पहला मान है।
- **DataItemNamex**: उस डेटा आइटम का नाम जिसे आप आयात करना चाहते हैं।
- **डेटाटाइप**: रजिस्ट्री मान के लिए डेटा प्रकार।

कुंजियों को निम्न सिंटैक्स का उपयोग करके .reg फ़ाइलों में संग्रहीत किया जाता है:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
आप "मान नाम" के बजाय "@" का उपयोग करके किसी कुंजी के डिफ़ॉल्ट मान को संपादित कर सकते हैं:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### उदाहरण
यहाँ REG फ़ाइल का एक उदाहरण है
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## संदर्भ

* [विंडो रजिस्ट्री- विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/Windows_Registry)
* [.reg फ़ाइल का उपयोग करके रजिस्ट्री उपकुंजियों और मानों को कैसे जोड़ें, संशोधित करें या हटाएं](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
