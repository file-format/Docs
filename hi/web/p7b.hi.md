{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7 प्रमाणपत्र फ़ाइल",
  "description":"P7C फ़ाइल स्वरूप और API के बारे में जानें जो P7C फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## P7B फ़ाइल क्या है?

P7B फ़ाइल एक सुरक्षा प्रमाणपत्र फ़ाइल है जिसमें किसी व्यक्ति या डिवाइस को प्रमाणित करने के लिए सुरक्षित डिजिटल प्रमाणपत्र होता है। [.cer](/hi/web/cer/) प्रमाणपत्र फ़ाइल के समान, फ़ाइल पर राइट क्लिक विकल्प का उपयोग करके "प्रमाणपत्र स्थापित करें" विकल्प का उपयोग करके एक P7B फ़ाइल स्थापित की जा सकती है। P7B CER फ़ाइल फ़ॉर्मेट की तुलना में भिन्न फ़ॉर्मेटिंग विकल्प का उपयोग करता है। इसमें एक या अधिक X.509 डिजिटल प्रमाणपत्र फ़ाइलें हैं जो बेस64 (ASCII) एन्कोडिंग का उपयोग करती हैं। P7B फाइलें [ZIP](/hi/compression/zip/) फाइल के रूप में प्राप्त होती हैं या सर्टिफिकेट अथॉरिटी से प्राप्त होती हैं।

## P7B फ़ाइल स्वरूप

P7B फाइलें सादे ASCII फाइलों के रूप में संग्रहित की जाती हैं जिन्हें किसी भी टेक्स्ट एडिटर में खोला जा सकता है। इसमें सार्वजनिक कुंजी होती है जो एक एन्कोडेड स्ट्रिंग है जो पठनीयता के दृष्टिकोण से अर्थहीन है।

### P7B फ़ाइल स्वरूप उदाहरण

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## संदर्भ ##

* [सार्वजनिक कुंजी क्रिप्टोग्राफी](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [पी7सी फाइल कैसे बनाएं?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

