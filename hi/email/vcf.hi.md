{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"वीसीएफ - वर्चुअल संपर्क फ़ाइल",
  "description":"VCF फ़ाइल स्वरूप और API के बारे में जानें जो VCF फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## वीसीएफ फाइल क्या है?

VCF (वर्चुअल कार्ड फॉर्मेट) या vCard संपर्क जानकारी संग्रहीत करने के लिए एक डिजिटल फ़ाइल स्वरूप है। लोकप्रिय सूचना विनिमय अनुप्रयोगों के बीच डेटा इंटरचेंज के लिए प्रारूप का व्यापक रूप से उपयोग किया जाता है। अधिकांश ऑपरेटिंग सिस्टम जैसे विंडोज और मैकओएस इन फाइलों को बनाने और खोलने के लिए डिफ़ॉल्ट एप्लिकेशन के साथ आते हैं। एक एकल VCF फ़ाइल में एक या एक से अधिक संपर्कों की संपर्क जानकारी हो सकती है। एक वीसीएफ फ़ाइल में आम तौर पर कई अन्य क्षेत्रों के अलावा संपर्क का नाम, पता, फोन नंबर, ईमेल, जन्मदिन, फोटो और ऑडियो जैसी जानकारी होती है। ईमेल क्लाइंट और सेवाओं द्वारा समर्थित होने के कारण, vCard प्रारूप का उपयोग करके संपर्कों के हस्तांतरण के दौरान डेटा की कोई हानि नहीं होती है। वीसीएफ फ़ाइल प्रारूप के लिए मीडिया प्रकार टेक्स्ट/वीकार्ड है।

## वीसीएफ फ़ाइल प्रारूप

वीसीएफ फाइलें स्वभाव से पाठ्य हैं और मानव पठनीय हैं। इन्हें माइक्रोसॉफ्ट विंडोज़ पर नोटपैड और मैकोज़ पर टेक्स्टएडिट जैसे टेक्स्ट एडिटर्स में खोला जा सकता है। हालांकि, अगर फ़ाइल में कोई छवि है, तो वह टेक्स्ट एडिटर में दिखाई नहीं देगी।

[माइक्रोसॉफ्ट आउटलुक](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) के लिए समर्थन प्रदान करता है वीसीएफ फाइलें खोलने के साथ-साथ लोकप्रिय [एमएसजी] (/hi/ ईमेल / संदेश /) प्रारूप जैसे कई अन्य प्रारूपों में कनवर्ट करें। VCF फ़ाइल स्वरूप को समय के साथ संस्करण 2.1 से 4.0 तक बढ़ाया गया और फ़ाइल स्वरूप में विस्तृत जानकारी जोड़ दी गई। प्रारूप का उपयोग फोन संपर्कों को निर्यात करने और बाद में किसी अन्य डिवाइस में आयात करने के लिए भी किया जाता है।

{{< figure src="../VCF.png" alt="वीसीएफ फ़ाइल प्रारूप" >}}

### वीसीएफ 2.1 उदाहरण

संस्करण 2.1 का एक उदाहरण निम्नलिखित है।

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### वीसीएफ 3.0 उदाहरण

निम्नलिखित संस्करण 3.0 का एक उदाहरण है।

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### वीसीएफ 4.0 उदाहरण

निम्नलिखित संस्करण 4.0 का एक उदाहरण है।

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## संदर्भ

* [वीसीएफ - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/VCard)

