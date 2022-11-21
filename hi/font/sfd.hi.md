{
  "date" : "2020-08-20",
  "keywords" :[ "sdf फ़ाइल", "sdf फ़ाइल स्वरूप", "sdf फ़ाइल क्या है", "फ़ाइल", "sdf उदाहरण", "sdf फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - तख़्ता फ़ॉन्ट डेटाबेस स्वरूप",
  "description":"एसएफडी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एसएफडी फाइलें बना और खोल सकते हैं।",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## एसएफडी फाइल क्या है?

.sfd (स्पलाइन फॉन्ट डेटाबेस) एक्सटेंशन वाली फाइल फॉन्ट एडिटिंग सॉफ्टवेयर - FontForge के लिए मूल ASCII फॉन्ट फॉर्मेट है। सॉफ्टवेयर कई अन्य सामान्य फ़ॉन्ट स्वरूपों का समर्थन करता है और स्वतंत्र रूप से उपलब्ध है। सॉफ्टवेयर का उपयोग लिनक्स, विंडोज और मैकओएस सहित लगभग सभी आधुनिक ऑपरेटिंग सिस्टम के लिए किया जा सकता है।

## **एसएफडी फ़ाइल प्रारूप**
एसएफडी फाइलें एएससीआईआई फाइलें हैं जो मानव पठनीय हैं और आसानी से इंटरनेट पर स्थानांतरित हो जाती हैं। इसे application/vnd.font-fontforget-sfd द्वारा इसके MIME प्रकार के रूप में पहचाना जाता है।

### हैडर
एक सामान्य SFD फ़ाइल हेडर निम्न उदाहरण में दिखाया गया है।

```
SplineFontDB: 3.0
FontName: Ambrosia
FullName: Ambrosia
FamilyName: Ambrosia
DefaultBaseFilename: Ambrosia-1.0
Weight: Medium
Copyright: Copyright (C) 1995-2000 by George Williams
Comments: This is a funny font.
UComments: "This is a funny font."
FontLog: "Create Jan 2008"
Version: 001.000
ItalicAngle: 0
UnderlinePosition: -133
UnderlineWidth: 20
Ascent: 800
Descent: 200
sfntRevision: 0x00078106
WidthSeparation: 140
LayerCount: 4
Layer: 0 0 "Back" 1
Layer: 1 1 "Fore" 0
Layer: 2 0 "Cubic_Fore" 0
Layer: 3 0 "Test" 1
DisplaySize: -24
DisplayLayer: 1
AntiAlias: 1
WinInfo: 64 16 4
FitToEm: 1
UseUniqueID: 0
UseXUID: 1
XUID: 3 18 21
Encoding: unicode
Order2: 1
OnlyBitmaps: 0
MacStyle: 0
TeXData: 1 10485760 0 269484 134742 89828 526385 1048576 89828
CreationTime: 1151539072
ModificationTime: 11516487392
GaspTable 3 8 2 16 1 65535 3 0
DEI: 91125
ExtremaBound: 30
```


## **संदर्भ**

* [FontForge द्वारा SFD फ़ाइल स्वरूप](https://fontforge.org/docs/techref/sfdformat.html)

