{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Data Tier AppliCation Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DACPAC et les API qui peuvent créer et ouvrir des fichiers DACPAC.",
  "title" :"DACPAC - Package d'application de niveau de données",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Qu'est-ce qu'un fichier DACPAC ?

Un fichier avec l'extension .dacpac (signifie Data Tier AppliCation Package) est un fichier de base de données, créé avec l'application de niveau de données Microsoft SQL Server, qui contient le modèle de base de données pour la représentation des objets de la base de données. Comme il contient le modèle complet de la base de données, il permet de restaurer une base de données à partir des détails disponibles dans le modèle. Les fichiers DACPAC sont généralement remis aux équipes de déploiement pour être installés dans les locaux du client afin de restaurer la base de données. Ceux-ci peuvent être ouverts avec
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Format de fichier DACPAC - Plus d'informations

Les fichiers de package de données DACPAC sont en fait des fichiers ZIP compressés qui contiennent plusieurs fichiers [XML](/fr/web/xml/) contenant des informations sur le modèle de base de données, telles que des tables et des vues, utilisées pour restaurer une base de données. Pour afficher le contenu des fichiers DACPAC, renommez les fichiers de .dacpac en [.zip](/fr/compression/zip/) et extrayez l'archive zip à l'aide de n'importe quel utilitaire de décompression.

Voici quelques fichiers qui se trouvent dans un fichier DACPAC.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>GRC</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origine.xml

* modèle.xml

Il convient de noter que DACPAC ne contient pas de DATA ni d'autres objets au niveau du serveur. Le fichier peut contenir tous les types d'objets pouvant être conservés dans le projet SSDT.

## Références

* [Applications de niveau de données - Avantages](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [Déploiement d'une application de niveau de données - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Comment créer un fichier DACPAC ?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

