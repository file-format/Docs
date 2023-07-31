{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "ce este un fișier xsd", "cum se deschide fișierul xsd", "extensie", "fișier", "fișier xsd", "format fișier xsd", "extensie .xsd" ,"exemplu de fișier xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier XSD și despre API-urile care pot crea și deschide un fișier XSD.",
  "title" :"Format de fișier XSD - fișier de definiție a schemei XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Ce este un fișier XSD Schema?

Un fișier XSD este un fișier de definiție care specifică elementele și atributele care pot face parte dintr-un document XML. Acest lucru asigură că datele sunt interpretate corect și că erorile sunt capturate, rezultând o validare XML adecvată. Fișierele XSD asigură că datele introduse urmează aceeași structură definită în fișier. Fișierele XSD sunt stocate în format de fișier [XML](/ro/web/xml/) și pot fi deschise sau editate în orice editor de text, cum ar fi Microsoft Notepad, Notepad++ sau [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## Format de fișier XSD

Fișierele XSD sunt stocate pe disc în format text simplu, care poate fi citit de om. Un XSD definește elementele care pot fi utilizate în documente, referitoare la datele reale cu care urmează să fie codat.

## Exemplu de fișier XSD

Un fișier XSD simplu având o schemă de comandă definește elementele folosind etichete, așa cum se arată în următorul [exemplu XSD de la Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022).

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

Aici sunt folosite următoarele etichete.

* `xs:element` - Definește un element.
* `xs:sequence` - Indică elementele copil care apar numai în ordinea menționată.
* `xs:complexType` - Indică faptul că conține alte elemente.
* `xs:simpleType` - Denotă că nu conțin alte elemente.
* `type` - șir, zecimal, întreg, boolean, dată, oră,

## Referințe ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [Exemplu de exemplu XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

