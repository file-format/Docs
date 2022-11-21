{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "xsd फ़ाइल क्या है", "xsd फ़ाइल कैसे खोलें", "एक्सटेंशन", "फ़ाइल", "xsd फ़ाइल", "xsd फ़ाइल स्वरूप", ".xsd एक्सटेंशन" ,"xsd फ़ाइल उदाहरण"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XSD फ़ाइल स्वरूप और API के बारे में जानें जो XSD फ़ाइल बना और खोल सकते हैं।",
  "title" :"XSD फ़ाइल स्वरूप - XML स्कीमा परिभाषा फ़ाइल",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## XSD स्कीमा फ़ाइल क्या है?

एक एक्सएसडी फ़ाइल एक परिभाषा फ़ाइल है जो उन तत्वों और विशेषताओं को निर्दिष्ट करती है जो एक्सएमएल दस्तावेज़ का हिस्सा हो सकते हैं। यह सुनिश्चित करता है कि डेटा की ठीक से व्याख्या की गई है, और त्रुटियां पकड़ी गई हैं, जिसके परिणामस्वरूप उचित XML सत्यापन हुआ है। XSD फाइलें सुनिश्चित करती हैं कि दर्ज किया गया डेटा उसी संरचना का अनुसरण करता है जैसा कि फ़ाइल में परिभाषित किया गया है। XSD फ़ाइलें [XML](/hi/web/xml/) फ़ाइल फ़ॉर्मैट में स्टोर की जाती हैं और इन्हें Microsoft Notepad, Notepad++, या [Microsoft XML Notepad](https://microsoft.github.io) जैसे किसी भी टेक्स्ट एडिटर में खोला या संपादित किया जा सकता है / एक्सएमएल नोटपैड /)।

## एक्सएसडी फ़ाइल स्वरूप

XSD फ़ाइलें सादे पाठ फ़ाइल स्वरूप में डिस्क में संग्रहीत की जाती हैं जो मानव पठनीय है। एक एक्सएसडी उन तत्वों को परिभाषित करता है जिनका उपयोग दस्तावेज़ों में किया जा सकता है, वास्तविक डेटा से संबंधित जिसके साथ इसे एन्कोड किया जाना है।

## एक्सएसडी फ़ाइल का उदाहरण

खरीद ऑर्डर स्कीमा वाली एक साधारण XSD फ़ाइल टैग का उपयोग करने वाले तत्वों को परिभाषित करती है जैसा कि निम्नलिखित में दिखाया गया है [Microsoft द्वारा XSD उदाहरण] (https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file) -सरल-स्कीमा? देखें = बनाम-2022)।

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

यहाँ, निम्न टैग का उपयोग किया जाता है।

* `xs:element` - एक तत्व को परिभाषित करता है।
* `xs:sequence` - इंगित करता है कि बाल तत्व केवल उल्लिखित क्रम में दिखाई देते हैं।
* `xs:complexType` - दर्शाता है कि इसमें अन्य तत्व शामिल हैं।
* `xs: simpleType` - दर्शाता है कि उनमें अन्य तत्व नहीं हैं।
* `प्रकार` - स्ट्रिंग, दशमलव, पूर्णांक, बूलियन, दिनांक, समय,

## संदर्भ ##

- [माइक्रोसॉफ्ट एक्सएमएल नोटपैड](https://microsoft.github.io/XmlNotepad/)
- [XSD नमूना उदाहरण](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

