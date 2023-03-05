{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - Format de fichier de collection TrueType",
  "description":"Un fichier TrueType Collection (TTC) combine plusieurs polices en un seul fichier. Apple et Microsoft ont utilisé TTF sur les systèmes d'exploitation Mac et Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Qu'est-ce qu'un fichier TTC ?
Le TTC est abrégé car TrueType Collection est une extension du format True Type. Un fichier TTC peut combiner plusieurs fichiers de polices. Ces fichiers sont utiles pour combiner plusieurs polices qui partagent de nombreux glyphes en commun. Avant Windows 2000, les fichiers TTC étaient utilisés dans les versions chinoise, japonaise et coréenne de Windows, mais plus tard, la prise en charge était disponible pour toutes les régions.


## La structure du fichier de collection de polices
Un fichier TTC se compose d'une table d'en-tête TTC, de répertoires de tables et de plusieurs tables OpenType. L'en-tête TTC doit se trouver au début du fichier. Un répertoire de table complet pour chaque police doit exister. Le format TableDirectory doit être similaire à celui existant dans un fichier non-collection. Le nombre de tableaux dans tous les répertoires d'un fichier TTC est calculé à partir du début d'un fichier TTC.
Les tables d'un fichier TTC sont référencées via le répertoire de tables de leurs polices respectives. Quelques-unes des tables OpenType doivent apparaître plusieurs fois, une fois pour chaque police ajoutée dans la TTC. Alors que les autres tables peuvent être partagées par plusieurs polices dans le fichier TTC.

### En-tête TTC
Deux versions de la table d'en-tête TTC sont disponibles à ce jour :
- La version 1.0 est utilisée pour les fichiers TTC sans signature numérique.
- La version 2.0 peut être utilisée pour les fichiers TTC avec ou sans signature numérique.
Voici les tables d'en-tête TTC des deux versions :

**En-tête TTC Version 1.0 :**

|Type|Nom|Description|
---|---|---|
|TAG|ttcTag|Chaîne d'identification de la collection de polices : 'ttcf' (utilisée pour les polices avec des contours CFF ou CFF2 ainsi que des contours TrueType)|
|uint16|majorVersion|Version majeure de l'en-tête TTC, = 1.|
|uint16|minorVersion|Version mineure de l'en-tête TTC, = 0.|
|uint32|numFonts|Nombre de polices dans TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Tableau des décalages vers le TableDirectory pour chaque police depuis le début du fichier|

**En-tête TTC version 2.0 :**

|Type|Nom|Description|
---|---|---|
|TAG|ttcTag |Chaîne d'identification de la collection de polices : 'ttcf'|
|uint16| majorVersion |Version majeure de l'en-tête TTC, = 2.|
|uint16| minorVersion |Version mineure de l'en-tête TTC, = 0.|
|uint32| numFonts |Nombre de polices dans TTC|
|Décalage32| tableDirectoryOffsets[numFonts] |Tableau des décalages vers le TableDirectory pour chaque police depuis le début du fichier|
|uint32| dsigTag |Tag indiquant qu'une table DSIG existe, 0x44534947 ('DSIG') (null si pas de signature)|
|uint32| dsigLength |La longueur (en octets) de la table DSIG (null si pas de signature)|
|uint32| dsigOffset |Le décalage (en octets) de la table DSIG depuis le début du fichier TTC (null si pas de signature)|

## Références
* [Le fichier de police OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipédia)](https://en.wikipedia.org/wiki/TrueType)

