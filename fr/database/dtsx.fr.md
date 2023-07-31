{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DTSX et les API qui peuvent créer et ouvrir des fichiers DTSX.",
  "title" :"Format de fichier DTSX - Fichier de paramètres SQL Server DTS",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Qu'est-ce qu'un fichier DTSX ?

Un fichier avec l'extension .dtsx (Data Transformation Services Package XML) est un fichier DTS (Data Transformation Services) utilisé par Microsoft SQL pour faire référence aux étapes/règles de migration de données pour le transfert de données d'une base de données à une autre. Cela inclut les transformations et toutes les étapes de traitement facultatives qui peuvent être nécessaires pendant le transfert de données entre les points d'origine et de destination. SQL Server Integration Services (SSIS), un composant de Microsoft SQL Server, utilise les fichiers DTSX pour identifier les étapes de traitement des données entre les serveurs de base de données. Les fichiers DTSX peuvent être ouverts avec Microsoft SQL Server 2019.

## Format de fichier DTSX

Le déplacement des données entre les serveurs de base de données nécessite des règles et des étapes de traitement pour garantir l'intégrité des données au cours de cette opération. SSIS garantit que toutes ces activités, pour déplacer et conformer les données provenant de différentes sources dans une entreprise, se déroulent de manière pratique. C'est là que vient DTSX qui définit les structures à utiliser par SSIS pour établir les étapes où les données peuvent être traitées au fur et à mesure de ces étapes.

Le flux de données décrit par DTSX est illustré dans l'image suivante.

{{< figure src="../DataFlowDTSX.png" alt="Flux de données DTSX" >}}

DTSX est basé sur [XML](/fr/web/xml/) et est documenté dans [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). La refactorisation améliorée de DTSX XML est DTSX 2.0 qui inclut de nouveaux attributs pour les structures, le remplacement des propriétés nommées en tant qu'attributs XML parents, spécifie les valeurs par défaut pour la plupart des valeurs d'attribut et le placement des éléments répétés dans un élément parent. Les structures DTSX sont décrites à l'aide de ces [schémas XML](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) et le format structurel est celar-texte XML.

## Références

* [Format DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Format DTSX 2 - Par Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

