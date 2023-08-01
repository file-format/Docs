{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "wat is een xsd-bestand", "hoe een xsd-bestand te openen", "extensie", "bestand", "xsd-bestand", "xsd-bestandsformaat", ".xsd-extensie" ,"xsd-bestandsvoorbeeld"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Meer informatie over XSD-bestandsindeling en API's die een XSD-bestand kunnen maken en openen.",
  "title" :"XSD-bestandsindeling - XML-schemadefinitiebestand",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Wat is een XSD Schema-bestand?

Een XSD-bestand is een definitiebestand dat de elementen en attributen specificeert die deel kunnen uitmaken van een XML-document. Dit zorgt ervoor dat gegevens correct worden geïnterpreteerd en dat fouten worden opgevangen, wat resulteert in de juiste XML-validatie. XSD-bestanden zorgen ervoor dat de ingevoerde gegevens dezelfde structuur volgen als gedefinieerd in het bestand. XSD-bestanden worden opgeslagen in de bestandsindeling [XML](/nl/web/xml/) en kunnen worden geopend of bewerkt in elke teksteditor zoals Microsoft Notepad, Notepad++ of [Microsoft XML Notepad](https://microsoft.github.io /XmlKladblok/).

## XSD-bestandsindeling

XSD-bestanden worden op schijf opgeslagen in platte tekstbestandsindeling die voor mensen leesbaar is. Een XSD definieert de elementen die in de documenten kunnen worden gebruikt, met betrekking tot de feitelijke gegevens waarmee het moet worden gecodeerd.

## Voorbeeld van XSD-bestand

Een eenvoudig XSD-bestand met een inkooporderschema definieert de elementen met behulp van tags zoals weergegeven in het volgende [XSD-voorbeeld door Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

Hier worden de volgende tags gebruikt.

* `xs:element` - Definieert een element.
* `xs:sequence` - Geeft aan dat onderliggende elementen alleen in de genoemde volgorde verschijnen.
* `xs:complexType` - Geeft aan dat het andere elementen bevat.
* `xs:simpleType` - Geeft aan dat ze geen andere elementen bevatten.
* `type` - string, decimaal, geheel getal, boolean, datum, tijd,

## Referenties ##

- [Microsoft XML Kladblok](https://microsoft.github.io/XmlNotepad/)
- [XSD-voorbeeldvoorbeeld](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

