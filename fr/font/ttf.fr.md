{
  "date" : "2020-08-20",
  "keywords" :[ "fichier ttf", "format de fichier ttf", "qu'est-ce qu'un fichier ttf", "fichier", "exemple ttf", "extension de fichier ttf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - Format de fichier de police TrueType",
  "description":"Les polices TrueType (TTF) sont basées sur les spécifications de la technologie de police numérique initialement conçues par Apple, Inc. Apple et Microsoft ont utilisé TTF sur les systèmes d'exploitation Mac et Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Qu'est-ce qu'un fichier TTF ?

Un fichier avec l'extension .ttf représente des fichiers de police basés sur la technologie de police des spécifications TrueType. Il a été initialement conçu et lancé par Apple Computer, Inc pour Mac OS et a ensuite été adopté par Microsoft pour Windows OS. Les polices TrueType offrent un affichage de la plus haute qualité sur les écrans d'ordinateur et les imprimantes sans aucune dépendance à la résolution. Toutes les applications modernes utilisant des polices sont capables de travailler avec des fichiers TTF. Les fichiers de polices TTF sont disponibles gratuitement sur Internet et peuvent également être convertis en d'autres formats de fichiers de polices tels que OTF et WOFF.

## Bref historique

Conçu par Apply Computer, Inc dans les années 1980 pour MacOS, le format de police TTF visait à résoudre certaines limitations techniques du format Type 1 d'Adobe. Apple a inclus la prise en charge des polices TrueType sur Mac en 1991. L'objectif de conception des polices TTF était l'efficacité du stockage et du traitement, ainsi que l'extensibilité. Sur la base de cette extensibilité, les polices existantes peuvent être converties au format TrueType.

Microsoft a utilisé pour la première fois les polices TrueType dans Windows 3.1 en avril 1992 après qu'Apple ait accepté de concéder une licence TrueType à Microsoft. Il a amélioré le mécanisme de pixellisation et amélioré son efficacité et ses performances.

## Spécifications du format de fichier True Type

Un fichier de police TrueType est un fichier binaire composé d'une séquence de tables concaténées. Chaque table est une séquence de mots et porte un nom connu sous le nom de `Tag`. Chaque balise est de type de données uint32 et se compose de quatre caractères. La première table du fichier est le répertoire de polices qui donne accès aux autres tables du fichier de polices. Les données de police sont contenues dans d'autres tables suivies après la table du répertoire de polices. Étant donné que chaque table est accessible par sa balise, les tables peuvent apparaître dans n'importe quel ordre dans le fichier.

Les tables requises et leurs noms de balises sont indiqués dans le tableau suivant.

|**Balise**|**Table**|
---|---|
|'cmap'| mappage de caractère à glyphe |
|'glyf'| données de glyphe |
|'tête'| en-tête de police |
|'hhea'| en-tête horizontal |
|'hmtx'| mesures horizontales |
|'lieu'| index de l'emplacement |
|'maxp'| profil maximal |
|'nom'| dénomination |
|'poster'| PostScript|

### Types de données
Les polices TrueType utilisent les entiers standard et les types de données supplémentaires répertoriés dans le tableau suivant.

|**Type de données** | **Description** |
---|---|
|shortFrac| Fraction signée 16 bits |
|Fixé| Numéro à virgule fixe signé 16,16 bits |
|FWord| Entier signé 16 bits décrivant une quantité en FUnits, la plus petite distance mesurable dans l'espace em.|
|uFWord| Entier non signé de 16 bits décrivant une quantité en FUnits, la plus petite distance mesurable dans l'espace em.|
|F2Point14| Nombre fixe signé 16 bits avec les 14 bits inférieurs représentant la fraction.|
|longDateHeure| Le format interne long d'une date en secondes depuis 12h00 minuit, le 1er janvier 1904. Il est représenté sous la forme d'un entier signé de 64 bits.|

### Répertoire des polices

La première table de la police TrueType est le répertoire des polices qui permet d'accéder aux informations requises pour accéder aux données d'autres tables. Il se compose en outre de :

* `Offset subtable` - conserve un enregistrement des tables dans la police et fournit des informations de décalage pour accéder à chaque table du répertoire
* `Table Directory` - Contient des entrées pour chaque table dans la police

#### Sous-table de décalage
Le sous-tableau de décalage est illustré ci-dessous.

|**Type**|**Nom**|**Description**|
---|---|---|
|uint32| type de détartreur | Une balise pour indiquer le scaler OFA à utiliser pour pixelliser cette police ; voir la note sur le type de détartreur ci-dessous pour plus d'informations.|
|uint16| nombreTables| nombre de tables|
|uint16| plage de recherche| (puissance maximale de 2 <= numTables)*16|
|uint16| sélecteur d'entrée| log2(puissance maximale de 2 <= numTables)|
|uint16| rangeShift| numTables*16-plage de recherche|

#### Répertoire des tables
Le répertoire de la table vient juste après la sous-table offset. Sa structure est telle que présentée dans le tableau suivant.

|**Type**|**Nom**|**Description**|
---|---|---|
|uint32| balise| Identifiant de 4 octets |
|uint32| somme de contrôle | somme de contrôle pour cette table |
|uint32| décalage| décalage depuis le début de sfnt|
|uint32| longueur| longueur de cette table en octets (longueur réelle non rembourrée) |

Chaque table d'un fichier de police doit avoir sa propre entrée de répertoire de table. Les entrées d'un tableau doivent être triées par ordre croissant par balise.


## Références
* [Manuel de référence des polices TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Aperçu de TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

