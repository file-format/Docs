{
  "date": "2022-02-06",
  "keywords": [
"xsd",
".xsd",
"mikä on xsd-tiedosto",
"kuinka avata xsd-tiedosto",
"laajennus",
"tiedosto",
"xsd tiedosto",
"xsd tiedostomuoto",
".xsd laajennus",
"xsd-tiedosto esimerkki"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": " Opi XSD-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XSD-tiedoston.",
  "title": "XSD-tiedostomuoto - XML Schema Definition -tiedosto",
  "linktitle": "XSD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-xs-fid"
}
},
  "lastmod": "2022-02-06"
}

## Mikä on XSD Schema -tiedosto?

XSD-tiedosto on määritystiedosto, joka määrittää elementit ja attribuutit, jotka voivat olla osa XML-dokumenttia. Tämä varmistaa, että tiedot tulkitaan oikein ja virheet havaitaan, mikä johtaa asianmukaiseen XML-validointiin. XSD-tiedostot varmistavat, että syötetyt tiedot noudattavat samaa rakennetta kuin tiedostossa on määritelty. XSD-tiedostot on tallennettu [XML](/web/xml/)-tiedostomuodossa, ja niitä voidaan avata tai muokata missä tahansa tekstieditorissa, kuten Microsoft Notepad, Notepad++ tai [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/).

## XSD tiedostomuoto

XSD-tiedostot tallennetaan levylle vain tekstitiedostomuodossa, joka on ihmisen luettavissa. XSD määrittelee elementit, joita voidaan käyttää asiakirjoissa ja jotka liittyvät todelliseen dataan, jolla se on koodattava.

## Esimerkki XSD-tiedostosta

Yksinkertainen XSD-tiedosto, jossa on ostotilausskeema, määrittää elementit tunnisteiden avulla seuraavassa {{HYPERLINKKI}}:ssa esitetyllä tavalla.

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

Tässä käytetään seuraavia tunnisteita.

 * `xs:element' - Määrittää elementin.
 * `xs:sequence` - tarkoittaa, että alatason elementit näkyvät vain mainitussa järjestyksessä.
 * `xs:complexType` - tarkoittaa, että se sisältää muita elementtejä.
 * `xs:simpleType` - Ilmaisee, että ne eivät sisällä muita elementtejä.
 * tyyppi - merkkijono, desimaali, kokonaisluku, looginen arvo, päivämäärä, aika,

## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

