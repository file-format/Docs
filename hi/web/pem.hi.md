{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"पीईएम फाइल - प्राइवेसी एन्हांस्ड मेल सर्टिफिकेट फाइल फॉर्मेट",
  "description":"PEM फ़ाइल स्वरूप और API के बारे में जानें जो PEM फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## पीईएम फाइल क्या है?

PEM फ़ाइल एक सुरक्षा प्रमाणपत्र फ़ाइल है जिसका उपयोग वेब सर्वर और ब्राउज़र के बीच एक सुरक्षित संचार चैनल स्थापित करने के लिए किया जाता है। यह बेस 64-एन्कोडेड है और इसमें एक निजी कुंजी, सर्वर प्रमाणपत्र और/या अन्य प्रमाणपत्रों का संयोजन हो सकता है। PEM फाइलें उपयोग के संदर्भ में .der प्रमाणपत्र फ़ाइलों के समान हैं लेकिन बाइनरी डेटा के बजाय बेस 64-एन्कोडेड टेक्स्ट के रूप में संग्रहीत की जाती हैं। अन्य समान प्रमाणपत्र फ़ाइल स्वरूपों में [.cer](/hi/web/cer/) और [.crt](/hi/web/crt/) फ़ाइलें शामिल हैं।

वे एप्लिकेशन जो **PEM फ़ाइलें खोल सकते हैं** उनमें टेक्स्ट संपादक जैसे Microsoft Notepad और Apple TextEdit शामिल हैं।

## पीईएम फ़ाइल प्रारूप

PEM एक कंटेनर फ़ाइल स्वरूप है जो डेटा को संग्रहीत करने के लिए उपयोग की जाने वाली फ़ाइल की संरचना और एन्कोडिंग प्रकार को परिभाषित करता है। PEM फ़ाइलों को बेस 64-एन्कोडेड फ़ाइल स्वरूप के रूप में डिस्क में संग्रहीत किया जाता है जो मानव-पठनीय नहीं है। मानक परिभाषित करता है कि एक पीईएम फ़ाइल इसके साथ शुरू होती है:

```
-----BEGIN <type>-----
```
और इसके साथ समाप्त होता है:
```
-----END <type>-----
```

इनके अंदर अन्य सभी सामग्री बेस 64 एन्कोडेड (अपरकेस और लोअरकेस अक्षर, अंक, +, और /) हैं। एक एकल पीईएम फ़ाइल में कई ब्लॉक शामिल हो सकते हैं जिनका उपयोग अन्य कार्यक्रमों द्वारा किया जा सकता है। यदि एक पीईएम फ़ाइल में कई प्रमाणपत्र हैं, तो प्रत्येक प्रमाणपत्र को अलग-अलग ब्लॉकों द्वारा निम्नानुसार अलग किया जाता है:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### पीईएम फ़ाइल उदाहरण

CERTIFICATE ब्लॉक वाली एक PEM फाइल आमतौर पर निम्नलिखित की तरह दिखती है:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

आरएसए के साथ एक पीईएम फ़ाइल निम्न की तरह शुरू होती है।

```
-----BEGIN RSA PRIVATE KEY-----
```

## संदर्भ ##

* [सार्वजनिक कुंजी क्रिप्टोग्राफी](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [पी7सी फाइल कैसे बनाएं?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

