{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "mi az xsd fájl", "az xsd fájl megnyitása", "kiterjesztés", "fájl", "xsd fájl", "xsd fájlformátum", ".xsd kiterjesztése", "xsd file example"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet az XSD fájlformátumról és az API-król, amelyekkel XSD-fájlt hozhat létre és nyithat meg.",
  "title" :"XSD fájlformátum - XML sémadefiníciós fájl",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Mi az az XSD-sémafájl?

Az XSD-fájl egy definíciós fájl, amely meghatározza azokat az elemeket és attribútumokat, amelyek részei lehetnek egy XML-dokumentumnak. Ez biztosítja az adatok megfelelő értelmezését és a hibák elkapását, ami megfelelő XML-ellenőrzést eredményez. Az XSD fájlok biztosítják, hogy a bevitt adatok a fájlban meghatározott szerkezetet követik. Az XSD-fájlok [XML](/hu/web/xml/) fájlformátumban vannak tárolva, és bármilyen szövegszerkesztőben megnyithatók vagy szerkeszthetők, például Microsoft Notepad, Notepad++ vagy [Microsoft XML Notepad](https://microsoft.github.io /XmlJegyzettömb/).

## XSD fájl formátum

Az XSD fájlok egyszerű szöveges fájlformátumban kerülnek a lemezre, amely ember által olvasható. Az XSD meghatározza a dokumentumokban használható elemeket, amelyek a kódolni kívánt tényleges adatokhoz kapcsolódnak.

## Példa XSD fájlra

Egy egyszerű, beszerzési rendelési sémával rendelkező XSD-fájl címkék segítségével határozza meg az elemeket a következő [XSD-példa a Microsofttól] szerint](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022).

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

Itt a következő címkéket használjuk.

* `xs:element` – Egy elemet határoz meg.
* `xs:sequence` – Azt jelzi, hogy a gyermekelemek csak az említett sorrendben jelennek meg.
* `xs:complexType` – Azt jelzi, hogy más elemeket is tartalmaz.
* `xs:simpleType` – Azt jelzi, hogy nem tartalmaznak más elemeket.
* "típus" - karakterlánc, tizedes, egész, logikai érték, dátum, idő,

## Hivatkozások ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD-minta példa](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

