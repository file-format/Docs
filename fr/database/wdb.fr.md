{
  "date" : "2021-08-24",
  "keywords" :[ "fichier wdb", "format de fichier wdb", "qu'est-ce qu'un fichier wdb", "fichier", "exemple wdb", "extension de fichier wdb","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier WDB et les API qui peuvent créer et ouvrir des fichiers WDB.",
  "title" :"WDB - Fichier de suivi SQL Server",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Qu'est-ce qu'un fichier WDB ?
Un fichier avec l'extension .wdb est en fait un fichier de base de données créé par Microsoft Works qui a été utilisé pour exécuter des fonctions comme un système de gestion de base de données. Le fichier WDB est similaire au fichier Access Database ([MDB](/fr/database/mdb/)), mais moins efficace et plus limité. Les fichiers WDB ne peuvent pas être ouverts à l'aide de Microsoft Access. Cependant, vous pouvez ouvrir le fichier WDB dans Microsoft Works, puis l'exporter vers un fichier MDB, afin d'ouvrir un fichier WDB dans MS Access.

## Format de fichier WDB
La base de données Microsoft Works est le format de base de données natif de la suite bureautique Microsoft Works. En raison de la nature propriétaire du format et de certaines limitations. Les fichiers WDB ne peuvent être ouverts dans aucun autre logiciel que Microsoft Works. Dans le format de fichier, un en-tête récurrent de 10 octets peut être trouvé avant chacune des chaînes de texte ASCII représentant les valeurs des champs terminés par une valeur NULL. L'en-tête commence généralement par un octet **\x0f** et NULL, suivi de 4 octets de données alternés avec des NULL.

### Structure du fichier

La structure du fichier WDB est donnée ci-dessous :
- **1er en-tête** : depuis le début du fichier, se terminant par \x25\x00\xf2 et 244 octets NULL
- **2ème en-tête** : commençant par \xffT - c'est-à-dire \xff\x54 et s'étendant sur 4 096 octets, qui contient des noms de colonnes/champs et d'autres éléments, et semble commencer à la position d'octet 6144.
- **Champ** : la valeur a un en-tête de 10 octets, au format suivant : {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , partie 2} {db 4} \x00. l'octet de données 2 est le numéro de champ, l'octet de données 3 est le numéro d'enregistrement (ajout de l'octet de données 3, partie 2 lorsqu'il dépasse 256 enregistrements).


## Références ##

* [Utilisateur :JesseW/wdb format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

