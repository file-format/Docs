{
  "date" : "2019-12-09",
  "keywords" :[ "fichier zl", "format de fichier zl", "qu'est-ce qu'un fichier zl", "fichier", "exemple zl", "extension de fichier zl","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Format de fichier compressé ZLIP",
  "description":"En savoir plus sur le format de fichier ZL et les API qui peuvent créer et ouvrir des fichiers ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Qu'est-ce qu'un fichier ZL ?

Un fichier avec l'extension .zl est un format de fichier compressé ZLIP qui utilise une variante de l'algorithme de compression DEFLATE pour compresser les fichiers. Il est indépendant du type de processeur, du système d'exploitation, du système de fichiers et du jeu de caractères, et peut donc être utilisé pour l'échange d'informations. Les spécifications techniques de la compression ZLIP sont disponibles sur le [site IETF](https://tools.ietf.org/html/rfc1950) et peuvent être consultées du point de vue du développeur.

## Format de fichier ZL

Un flux zlib a la structure suivante :

* `CMF (Compression Method and flags)` - Cet octet est divisé en une méthode de compression de 4 bits et un champ d'information de 4 bits selon la méthode de compression.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Méthode de compression)` - Identifie la méthode de compression utilisée dans le fichier. Ses valeurs et la méthode de compression correspondante sont les suivantes.

| Valeur CM| Compression|
|---|---|
|CM = 8|DEFLATE avec une taille de fenêtre jusqu'à 32K|
|CM = 15|Réservé|

* `CINFO (Informations de compression)` - Pour CM = 8, CINFO est le logarithme en base 2 de la taille de la fenêtre LZ77, moins huit (CINFO=7 indique une taille de fenêtre de 32K).

* `FLG (FLaGs)` - Cet octet d'indicateur est divisé comme suit :
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Références ##

* [Spécifications du format de fichier Zlib](https://tools.ietf.org/html/rfc1950)

