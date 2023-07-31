{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "что такое файл xsd", "как открыть файл xsd", "расширение", "файл", "файл xsd", "формат файла xsd", "расширение .xsd" ,"пример файла xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Узнайте о формате файла XSD и API, которые могут создавать и открывать файл XSD.",
  "title" :"Формат файла XSD — файл определения схемы XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Что такое файл схемы XSD?

Файл XSD — это файл определения, определяющий элементы и атрибуты, которые могут быть частью документа XML. Это гарантирует правильную интерпретацию данных и обнаружение ошибок, что приводит к соответствующей проверке XML. Файлы XSD обеспечивают соответствие введенных данных той же структуре, которая определена в файле. Файлы XSD хранятся в формате [XML](/ru/web/xml/) и могут быть открыты или отредактированы в любом текстовом редакторе, таком как Блокнот Microsoft, Notepad++ или [Блокнот Microsoft XML](https://microsoft.github.io /XmlБлокнот/).

## Формат XSD-файла

Файлы XSD хранятся на диске в формате обычного текстового файла, который удобочитаем. XSD определяет элементы, которые можно использовать в документах, относящиеся к фактическим данным, с которыми он должен быть закодирован.

## Пример XSD-файла

Простой файл XSD со схемой заказа на покупку определяет элементы с помощью тегов, как показано в следующем [пример XSD от Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -простая-схема?view=vs-2022).

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

Здесь используются следующие теги.

* `xs:element` — определяет элемент.
* `xs:sequence` - Обозначает, что дочерние элементы появляются только в указанном порядке.
* `xs:complexType` - Обозначает, что он содержит другие элементы.
* `xs:simpleType` - Обозначает, что они не содержат других элементов.
* `тип` - строка, десятичное число, целое число, логическое значение, дата, время,

## Использованная литература ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [Пример XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

