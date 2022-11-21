{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"सीएसआर फाइल - सर्टिफिकेट साइनिंग रिक्वेस्ट फाइल फॉर्मेट",
  "description" :"सीएसआर फ़ाइल और एपीआई क्या है, इसके बारे में जानें, जो सीएसआर फाइलें बना और खोल सकता है।",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## सीएसआर फाइल क्या है?

सीएसआर फाइल एक **सर्टिफिकेट साइनिंग रिक्वेस्ट** फाइल होती है, जिसका इस्तेमाल एसएसएल/टीएलएस सर्टिफिकेट के लिए अनुरोध करने के लिए किया जाता है। जब आपको अपने एसएसएल/टीएलएस प्रमाणपत्र की आवश्यकता होती है, तो आप उसी सर्वर पर सीएसआर उत्पन्न करते हैं जहां इसे अंततः स्थापित किया जाएगा। यह सीएसआर फाइल सर्टिफिकेट बनाने के लिए सर्टिफिकेट अथॉरिटी (सीए) के साथ साझा की जाती है। इसमें सामान्य नाम, संगठन, देश, और, अधिक महत्वपूर्ण रूप से, **सार्वजनिक कुंजी** जैसी जानकारी होती है, जो आपकी प्रमाणपत्र फ़ाइल में एकीकृत होती है और संबंधित निजी कुंजी के साथ हस्ताक्षरित होती है।

वे एप्लिकेशन जो **CSR फ़ाइलें खोल सकते हैं** में OpenSSL और Microsoft IIS शामिल हैं।

## प्रमाणपत्र हस्ताक्षर अनुरोध फ़ाइल स्वरूप

एक CSR फाइल बेस-64 PEM फॉर्मेट में बनाई जाती है जिसे माइक्रोसॉफ्ट नोटपैड जैसे साधारण टेक्स्ट एडिटर में खोला और देखा जा सकता है। इसमें एक शीर्षलेख शामिल है **-----नया प्रमाणपत्र अनुरोध शुरू करें-----** फ़ाइल की शुरुआत में और एक पादलेख **-----नया प्रमाणपत्र अनुरोध समाप्त करें-----** पर फ़ाइल का अंत।

### सीएसआर फ़ाइल कैसी दिखती है?

CSR फ़ाइल का एक सरल उदाहरण इस प्रकार है।

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## सीएसआर में कौन सी जानकारी शामिल होती है?

एक सीएसआर फ़ाइल में निम्नलिखित जानकारी होती है।

1. 'व्यवसाय और वेबसाइट के बारे में जानकारी' - इसमें सामान्य नाम, संगठन, संगठनात्मक इकाई, शहर/इलाका, राज्य/काउंटी/क्षेत्र (एस), देश और ईमेल पता जैसी जानकारी शामिल है
1. `सार्वजनिक कुंजी` - यह प्रमाणपत्र में शामिल है और प्रेषित डेटा को एन्क्रिप्ट करने के लिए उपयोग किया जाता है जिसे संबंधित निजी कुंजी का उपयोग करके डिक्रिप्ट किया जाता है
1. `कुंजी प्रकार और लंबाई के बारे में जानकारी` - यह आम तौर पर आरएसए 2048 है लेकिन यह बड़े आकार में भी आ सकता है जैसे आरएसए 4096+

## संदर्भ

* [संकल्पना अनुप्रयोग सर्वर] (https://github.com/Devronium/ConceptApplicationServer)

