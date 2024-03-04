{
  "date": "2022-02-06",
  "keywords": [
"xsd",
".xsd",
"kas yra xsd failas",
"kaip atidaryti xsd failą",
"pratęsimas",
"failą",
"xsd failą",
"xsd failo formatas",
".xsd plėtinys",
"xsd failo pavyzdys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": " Sužinokite apie XSD failo formatą ir API, kurios gali sukurti ir atidaryti XSD failą.",
  "title": "XSD failo formatas – XML schemos apibrėžimo failas",
  "linktitle": "XSD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-xs-ltd"
}
},
  "lastmod": "2022-02-06"
}

## Kas yra XSD schemos failas?

XSD failas yra apibrėžimo failas, nurodantis elementus ir atributus, kurie gali būti XML dokumento dalis. Taip užtikrinama, kad duomenys būtų tinkamai interpretuojami, o klaidos sugautos, todėl atliekamas tinkamas XML patvirtinimas. XSD failai užtikrina, kad įvesti duomenys atitiktų tą pačią struktūrą, kaip apibrėžta faile. XSD failai saugomi [XML](/web/xml/) failo formatu ir gali būti atidaryti arba redaguoti bet kuriame teksto rengyklėje, pvz., Microsoft Notepad, Notepad++ arba [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/).

## XSD failo formatas

XSD failai saugomi diske paprasto teksto failo formatu, kuris yra skaitomas žmogui. XSD apibrėžia elementus, kuriuos galima naudoti dokumentuose, susijusius su faktiniais duomenimis, su kuriais jis turi būti užkoduotas.

## XSD failo pavyzdys

Paprastas XSD failas, turintis pirkimo užsakymo schemą, apibrėžia elementus naudodamas žymas, kaip parodyta toliau pateiktoje [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

Čia naudojamos šios žymos.

 * xs:element – apibrėžia elementą.
 * xs:sequence – nurodo, kad antriniai elementai rodomi tik nurodyta tvarka.
 * xs:complexType – reiškia, kad jame yra kitų elementų.
 * xs:simpleType – reiškia, kad juose nėra kitų elementų.
 * tipas – eilutė, dešimtainis skaičius, sveikasis skaičius, loginis, data, laikas,

## Nuorodos Nr.

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

