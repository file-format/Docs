{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "cos'è un file xsd", "come aprire un file xsd", "estensione", "file", "file xsd", "formato file xsd", "estensione xsd" ,"esempio di file xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Ulteriori informazioni sul formato di file XSD e sulle API che possono creare e aprire un file XSD.",
  "title" :"Formato file XSD - File di definizione schema XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Che cos'è un file di schema XSD?

Un file XSD è un file di definizione che specifica gli elementi e gli attributi che possono far parte di un documento XML. Ciò garantisce che i dati vengano interpretati correttamente e che gli errori vengano rilevati, determinando un'appropriata convalida XML. I file XSD assicurano che i dati inseriti seguano la stessa struttura definita nel file. I file XSD sono archiviati nel formato di file [XML](/it/web/xml/) e possono essere aperti o modificati in qualsiasi editor di testo come Microsoft Notepad, Notepad++ o [Microsoft XML Notepad](https://microsoft.github.io /XmlBlocco note/).

## Formato file XSD

I file XSD vengono archiviati su disco in un formato di file di testo normale leggibile dall'uomo. Un XSD definisce gli elementi che possono essere utilizzati nei documenti, relativi ai dati effettivi con cui deve essere codificato.

## Esempio di file XSD

Un semplice file XSD con uno schema dell'ordine di acquisto definisce gli elementi utilizzando i tag come mostrato nel seguente [esempio XSD di Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -schema-semplice?view=vs-2022).

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

Qui vengono utilizzati i seguenti tag.

* `xs:element` - Definisce un elemento.
* `xs:sequence` - Indica che gli elementi figlio appaiono solo nell'ordine indicato.
* `xs:complexType` - Denota che contiene altri elementi.
* `xs:simpleType` - Denota che non contengono altri elementi.
* `tipo` - stringa, decimale, intero, booleano, data, ora,

## Riferimenti ##

- [Blocco note XML Microsoft](https://microsoft.github.io/XmlNotepad/)
- [Esempio di esempio XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

