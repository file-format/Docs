{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FZP फ़ाइल स्वरूप और API के बारे में जानें जो FZP फ़ाइलें बना और खोल सकते हैं।",
  "title" :"FZP फ़ाइल स्वरूप - फ्रिटिंग XML भाग विवरण फ़ाइल",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## FZP फाइल क्या है?

FZP फ़ाइल [Fritzing](https://fritzing.org/) इलेक्ट्रॉनिक सर्किट प्रोटोटाइप और डिज़ाइन एप्लिकेशन द्वारा बनाई गई एक XML फ़ाइल है। इसमें [XML](/hi/web/xml/) फ़ाइल स्वरूप में भाग के गुणों, कनेक्टर्स और बसों के बारे में जानकारी शामिल है। FPZ फ़ाइलों को फ्रिट्ज़िंग में स्वतंत्र रूप से उपयोग नहीं किया जा सकता है। इसके बजाय, उन्हें FZPZ संग्रह फ़ाइल के भाग के रूप में आयात किया जाता है।

## FZP फ़ाइल स्वरूप - अधिक जानकारी

FZP फाइलें XML फाइलें होती हैं जिनमें भाग के गुणों, कनेक्टर्स और बसों के बारे में जानकारी होती है। इनके अलावा, FZP फाइलों में शीर्षक, विवरण, लेखक और FZP फ़ाइल के प्रकाशन की तारीख के बारे में भी जानकारी होती है। जब एक फ़्रिट्ज़िंग भाग फ़ाइल निर्यात की जाती है, तो फ़्रिट्ज़िंग ऐप एक [FZPZ](/hi/compression/fzpz/) संपीड़ित संग्रह बनाता है जिसमें एक FZP फ़ाइल और चार [SVG](/hi/page-description-language/svg/) फ़ाइलें होती हैं।

[FZP फ़ाइल प्रारूप विनिर्देश](https://github.com/fritzing/fzp/blob/master/docs/README.md) फ्रिट्ज़िंग द्वारा जीथब पर उपलब्ध हैं।

## FZP फ़ाइल संरचना उदाहरण

एक विशिष्ट FZP फ़ाइल में निम्न XML संरचना होती है।

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## संदर्भ

* [FZP फ़ाइल प्रारूप निर्दिष्टीकरण](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [fzpz एक्सटेंशन के साथ नए हिस्से](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

