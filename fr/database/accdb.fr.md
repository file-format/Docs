{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier ACCDB et les API qui peuvent créer et ouvrir des fichiers ACCDB.",
  "title" :"Format de fichier ACCDB - Fichier de base de données Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Qu'est-ce qu'un fichier ACCDB ?

Un fichier avec l'extension .accdb est un fichier de base de données Microsoft Access 2007 qui stocke les données des utilisateurs dans des tables. Il prend en charge le stockage
formulaires personnalisés, requêtes SQL et autres données. Les fichiers ACCDB ont remplacé les fichiers [MDB](/fr/database/mdb/) après que Microsoft est passé à la structure de fichiers basée sur XML. Les fichiers ACCDB peuvent toujours être convertis en MDB avec une ancienne compatibilité. Cependant, les ACCDB sont actuellement le format de fichier de base de données Access largement utilisé. Microsoft a également pris en charge des fonctionnalités supplémentaires au format ACCDB telles que la possibilité de stocker des pièces jointes, des données binaires et la prise en charge de champs à valeurs multiples.

## Format de fichier ACCDB

Comme MDB, aucune spécification publique n'est disponible pour le format de fichier ACCDB. Microsoft prend en charge l'accès à ces fichiers par programmation via la norme ODBC (Open Database Connectivity) et Visual Basic pour Applications (VBA).

### Un aperçu

Un vidage hexadécimal d'un simple fichier ACCDB suggère qu'il existe des similitudes générales dans la structure des dernières versions de la famille de formats MDB précédente. Les deux formats de fichier utilisent des tailles de page fixes de 4096 octets. Une autre similitude entre ACCDB et MDB est la forme du nombre magique, qui inclut la chaîne "Standard ACE DB" pour ACCDB. Une version ou un code de compatibilité se trouve au même emplacement dans les deux formats. Les mdbtools | Le fichier HACKING indique "Offset 0x14 contient la version Jet de cette base de données" et le guide MDB non officiel est d'accord. Les informations contenues dans ces sources, combinées à l'entrée Wikipedia pour [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggèrent qu'une valeur de 0x02 indique ACE 12 (Access 2007) et 0x03 indique ACE 14 (Accès 2010). Cependant, une base de données minimale créée dans Access 2010 et une autre similaire créée dans Access 2016 ont toutes deux 0x02 à cet emplacement. Une base de données minimale créée dans Access 2016, mais définissant une colonne avec le type de données "grand entier" nouvellement introduit, avait une valeur de 0x05. Dans les fichiers ACCDB, cet indicateur semble refléter la compatibilité du fichier plutôt que la version du moteur ACE utilisé pour le créer.

## Références

* [Format de fichier d'accès](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
* [Spécifications d'accès 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Moteur de base de données Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Quel format de fichier Access dois-je utiliser ?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)

