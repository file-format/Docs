{
  "date" : "2020-08-20",
  "keywords" :[ "fichier otf", "format de fichier otf", "qu'est-ce qu'un fichier otf", "fichier", "exemple otf", "extension de fichier otf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Format de fichier de police TrueType",
  "description":"En savoir plus sur le format de fichier OTF et les API qui peuvent créer et ouvrir des fichiers OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Qu'est-ce qu'un fichier OTF ?

Un fichier avec l'extension .otf fait référence au format de police OpenType. Le format de police OTF est plus évolutif et étend les fonctionnalités existantes des formats [TTF](/fr/font/ttf/) pour la typographie numérique. Développé par Microsoft et Adobe, OTF combine les fonctionnalités des formats de police PostScript et TrueType. Cela permet au format OTF de s'adapter aux systèmes d'écriture majoritaires et c'est pourquoi il est uniformément utilisé sur les principales plates-formes informatiques. Le format de police OpenType est pris en charge par Mac OS X et Windows 2000 et versions ultérieures.

## Bref historique

L'exigence des polices OpenType est née de l'exigence d'un format de police plus expressif capable de gérer une typographie fine. En outre, il visait à répondre aux exigences du comportement complexe de nombreux systèmes d'écriture du monde. Microsoft a tenté d'obtenir une licence pour la technologie de typographie avancée d'Apple, connue sous le nom de GX Typography, au début des années 1990. Cela ne s'est pas bien passé et, par conséquent, Microsoft a commencé à améliorer sa propre technologie de police TrueType en 1994. Les modifications comprenaient également l'introduction d'un format de police plus approprié qui répond également aux fonctionnalités des formats de police Type 1 (PostScript) d'Adobe.

Adobe, en 1996, a rejoint Microsoft dans ses efforts pour remplacer à la fois le TrueType d'Apple et ses propres formats de police Type 1. Cela a entraîné la combinaison des deux formats de police sous-jacents pour surmonter les limitations et ajouter de nouvelles extensions. Cette nouvelle technologie a été introduite la même année sous le nom **OpenType**.

## Spécifications du format de fichier OTF

Les spécifications OTF sont disponibles publiquement par Microsoft et peuvent être consultées du point de vue du développeur. Comme TTF, il utilise la même structure de conteneur 'sfnt' et est compatible avec les spécifications TrueType. Les données contenues dans un fichier de police OpenType sont utilisées à différentes fins, telles que le calcul de la mise en page du texte, la définition de glyphes en tant que contours TrueType ou Compact Font Format (CFF), la fourniture de bitmaps monochromes ou de couleur ou de documents SVG comme descriptions de glyphes alternatives et des informations de métadonnées.

### Types de données OTF
Les fichiers OTF utilisent les types de données suivants qui sont tous en Big Endian.

|Type de données| Descriptif|
---|---|
|uint8| Entier non signé 8 bits.|
|int8| Entier signé 8 bits.|
|uint16| Entier non signé 16 bits.|
|int16| Entier signé 16 bits.|
|uint24| Entier non signé 24 bits.|
|uint32| Entier non signé 32 bits.|
|int32| Entier signé 32 bits.|
|Fixé| Nombre à virgule fixe signé 32 bits (16.16)|
|FWORD| int16 qui décrit une quantité en unités de conception de police.|
|UFWORD| uint16 qui décrit une quantité en unités de conception de police.|
|F2DOT14| Nombre fixe signé 16 bits avec les 14 bits inférieurs de la fraction (2.14).|
|LONGDATETIME| Date et heure représentées en nombre de secondes depuis 12h00 minuit, le 1er janvier 1904, UTC. La valeur est représentée sous la forme d'un entier 64 bits signé.|
|Étiquette| Tableau de quatre uint8 (longueur = 32 bits) utilisé pour identifier un tableau, un axe de variation de conception, un script, un système linguistique, une fonctionnalité ou une ligne de base |
|Décalage16| Décalage court vers une table, identique à uint16, décalage NULL = 0x0000 |
|Décalage32| Décalage long vers une table, identique à uint32, décalage NULL = 0x00000000 |
|Version16Point16| Valeur 32 bits compressée avec numéros de version majeurs et mineurs. (Voir les numéros de version du tableau.)|

### Répertoire des tables OTF

Un fichier OTF commence par un répertoire de table. Ce répertoire est la collection de niveau supérieur des tables du fichier de police. Selon le nombre de polices dans un fichier, le répertoire de la table peut se trouver à un emplacement différent dans le fichier. Par exemple, si le fichier de polices n'a qu'une seule police, le répertoire de la table commence à l'octet 0 du fichier. En cas de collection de plusieurs polices OpenType,
le début du répertoire de la table est indiqué dans le TTCHeader.

|Type |Nom |Description|
---|---|---|
|uint32 |sfntVersion| 0x00010000 ou 0x4F54544F ('OTTO')|
|uint16| numTables |Nombre de tables.|
|uint16| searchRange |Puissance maximale de 2 inférieure ou égale à numTables, fois 16 ((2\**floor(log2(numTables))) * 16, où "**" est un opérateur d'exponentiation).|
|uint16 |entrySelector Log2 de la puissance maximale de 2 inférieure ou égale à numTables (log2(searchRange/16), qui est égal à floor(log2(numTables))).|
|uint16 |rangeShift |numTables fois 16, moins searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[numTables] | Tableau d'enregistrements de table—un pour chaque table de niveau supérieur dans la police|


### Enregistrement de tableau

Pour chaque table de niveau supérieur dans la police, il existe un enregistrement de table composé des champs suivants.

|Type| Nom| Descriptif|
---|---|---|
|Étiquette| tableTag| Identificateur de table.|
|uint32| somme de contrôle | Somme de contrôle pour cette table.|
|Décalage32| décalage| Décalage depuis le début du fichier de police.|
|uint32| longueur Longueur de ce tableau.|

Chaque tableau du fichier de polices OpenType est représenté par des noms connus sous le nom de balises de tableau. Il est indispensable que tous les enregistrements du tableau soient triés par ordre croissant par balise.

## Références
* [Spécifications des polices OpenType par Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [Aperçu de TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

