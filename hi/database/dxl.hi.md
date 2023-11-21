{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"डीएक्सएल फ़ाइल प्रारूप और एपीआई के बारे में जानें जो डीटीएसएक्स फाइलें बना और खोल सकते हैं।",
  "title" :"DXL फ़ाइल स्वरूप - डोमिनोज़ XML भाषा फ़ाइल स्वरूप",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## DXL फ़ाइल क्या है?

DXL फ़ाइल एक XML आधारित डेटा संग्रहण फ़ाइल है जो एंटरप्राइज़ स्तर के व्यावसायिक सहयोग सॉफ़्टवेयर, लोटस डोमिनोज़ के लिए बनाई गई है। इसमें लोटस डोमिनोज़ डेटाबेस से संबंधित डेटा जैसे स्कीमा, डिज़ाइन तत्व, दृश्य, फॉर्म, दस्तावेज़ और स्वयं डेटाबेस डेटा शामिल है। [एक्सएमएल](/hi/वेब/एक्सएमएल/) एक सार्वभौमिक फ़ाइल प्रारूप है जिसे किसी भी प्रोग्रामिंग भाषा में लिखे गए सॉफ़्टवेयर एप्लिकेशन द्वारा पढ़ा जा सकता है। यह मानव-पठनीय भी है और इसे किसी भी टेक्स्ट एडिटर के साथ खोला जा सकता है। इसीलिए DXL फ़ाइलें विनिमेय फ़ाइल स्वरूप में डेटा निर्यात करने की क्षमता प्रदान करती हैं।

## डीएक्सएल फ़ाइल स्वरूप

DXL फ़ाइलें XML फ़ाइल स्वरूप में सहेजी जाती हैं और किसी भी प्रोग्रामिंग भाषा में लिखे गए एप्लिकेशन द्वारा आसानी से पढ़ी जा सकती हैं। ये फ़ाइलें XML टैग में डेटा और सेटिंग्स संग्रहीत करती हैं जो डेटा को वर्गीकृत करने के साथ-साथ उसे उचित क्रम में व्यवस्थित करती हैं

### डीएक्सएल आउटपुट उदाहरण

नोट्स दस्तावेज़ के लिए आउटपुट टेक्स्ट अंश आउटपुट निम्नलिखित है।

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## संदर्भ

* [डीएक्सएल प्रारूप - माइक्रोसॉफ्ट](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

