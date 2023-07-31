{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","qu'est-ce qu'un fichier xsd","comment ouvrir un fichier xsd", "extension", "fichier", "fichier xsd","format de fichier xsd", "extension .xsd" ,"exemple de fichier xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" En savoir plus sur le format de fichier XSD et les API permettant de créer et d'ouvrir un fichier XSD.",
  "title" :"Format de fichier XSD - Fichier de définition de schéma XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Qu'est-ce qu'un fichier de schéma XSD ?

Un fichier XSD est un fichier de définition spécifiant les éléments et les attributs pouvant faire partie d'un document XML. Cela garantit que les données sont correctement interprétées et que les erreurs sont détectées, ce qui entraîne une validation XML appropriée. Les fichiers XSD garantissent que les données saisies suivent la même structure que celle définie dans le fichier. Les fichiers XSD sont stockés au format de fichier [XML](/fr/web/xml/) et peuvent être ouverts ou modifiés dans n'importe quel éditeur de texte tel que Microsoft Notepad, Notepad++ ou [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## Format de fichier XSD

Les fichiers XSD sont stockés sur disque dans un format de fichier texte brut lisible par l'homme. Un XSD définit les éléments qui peuvent être utilisés dans les documents, relatifs aux données réelles avec lesquelles il doit être encodé.

## Exemple de fichier XSD

Un simple fichier XSD ayant un schéma de bon de commande définit les éléments à l'aide de balises comme indiqué dans [exemple XSD par Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -schéma-simple?view=vs-2022).

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

Ici, les balises suivantes sont utilisées.

* `xs:element` - Définit un élément.
* `xs:sequence` - Indique que les éléments enfants n'apparaissent que dans l'ordre mentionné.
* `xs:complexType` - Indique qu'il contient d'autres éléments.
* `xs:simpleType` - Indique qu'ils ne contiennent pas d'autres éléments.
* `type` - chaîne, décimal, entier, booléen, date, heure,

## Références ##

- [Bloc-notes Microsoft XML](https://microsoft.github.io/XmlNotepad/)
- [Exemple d'exemple XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

