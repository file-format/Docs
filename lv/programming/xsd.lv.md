{
  "date": "2022-02-06",
  "keywords": [
"xsd",
".xsd",
"kas ir xsd fails",
"kā atvērt xsd failu",
"pagarinājumu",
"failu",
"xsd failu",
"xsd faila formātā",
".xsd paplašinājums",
"xsd faila piemērs"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": " Uzziniet par XSD faila formātu un API, kas var izveidot un atvērt XSD failu.",
  "title": "XSD faila formāts — XML shēmas definīcijas fails",
  "linktitle": "XSD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-xs-lvd"
}
},
  "lastmod": "2022-02-06"
}

## Kas ir XSD shēmas fails?

XSD fails ir definīcijas fails, kas norāda elementus un atribūtus, kas var būt daļa no XML dokumenta. Tas nodrošina datu pareizu interpretāciju un kļūdu uztveršanu, kā rezultātā tiek veikta atbilstoša XML validācija. XSD faili nodrošina, ka ievadītie dati atbilst failā definētajai struktūrai. XSD faili tiek glabāti [XML](/web/xml/) faila formātā, un tos var atvērt vai rediģēt jebkurā teksta redaktorā, piemēram, Microsoft Notepad, Notepad++ vai [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/).

## XSD faila formāts

XSD faili tiek saglabāti diskā vienkārša teksta faila formātā, kas ir cilvēkiem lasāms. XSD definē elementus, ko var izmantot dokumentos, kas attiecas uz faktiskajiem datiem, ar kuriem tas ir jākodē.

## XSD faila piemērs

Vienkāršs XSD fails ar pirkuma pasūtījuma shēmu definē elementus, izmantojot tagus, kā parādīts šajā [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

Šeit tiek izmantoti šādi tagi.

 * xs:element — definē elementu.
 * xs:sequence — norāda, ka pakārtotie elementi parādās tikai norādītajā secībā.
 * xs:complexType” — norāda, ka tajā ir citi elementi.
 * xs:simpleType” — norāda, ka tie nesatur citus elementus.
 * tips — virkne, decimāldaļa, vesels skaitlis, Būla vērtība, datums, laiks,

## Atsauces Nr.

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

