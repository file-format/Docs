{
  "date": "2022-02-06",
  "keywords": [
"xsd",
".xsd",
"hvad er en xsd-fil",
"hvordan man åbner xsd fil",
"udvidelse",
"fil",
"xsd-fil",
"xsd filformat",
".xsd udvidelse",
"xsd fil eksempel"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": " Lær om XSD-filformat og API'er, der kan oprette og åbne en XSD-fil.",
  "title": "XSD-filformat - XML-skemadefinitionsfil",
  "linktitle": "XSD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-xs-dad"
}
},
  "lastmod": "2022-02-06"
}

## Hvad er en XSD Schema fil?

En XSD-fil er en definitionsfil, der specificerer de elementer og attributter, der kan være en del af et XML-dokument. Dette sikrer, at data fortolkes korrekt, og at fejl fanges, hvilket resulterer i passende XML-validering. XSD-filer sikrer, at de indtastede data følger samme struktur som defineret i filen. XSD-filer gemmes i filformatet [XML](/web/xml/) og kan åbnes eller redigeres i et hvilket som helst tekstredigeringsprogram såsom Microsoft Notesblok, Notesblok++ eller [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/).

## XSD filformat

XSD-filer gemmes på en disk i almindeligt tekstfilformat, der kan læses af mennesker. En XSD definerer de elementer, der kan bruges i dokumenterne, relateret til de faktiske data, som det skal kodes med.

## Eksempel på XSD-fil

En simpel XSD-fil med et indkøbsordreskema definerer elementerne ved hjælp af tags som vist i følgende [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

Her bruges følgende tags.

 * `xs:element` - Definerer et element.
 * `xs:sequence` - Angiver underordnede elementer, der kun vises i den nævnte rækkefølge.
 * `xs:complexType` - Angiver, at den indeholder andre elementer.
 * `xs:simpleType` - Angiver, at de ikke indeholder andre elementer.
 * type - streng, decimal, heltal, boolesk, dato, tid,

## Referencer ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

