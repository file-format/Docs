{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Format de fichier d'image disque",
  "description":"Qu'est-ce qu'un fichier ISO et les API qui peuvent créer et ouvrir des fichiers ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Qu'est-ce qu'un fichier ISO ?

Un fichier avec l'extension .iso est un fichier d'image de disque d'archive non compressé qui représente le contenu de données entières sur un disque optique tel qu'un CD ou un DVD. Basé sur la norme [ISO-9660](https://www.iso.org/standard/17505.html), le format de fichier image ISO contient les données du disque ainsi que les informations sur le système de fichiers qui y sont stockées. La capacité des fichiers ISO à contenir une réplique exacte du contenu en fait le type de fichier idéal pour créer des copies de CD/DVD et est principalement utilisé pour stocker des données amorçables pour l'installation. La plupart du temps, les fichiers ISO sont gravés sur USB/CD/DVD en tant que contenu amorçable pour démarrer la machine pour l'installation. Les fichiers ISO ont le type MIME application/x-iso9660-image.

## Format de fichier ISO

Le format de fichier ISO n'est pas comme les autres formats de fichier de fichier conteneur bien qu'il archive le contenu spécifié des données. L'archive est créée sous forme de fichier binaire avec la structure exacte du contenu et des informations sur le système de fichiers. Le format de fichier ISO est décrit par [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) comme suit.

### Structure de niveau supérieur du fichier ISO

La structure globale du dossier se compose de :

* `System Area` - 32 768 octets et n'est pas utilisé par ISO_9660
* `Data Area` - se compose d'un ensemble de descripteurs de volume et de tables, de répertoires et de fichiers de chemin

### Ensemble de descripteurs de volume

La zone de données commence par l'ensemble de descripteurs de volume, un ensemble d'un ou plusieurs descripteurs de volume terminé par un terminateur d'ensemble de descripteurs de volume. Ceux-ci agissent collectivement comme un en-tête pour la zone de données, décrivant son contenu (similaire au bloc de paramètres BIOS utilisé par les disques formatés FAT, HPFS et NTFS).

Un ensemble de descripteurs de volume est illustré ci-dessous.

|Ensemble de descripteurs de volume|
---|
|Descripteur de volume #1|
|...|
|Descripteur de volume #N|
|Terminaison d'ensemble de descripteurs de volume|

#### Descripteur de volume

Chaque descripteur de volume a une taille de 2048 octets et a la structure suivante :

|Pièce |Type |Identifiant |Version |Données|
---|---|---|---|---|
|Taille |1 octet |5 octets (toujours 'CD001') |1 octet (toujours 0x01) |2 041 octets|

## Références

* [Image de disque optique - Wikipédia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Signatures de fichiers](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipédia](https://en.wikipedia.org/wiki/ISO_9660)

