{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","fichier xbrl", "format de fichier xbrl", "type de fichier xbrl", "fichier", "type", "qu'est-ce qu'un fichier xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Format de fichier de rapports commerciaux et financiers",
  "description":"En savoir plus sur le format de fichier XBRL et les API qui peuvent créer et ouvrir des fichiers XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Qu'est-ce qu'un fichier XBRL ?

Un fichier avec l'extension .xbrl (eXtensible Business Reporting Language) est un cadre mondial disponible gratuitement pour l'échange d'informations commerciales. Il est maintenant largement utilisé comme l'un des formats standards qui a remplacé les anciens rapports papier par des enregistrements numériques plus utiles et plus précis. Les données échangées à l'aide des fichiers XBRL comprennent les registres, les détails financiers et les bilans. Il prend en charge les balises de données qui permettent le traitement des données de la préparation à l'étape d'analyse des informations commerciales de toutes sortes. Les fichiers XBRL peuvent être ouverts à l'aide d'un logiciel tel que Rivet Software Dragon View XBRL Viewer et d'API comme [Aspose.Finance](https://products.aspose.com/finance/).

## Format de fichier XBRL

XBRL est une norme internationale ouverte pour les rapports commerciaux numériques qui est largement utilisée dans le monde. Il s'agit d'un langage basé sur [XML](/fr/web/xml/) qui utilise des éléments XBRL, appelés balises, pour décrire chaque élément de données commerciales afin de formuler des données pour le tri et l'analyse des rapports. Les spécifications de format de fichier XBRL sont développées et publiées par XBRL International, Inc, avec [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) actuellement à la disposition des utilisateurs.

### Structure des documents XBRL

Informations complètes sur les [balises XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) peuvent être consultés par les programmeurs pour écrire des applications permettant de travailler ce format de fichier. Un XBRL se compose d'une instance XBRL et d'un ensemble de taxonomies.

**`Instance XBRL`** - L'instance XBRL commence par le<xbrl> élément racine. Un document XML volumineux peut contenir plusieurs instances XBRL intégrées.

**`Taxonomie XBRL`** - La [taxonomie XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) est défini comme une structure de schéma XML et un ensemble d'éléments de liens externes directement référencés. Un schéma de taxonomie évolutif montrant les références de la base de liens est le suivant.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Références ##

* [XBRL - Par Wikipédia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

