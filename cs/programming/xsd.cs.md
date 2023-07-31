{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","co je soubor xsd","jak otevřít soubor xsd", "přípona", "soubor", "soubor xsd","formát souboru xsd", "přípona xsd", "příklad souboru xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru XSD a rozhraních API, která mohou vytvořit a otevřít soubor XSD.",
  "title" :"Formát souboru XSD - soubor definice schématu XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Co je soubor schématu XSD?

Soubor XSD je definiční soubor určující prvky a atributy, které mohou být součástí dokumentu XML. To zajišťuje, že data jsou správně interpretována a jsou zachyceny chyby, což vede k odpovídající validaci XML. Soubory XSD zajišťují, že zadaná data mají stejnou strukturu, jaká je definována v souboru. Soubory XSD jsou uloženy ve formátu souboru [XML](/cs/web/xml/) a lze je otevřít nebo upravit v libovolném textovém editoru, jako je Microsoft Notepad, Notepad++ nebo [Microsoft XML Notepad](https://microsoft.github.io /XmlPoznámkový blok/).

## Formát souboru XSD

Soubory XSD se ukládají na disk ve formátu prostého textu, který je čitelný pro člověka. XSD definuje prvky, které mohou být použity v dokumentech, týkající se skutečných dat, kterými má být kódován.

## Příklad souboru XSD

Jednoduchý soubor XSD se schématem nákupní objednávky definuje prvky pomocí značek, jak je znázorněno v následujícím [příkladu XSD od společnosti Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

Zde se používají následující značky.

* `xs:element` – Definuje prvek.
* `xs:sequence` - Označuje podřízené prvky, které se objevují pouze v uvedeném pořadí.
* `xs:complexType` - Označuje, že obsahuje další prvky.
* `xs:simpleType` - Označuje, že neobsahují další prvky.
* `type` - řetězec, desetinné číslo, celé číslo, boolean, datum, čas,

## Reference ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [Ukázkový příklad XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

