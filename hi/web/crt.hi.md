{
  "date" : "2019-10-11",
  "keywords" :["सीआरटी", "सीआरटी फ़ाइल", "सीआरटी फ़ाइल प्रारूप", "सीआरटी फ़ाइल प्रकार", "फ़ाइल", "प्रकार", "सीआरटी फ़ाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - सुरक्षा प्रमाणपत्र फ़ाइल स्वरूप",
  "description":"सीआरटी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो सीआरटी फाइलें बना और खोल सकते हैं।",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## सीआरटी फाइल क्या है?

.crt एक्सटेंशन वाली फ़ाइल एक सुरक्षा प्रमाणपत्र फ़ाइल है जिसका उपयोग सुरक्षित वेबसाइटों द्वारा वेब सर्वर से ब्राउज़र में सुरक्षित कनेक्शन स्थापित करने के लिए किया जाता है। सुरक्षित वेबसाइटें डेटा ट्रांसफर, लॉगिन, भुगतान कार्ड लेनदेन को सुरक्षित करना और साइट को सुरक्षित ब्राउज़िंग प्रदान करना संभव बनाती हैं। यदि आप एक सुरक्षित वेबसाइट खोलते हैं, तो आपको एड्रेस बार में "लॉक" आइकन दिखाई देता है। यदि आप उस पर क्लिक करते हैं, तो आप स्थापित प्रमाणपत्र का विवरण देख सकते हैं। Verisign और Thawte जैसी अंतर्राष्ट्रीय कंपनियाँ इन SSL प्रमाणपत्रों का वितरण करती हैं।

## सीआरटी फ़ाइल स्वरूप

CRT फाइलें ASCII प्रारूप में हैं और प्रमाणपत्र फ़ाइल की सामग्री को देखने के लिए किसी भी पाठ संपादक में खोली जा सकती हैं। यह X.509 प्रमाणन मानक का अनुसरण करता है जो प्रमाणपत्र की संरचना को परिभाषित करता है। यह उन डेटा फ़ील्ड्स को परिभाषित करता है जिन्हें एसएसएल प्रमाणपत्र में शामिल किया जाना चाहिए। CRT उन प्रमाणपत्रों के PEM प्रारूप से संबंधित है जो Base64 ASCII एन्कोडेड फ़ाइलें हैं।

### पीईएम फ़ाइल संरचना

एक PEM फ़ाइल में कई प्रमाणपत्र हो सकते हैं। ऐसी स्थिति में, PEM फ़ाइल में प्रत्येक प्रमाणपत्र निम्न संरचना का अनुसरण करता है।

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### सीआरटी फ़ाइल प्रारूप उदाहरण

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## संदर्भ ##

* [सार्वजनिक कुंजी, निजी कुंजी और प्रमाणपत्र](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

