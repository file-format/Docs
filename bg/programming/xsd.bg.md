{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "какво е xsd файл", "как да отворите xsd файл", "разширение", "файл", "xsd файл", "xsd файлов формат", ".xsd разширение" ,"xsd файл пример"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Научете за файловия формат XSD и API, които могат да създават и отварят XSD файл.",
  "title" :"XSD файлов формат – файл с дефиниция на XML схема",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Какво е файл със схема на XSD?

XSD файлът е дефиниционен файл, указващ елементите и атрибутите, които могат да бъдат част от XML документ. Това гарантира, че данните се интерпретират правилно и грешките се улавят, което води до подходящо валидиране на XML. XSD файловете гарантират, че въведените данни следват същата структура, както е дефинирана във файла. XSD файловете се съхраняват във файлов формат [XML](/bg/web/xml/) и могат да се отварят или редактират във всеки текстов редактор като Microsoft Notepad, Notepad++ или [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## XSD файлов формат

XSD файловете се съхраняват на диск във формат на обикновен текстов файл, който е четим от хора. XSD дефинира елементите, които могат да се използват в документите, свързани с действителните данни, с които той трябва да бъде кодиран.

## Пример за XSD файл

Прост XSD файл със схема на поръчка за покупка дефинира елементите с помощта на тагове, както е показано в следния [XSD пример от Microsoft](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -проста схема?view=vs-2022).

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

Тук се използват следните тагове.

* `xs:element` - Дефинира елемент.
* `xs:sequence` - Означава, че дъщерните елементи се появяват само в посочения ред.
* `xs:complexType` - Указва, че съдържа други елементи.
* `xs:simpleType` - Указва, че не съдържат други елементи.
* `тип` - низ, десетичен, цяло число, булево, дата, час,

## Препратки ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD примерен пример](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

