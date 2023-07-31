{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "що таке файл xsd", "як відкрити файл xsd", "розширення", "файл", "файл xsd", "формат файлу xsd", "розширення .xsd" ,"приклад файлу xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Дізнайтеся про формат файлу XSD та API, які можуть створювати та відкривати файл XSD.",
  "title" :"Формат файлу XSD - файл визначення схеми XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Що таке файл схеми XSD?

Файл XSD — це файл визначення, який визначає елементи й атрибути, які можуть бути частиною документа XML. Це гарантує правильну інтерпретацію даних і виявлення помилок, що призводить до належної перевірки XML. Файли XSD гарантують, що введені дані відповідають тій же структурі, що визначена у файлі. Файли XSD зберігаються у форматі [XML](/uk/web/xml/) і їх можна відкривати або редагувати в будь-якому текстовому редакторі, наприклад Microsoft Notepad, Notepad++ або [Microsoft XML Notepad](https://microsoft.github.io). /XmlNotepad/).

## Формат файлу XSD

Файли XSD зберігаються на диску у форматі звичайного текстового файлу, який легко читається людиною. XSD визначає елементи, які можна використовувати в документах, пов’язані з фактичними даними, якими він має бути закодований.

## Приклад файлу XSD

Простий файл XSD зі схемою замовлення на купівлю визначає елементи за допомогою тегів, як показано в наведеному нижче [прикладі XSD від Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

Тут використовуються такі теги.

* `xs:element` - визначає елемент.
* `xs:sequence` – позначає, що дочірні елементи з’являються лише у зазначеному порядку.
* `xs:complexType` - означає, що містить інші елементи.
* `xs:simpleType` - означає, що вони не містять інших елементів.
* `тип` - рядок, десяткове число, ціле число, логічний вираз, дата, час,

## Посилання ##

- [Блокнот Microsoft XML](https://microsoft.github.io/XmlNotepad/)
- [Приклад прикладу XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

