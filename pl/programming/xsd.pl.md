{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "co to jest plik xsd", "jak otworzyć plik xsd", "rozszerzenie", "plik", "plik xsd", "format pliku xsd", "rozszerzenie .xsd" ,"przykład pliku xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Dowiedz się więcej o formacie pliku XSD i interfejsach API, które mogą tworzyć i otwierać plik XSD.",
  "title" :"Format pliku XSD - plik definicji schematu XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Co to jest plik schematu XSD?

Plik XSD to plik definicji określający elementy i atrybuty, które mogą być częścią dokumentu XML. Zapewnia to prawidłową interpretację danych i wychwytywanie błędów, co skutkuje odpowiednią walidacją XML. Pliki XSD zapewniają, że wprowadzone dane mają taką samą strukturę, jak zdefiniowano w pliku. Pliki XSD są przechowywane w formacie [XML](/pl/web/xml/) i można je otwierać lub edytować w dowolnym edytorze tekstu, takim jak Microsoft Notepad, Notepad++ lub [Microsoft XML Notepad](https://microsoft.github.io /XmlNotatnik/).

## Format pliku XSD

Pliki XSD są zapisywane na dysku w formacie zwykłego pliku tekstowego, który jest czytelny dla człowieka. XSD definiuje elementy, które mogą być użyte w dokumentach, odnoszące się do rzeczywistych danych, z którymi ma być zakodowany.

## Przykład pliku XSD

Prosty plik XSD ze schematem zamówienia definiuje elementy przy użyciu tagów, jak pokazano w poniższym [przykładzie XSD firmy Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

Tutaj używane są następujące tagi.

* `xs:element` - Definiuje element.
* `xs:sequence` — oznacza, że elementy potomne pojawiają się tylko we wspomnianej kolejności.
* `xs:complexType` — oznacza, że zawiera inne elementy.
* `xs:simpleType` — oznacza, że nie zawierają innych elementów.
* `type` - string, dziesiętny, integer, boolean, data, czas,

## Bibliografia ##

- [Notatnik Microsoft XML](https://microsoft.github.io/XmlNotepad/)
- [Przykładowy przykład XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

