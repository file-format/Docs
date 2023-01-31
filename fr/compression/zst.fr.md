{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier ZST - Format de fichier compressé Zstandard",
  "description":"En savoir plus sur le format de fichier ZST et les API qui peuvent créer et ouvrir des fichiers ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Qu'est-ce qu'un fichier ZST ?

Un fichier ZST est un fichier compressé généré avec l'algorithme de compression Zstandard (zstd). Il s'agit d'un fichier compressé qui est créé avec une compression sans perte par l'algorithme. Les fichiers ZST peuvent être utilisés pour compresser différents types de fichiers tels que des bases de données, des systèmes de fichiers, des réseaux et des jeux. Le Zstandard est régi par [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) qui décrit le mécanisme de compression global, le type de média et l'encodage du contenu.

## Format de fichier ZST

Les fichiers ZST sont stockés au format de fichier compressé sur le disque. Le mécanisme de compression est tel que décrit par la RFC 8878 qui rend obsolète la RFC 8478.

## Cadres ZST

Un fichier ZST se compose d'une ou plusieurs images. Chaque image peut être une image Zstandard ou une image désactivable. Un cadre Zstandard contient des données compressées, tandis qu'un cadre désactivable contient des métadonnées utilisateur personnalisées.

### Cadre Zstandard

Un cadre Zstandard a la structure suivante.

|Champ|Taille en octets|
---|---|
|Magic_Number |4 octets|
|Frame_Header |2-14 octets|
|Data_Block |n octets|
|[Plus de Data_Blocks] ||
|[Content_Checksum] |4 octets|

### Cadre désactivable

Une trame désactivable permet l'insertion de métadonnées définies par l'utilisateur dans un flux de trames concaténées. La structure d'une trame désactivable est la suivante.

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 octets |4 octets |n octets|

## Références ##

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)

