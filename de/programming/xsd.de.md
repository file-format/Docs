{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "was ist eine xsd-Datei", "wie man eine xsd-Datei öffnet", "Erweiterung", "Datei", "xsd-Datei", "xsd-Dateiformat", ".xsd-Erweiterung" ,"XSD-Dateibeispiel"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Erfahren Sie mehr über das XSD-Dateiformat und APIs, die eine XSD-Datei erstellen und öffnen können.",
  "title" :"XSD-Dateiformat - XML-Schema-Definitionsdatei",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Was ist eine XSD-Schemadatei?

Eine XSD-Datei ist eine Definitionsdatei, die die Elemente und Attribute angibt, die Teil eines XML-Dokuments sein können. Dadurch wird sichergestellt, dass Daten richtig interpretiert und Fehler abgefangen werden, was zu einer angemessenen XML-Validierung führt. XSD-Dateien stellen sicher, dass die eingegebenen Daten der gleichen Struktur folgen, wie sie in der Datei definiert ist. XSD-Dateien werden im Dateiformat [XML](/de/web/xml/) gespeichert und können in jedem Texteditor wie Microsoft Notepad, Notepad++ oder [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## XSD-Dateiformat

XSD-Dateien werden im Nur-Text-Dateiformat auf der Disc gespeichert, das für Menschen lesbar ist. Ein XSD definiert die Elemente, die in den Dokumenten verwendet werden können, bezogen auf die eigentlichen Daten, mit denen es codiert werden soll.

## Beispiel einer XSD-Datei

Eine einfache XSD-Datei mit einem Bestellschema definiert die Elemente mithilfe von Tags, wie im folgenden [XSD-Beispiel von Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022).

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

Hier werden die folgenden Tags verwendet.

* `xs:element` - Definiert ein Element.
* `xs:sequence` - Bezeichnet untergeordnete Elemente, die nur in der angegebenen Reihenfolge erscheinen.
* `xs:complexType` - Zeigt an, dass es andere Elemente enthält.
* `xs:simpleType` - Gibt an, dass sie keine anderen Elemente enthalten.
* "Typ" - Zeichenfolge, Dezimalzahl, Ganzzahl, Boolean, Datum, Uhrzeit,

## Verweise ##

- [Microsoft XML-Editor](https://microsoft.github.io/XmlNotepad/)
- [XSD-Beispielbeispiel](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

