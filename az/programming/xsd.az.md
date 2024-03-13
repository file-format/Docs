{
  "date": "2022-02-06",
  "keywords": [
"xsd",
".xsd",
"xsd faylı nədir",
"xsd faylını necə açmaq olar",
"uzadılması",
"fayl",
"xsd faylı",
"xsd fayl formatı",
".xsd uzantısı",
"xsd fayl nümunəsi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": " XSD faylı yarada və aça bilən XSD fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "XSD Fayl Format - XML Sxema Tərif Faylı",
  "linktitle": "XSD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-xs-azd"
}
},
  "lastmod": "2022-02-06"
}

## XSD Şema faylı nədir?

XSD faylı XML sənədinin bir hissəsi ola biləcək elementləri və atributları təyin edən tərif faylıdır. Bu, məlumatların düzgün şərh edilməsini və səhvlərin tutulmasını təmin edir, nəticədə müvafiq XML təsdiqi olur. XSD faylları daxil edilmiş məlumatların faylda müəyyən edilmiş struktura uyğun olmasını təmin edir. XSD faylları [XML](/web/xml/) fayl formatında saxlanılır və Microsoft Notepad, Notepad++ və ya [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/) kimi istənilən mətn redaktorunda açıla və ya redaktə edilə bilər.

## XSD fayl formatı

XSD faylları diskdə insanların oxuna biləcəyi düz mətn faylı formatında saxlanılır. XSD, kodlaşdırılmalı olduğu faktiki məlumatla bağlı sənədlərdə istifadə oluna bilən elementləri müəyyən edir.

## XSD faylının nümunəsi

Satınalma sifarişi sxeminə malik sadə XSD faylı aşağıdakı [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)-də göstərildiyi kimi teqlərdən istifadə edən elementləri müəyyən edir.

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

Burada aşağıdakı etiketlərdən istifadə olunur.

 * `xs:element` - Elementi müəyyənləşdirir.
 * `xs:sequence` - Alt elementlərin yalnız qeyd olunan ardıcıllıqla göründüyünü bildirir.
 * `xs:complexType` - digər elementləri ehtiva etdiyini bildirir.
 * `xs:simpleType` - digər elementləri ehtiva etmədiyini bildirir.
 * `tip` - sətir, onluq, tam, mantiq, tarix, vaxt,

## İstinadlar ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

