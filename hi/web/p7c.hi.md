{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 प्रमाणपत्र फ़ाइल",
  "description":"P7C फ़ाइल स्वरूप और API के बारे में जानें जो P7C फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## P7C फ़ाइल क्या है?

एक P7C फ़ाइल, अन्य सुरक्षा प्रमाणपत्र फ़ाइलों की तरह, एक डिजिटल प्रमाणपत्र है जिसका उपयोग नेटवर्क पर पहचान को प्रमाणित करने के लिए किया जाता है। प्रमाणपत्रों का उपयोग करने वाले एप्लिकेशन इन प्रमाणपत्र फ़ाइलों में शामिल सार्वजनिक कुंजी का उपयोग करके पहचान को प्रमाणित करते हैं। सार्वजनिक-कुंजी क्रिप्टोग्राफी, या असममित क्रिप्टोग्राफी, कुंजियों की जोड़ी का उपयोग करती है जिनमें से एक सार्वजनिक कुंजी है और दूसरी निजी कुंजी के रूप में जानी जाती है। प्रभावी सुरक्षा के लिए निजी कुंजी को सुरक्षित रखा जाता है, जबकि सार्वजनिक कुंजी को दूसरों के साथ साझा किया जा सकता है। अन्य सामान्य प्रमाणपत्र फ़ाइल स्वरूपों में [CRT](/hi/web/crt/), DER, और PEM शामिल हैं।

## P7C फ़ाइल स्वरूप - अधिक जानकारी

P7C फाइलें बाइनरी फाइलों के रूप में डिस्क में सहेजी जाती हैं और इसमें गणितीय समस्याओं के आधार पर क्रिप्टोग्राफिक एल्गोरिदम का उपयोग करके उत्पन्न सार्वजनिक कुंजी जानकारी शामिल होती है। इन्हें किसी भी टेक्स्ट एडिटर में खोला जा सकता है लेकिन इनकी सामग्री मानव पठनीय रूप में नहीं है। कुछ एप्लिकेशन जो P7C फाइलें खोल सकते हैं उनमें Apple कीचेन एक्सेस, Adobe Acrobat Reader DC, Microsoft प्रमाणपत्र प्रबंधक और Microsoft Windows संपर्क शामिल हैं।

### P7C फ़ाइल स्वरूप उदाहरण

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## संदर्भ ##

* [सार्वजनिक कुंजी क्रिप्टोग्राफी](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C फाइल कैसे बनाएं?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

