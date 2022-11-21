{
  "date" : "2021-12-09",
  "keywords" :[ "आसा", ".सा", "फ़ाइल प्रारूप", "फ़ाइल प्रकार", "एक .सा फ़ाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एएसए - एएसपी कॉन्फ़िगरेशन फ़ाइल",
  "description" :"ASA फ़ाइल और API क्या है, जो ASA फ़ाइलें बना और खोल सकता है, इसके बारे में जानें।",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## एएसए फाइल क्या है?

एक ASA फ़ाइल कॉन्फ़िगरेशन फ़ाइल है, जिसे [ASP](/hi/web/asp/)/ASP.NET प्रोजेक्ट्स के लिए बनाया गया है। इसमें चर, सम्‍मिलित और कार्यों की घोषणाएं शामिल हैं जो कि अनुप्रयोग में वैश्विक स्तर पर पहुंच योग्य हैं। परियोजना के सभी पृष्ठ इन चरों और कार्यों तक पहुँच सकते हैं, इस प्रकार इन्हें फिर से लिखने की आवश्यकता से बचा जा सकता है। ऐसा ही एक उदाहरण Global.asa पेज है जो अन्य ASP वेबसाइट पेजों द्वारा एक्सेस किए जाने के लिए रूट डायरेक्टरी में स्टोर किया जाता है। Global.asa फ़ाइलें वैकल्पिक हैं, लेकिन यदि उपयोग की जाती हैं, तो प्रत्येक एप्लिकेशन में केवल एक Global.asa फ़ाइल हो सकती है।

## एएसए फ़ाइल स्वरूप - अधिक जानकारी

एएसए फाइलें निम्नलिखित सूचनाओं के साथ सादा पाठ फाइलें हैं।

* आवेदन घटनाएँ
* सत्र घटनाएँ
* \<object> घोषणाओं
* टाइप लाइब्रेरी घोषणाएं
* #शामिल निर्देश

## एएसए फ़ाइल उदाहरण

एक Global.asa फ़ाइल कुछ इस तरह दिख सकती है।

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## संदर्भ

* [ASP Global.asa फ़ाइल - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

