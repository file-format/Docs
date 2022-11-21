
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"विज्ञापन फ़ाइल - एडीए विशिष्टता फ़ाइल स्वरूप",
  "description":"एडीएस फ़ाइल प्रारूप क्या है, उदाहरण और एपीआई के बारे में जानें जो एडीएस फाइलें बना और खोल सकते हैं।",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## एडीएस फ़ाइल क्या है?

ADS फ़ाइल एक Ada प्रोग्रामिंग प्रोजेक्ट के लिए एक विनिर्देश फ़ाइल है। यह जावा के लिए एक वर्ग के समान है, या सी ++ के मामले में शीर्षलेख और कार्यान्वयन जोड़ी है। Ada पैकेज के सार्वजनिक और निजी विनिर्देशों को .ads फ़ाइल में संग्रहित किया जाता है। इसके विपरीत, .adb फ़ाइल में कार्यान्वयन, या Ada निकाय शामिल हैं। [C++](/hi/ प्रोग्रामिंग/cpp/) की तरह, Ada OOP से स्वतंत्र विनिर्देशों और कार्यान्वयन के बीच अलगाव प्रदान करता है।

ADS फाइलें किसी भी टेक्स्ट एडिटर जैसे Microsoft Notepad, Notepad++ और Atom में खोली जा सकती हैं।

## एडीएस फ़ाइल स्वरूप

ADS फाइलें सरल सादे पाठ फ़ाइल प्रारूप में हैं और इन्हें किसी भी पाठ संपादक के साथ खोला/संपादित किया जा सकता है। Ada संकुल को पदानुक्रम में व्यवस्थित किया जा सकता है। एक चाइल्ड यूनिट को निम्न तरीके से घोषित किया जा सकता है:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## संदर्भ

* [एडीए पैकेज](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

