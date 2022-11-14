{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier EDB - Un fichier de base de données de messagerie Exchange",
  "description":"En savoir plus sur le format de fichier EDB et les API qui peuvent créer et ouvrir des fichiers EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Qu'est-ce qu'un fichier EDB ?

Un fichier avec l'extension de fichier .edb est une base de données de boîtes aux lettres créée par Microsoft Exchange Server pour stocker les données relatives au courrier. EDB, Exchange Database, stocke les messages en cours de traitement et non SMTP. EDB est également connu sous le nom de fichiers de base de données Extensible Storage Engine (ESE) et stocke les fichiers à l'aide d'une structure b-tree. En tant que fichiers de stockage, les fichiers EDB peuvent être convertis en d'autres formats de fichiers de stockage de courrier tels que [PST](/fr/email/pst/) et [OST](/fr/email/ost/).

## Format de fichier EDB

Il n'y a pas de spécifications de format de fichier EDB officielles/ouvertes disponibles qui peuvent être référencées. Certains progrès ont été réalisés pour l'ingénierie inverse du format de fichier, ce qui a entraîné un décodage partiel des spécifications. Selon ceux-ci, un fichier EDB se compose de :
* En-tête de fichier - Contient des informations d'en-tête de fichier de base de données
* Pages de taille fixe - Contient la base de données composée de tables et d'index

### En-tête du fichier de base de données
L'en-tête du fichier de base de données réside dans la première page de la base de données et fait au moins 668 octets. L'en-tête du fichier contient "Version du format de fichier" et "Type de fichier" en plus d'autres champs.

#### Types de fichier
|Type|Description
---|---|
|0| Base de données|
|1| Streaming|

`Remarque :` Les identifiants de ces types ne sont pas connus.

#### Version du format de fichier
Le format original d'EDB a commencé en avril 1997 et a continué à évoluer pour des changements par la suite.

|Date de révision|Version|Révision|description
---|---|---|---|
|Avril 1997| 0x00000620|0x00000000| Format bêta du système d'exploitation d'origine.|
|Mai 1997 |0x00000620|0x00000001| Ajouter des colonnes dans le catalogue pour l'indexation conditionnelle et OLD.|
|Juin 1997|0x00000620|0x00000002|Ajouter l'indicateur fLocalizedText dans IDB.|
|Oct 1997|0x00000620|0x00000003|Ajouter SPLIT_BUFFER aux pages racine de l'arborescence des espaces.|
|Janvier 1998|0x00000620|0x00000002|Annuler la révision afin que ESE97 reste compatible avec les versions antérieures.|
||0x00000620|0x00000003|Ajouter de nouvelles colonnes balisées au catalogue ("CallbackData" et "CallbackDependencies").|
|Mai 1998|0x00000620|0x00000004|Prise en charge des valeurs super longues (SLV) : signSLV, fSLVExists in dbheader.|
|Mai 1998|0x00000620|0x00000005|Nouvel arbre spatial SLV.|
|Oct 1998|0x00000620|0x00000006|Carte de l'espace SLV.|
|Décembre 1998|0x00000620|0x00000007|IDSEG 4 octets.|
|Jan 1999|0x00000620|0x00000008|Nouveau format de colonne de modèle.|
|Juin 1999|0x00000620|0x00000009|Colonnes de modèles triées. Utilisé dans Windows XP SP3 |
||0x00000620|0x0000000b|Contient l'en-tête de page avec la somme de contrôle ECCUtilisée dans Exchange|
||0x00000620|0x0000000c|Utilisé dans Windows Vista (SP0)|
||0x00000620|0x00000011|Prise en charge des pages de 2 Kio, 16 Kio et 32 Kio.En-tête de page étendu avec sommes de contrôle ECC supplémentaires.Compression de colonne.Astuces d'espace.Utilisé dans Windows 7 (SP0)|
|Mai 1999|0x00000623|0x00000000|Nouveau gestionnaire d'espace.|

### Fichiers de base de données

Le fichier de base de données EDB contient le schéma de toutes les tables de la base de données. En outre, il comprend également des enregistrements pour toutes les tables de base de données et des index pour les tables. Son emplacement est déterminé par les identifiants suivants.

* JetCreateDatabase
* JetCreateDatabase2
* Base de données JetAttach
* JetAttachDatabase2

Sur la base de ceux-ci, l'état de la base de données peut être évalué comme suit.

|Valeur|Identifiant|Description
---|---|---|
|1|JET_dbstateJustCreated|La base de données vient d'être créée.|
|2|JET_dbstateDirtyShutdown|La base de données nécessite une récupération matérielle ou logicielle pour être exécutée afin de devenir utilisable ou mobile. Il ne faut pas essayer de déplacer des bases de données dans cet état.|
|3|JET_dbstateCleanShutdown|La base de données est dans un état propre. La base de données peut être jointe sans aucun fichier journal.|
|4|JET_dbstateBeingConverted|La base de données est en cours de mise à niveau.|
|5|JET_dbstateForceDetachInternal|Cette valeur est introduite dans WindowsXP|
 

## Références
* [Spécifications du fichier de base de données du moteur de stockage extensible (ESE) (EDB)] (https://github.com/libyal/libesedb/tree/master/documentation)

