{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","vad är en xsd-fil","hur man öppnar xsd-fil", "tillägg", "fil", "xsd-fil","xsd-filformat", ".xsd-tillägg", "exempel på xsd-fil"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Lär dig om XSD-filformat och API:er som kan skapa och öppna en XSD-fil.",
  "title" :"XSD-filformat - XML Schema Definition File",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Vad är en XSD Schema-fil?

En XSD-fil är en definitionsfil som anger de element och attribut som kan ingå i ett XML-dokument. Detta säkerställer att data tolkas korrekt och att fel fångas upp, vilket resulterar i lämplig XML-validering. XSD-filer säkerställer att inmatade data följer samma struktur som definierats i filen. XSD-filer lagras i filformat [XML](/sv/web/xml/) och kan öppnas eller redigeras i valfri textredigerare som Microsoft Notepad, Notepad++ eller [Microsoft XML Notepad](https://microsoft.github.io /XmlAnteckningar/).

## XSD filformat

XSD-filer lagras på skiva i vanligt textfilformat som är läsbart för människor. En XSD definierar de element som kan användas i dokumenten, relaterade till den faktiska data som den ska kodas med.

## Exempel på XSD-fil

En enkel XSD-fil med ett inköpsorderschema definierar elementen med taggar som visas i följande [XSD-exempel av Microsoft](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022).

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

Här används följande taggar.

* `xs:element` - Definierar ett element.
* `xs:sequence` - Anger att underordnade element endast visas i nämnd ordning.
* `xs:complexType` - Anger att den innehåller andra element.
* `xs:simpleType` - Anger att de inte innehåller andra element.
* `typ` - sträng, decimal, heltal, boolean, datum, tid,

## Referenser ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD-exempel](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

