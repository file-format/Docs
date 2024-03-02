{
  "date": "2022-02-06",
  "keywords": [
"xsd",
".xsd",
"Cad is comhad xsd ann",
"Conas a oscailt comhad xsd",
"síneadh",
"comhad",
"comhad xsd",
"Formáid comhaid xsd",
"síneadh .xsd",
"Sampla comhad xsd"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": " Foghlaim faoi fhormáid comhaid XSD agus APIs ar féidir leo comhad XSD a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid XSD - Comhad Sainmhínithe Scéimre XML",
  "linktitle": "XSD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-xs-gad"
}
},
  "lastmod": "2022-02-06"
}

## Cad is comhad Scéimre XSD ann?

Is comhad sainmhínithe é comhad XSD a shonraíonn na heilimintí agus na tréithe is féidir a bheith mar chuid de dhoiciméad XML. Cinntíonn sé seo go ndéantar sonraí a léirmhíniú i gceart, agus go bhfaightear earráidí, rud a fhágann go mbíonn bailíochtú cuí XML ann. Cinntíonn comhaid XSD go leanann na sonraí a chuirtear isteach an struchtúr céanna mar atá sainmhínithe sa chomhad. Stóráiltear comhaid XSD i bhformáid comhaid [XML](/web/xml/) agus is féidir iad a oscailt nó a chur in eagar in aon eagarthóir téacs ar nós Microsoft Notepad, Notepad++, nó [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/).

## Formáid Comhaid XSD

Stóráiltear comhaid XSD ar diosca i bhformáid gnáth-théacs atá inléite ag an duine. Sainmhíníonn XSD na heilimintí is féidir a úsáid sna doiciméid, a bhaineann leis na sonraí iarbhír a mbeidh sé le hionchódú leo.

## Sampla de Chomhad XSD

Sainmhíníonn comhad XSD simplí a bhfuil scéimre ordú ceannaigh aige na heilimintí trí úsáid a bhaint as clibeanna mar a léirítear i [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022) a leanas.

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

Anseo, úsáidtear na clibeanna seo a leanas.

 * `xs:element` - Sainmhíníonn sé eilimint.
 * `xs:seicheamh` - Ciallaíonn sé seo nach bhfuil gnéithe linbh le feiceáil ach san ord a luaitear.
 * `xs:complexType` - Ciallaíonn sé go bhfuil gnéithe eile ann.
 * `xs:simpleType` - Ciallaíonn sé nach bhfuil eilimintí eile iontu.
 * `cineál` - teaghrán, deachúil, slánuimhir, Boole, dáta, am,

## Tagairtí ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

