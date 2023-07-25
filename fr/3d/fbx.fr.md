{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "fichier", "extension", "format", "Format de fichier 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier FBX et les API qui peuvent les créer et les ouvrir.",
  "title" :"FBX - Format de fichier FilmBox 3D",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier FBX ?

FBX, FilmBox, est un format de fichier 3D populaire développé à l'origine par Kaydara pour MotionBuilder. Il a été acquis par Autodesk Inc en 2006 et est aujourd'hui l'un des principaux formats d'échange 3D utilisé par de nombreux outils 3D. FBX est disponible au format de fichier binaire et ASCII. Le format a été établi pour assurer l'interopérabilité entre les applications de création de contenu numérique. Il existe de nombreux outils disponibles pour la conversion depuis/vers le format de fichier FBX.

## Format de fichier FBX - Plus d'informations

FBX est un format propriétaire et les spécifications concernant son format de fichier binaire ne sont pas disponibles officiellement. Un SDK C++ FBX est fourni par Autodesk pour la lecture, l'écriture et la conversion vers/depuis le fichier FBX. Un script d'importation et d'exportation Python pour FBX est également disponible dans le logiciel Blender qui n'utilise pas le SDK FBX.

### Structure de fichier basée sur le texte

La structure du fichier à base de texte est une structure arborescente documentée avec des identifiants clairement nommés. Il se compose d'une liste imbriquée de nœuds organisés en hiérarchie où chaque nœud a :

* Un identifiant NodeType (nom de classe)
* Un tuple de propriétés qui lui est associé, les éléments du tuple sont les types de données primitifs habituels : ##float, integer, string## etc.
* Une liste qui contient des nœuds au même format (récursivement).

Celles-ci peuvent être représentées logiquement comme suit :

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Certains des nœuds standard sont définis comme une liste implicite où chaque élément consiste en une liste imbriquée. Toute application ayant l'intention d'accéder à la géométrie FBX doit analyser ce contenu et en tirer une signification utile. Un exemple de fichier FBX textuel est donné ci-dessous :

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Structure de fichier binaire des fichiers FBX

Comme indiqué précédemment, les spécifications du format de fichier FBX ne sont pas disponibles publiquement pour FBX. Étant donné que Blender Foundation implémente le format de fichier FBX sans utiliser le SDK fourni par la société, certains détails sur le format de fichier binaire sont [disponibles](https://code.blender.org/2013/08/fbx-binary-file-format -spécification/) dans le cadre de sa mise en œuvre.

La structure des fichiers binaires suit l'ordre suivant :

* Entête
* Enregistrement d'objet
* Bas de page

### En-tête FBX

Les informations d'en-tête de fichier sont composées de 27 octets.

* Octets 0 - 20 : Kaydara FBX Binary \x00 (file-magic, avec 2 espaces à la fin, puis un terminateur NULL).
* Octets 21 - 22 : [0x1A, 0x00]## (inconnu mais tous les fichiers observés affichent ces octets).
* Octets 23 à 26 : entier non signé, le numéro de version. 7300 pour la version 7.3 par exemple.

### Enregistrement d'objet ###

L'en-tête est suivi d'un enregistrement d'objet qui est un enregistrement de nœud complet avec un nom vide et une liste de propriétés vide. Il contient de manière récursive toute la formation du fichier.

### Bas de page ###

La section FBX Footer se trouve à la fin du fichier dont le contenu est inconnu.

## Formats d'enregistrement ##

Les enregistrements d'un fichier FBX sont classés comme :

* Enregistrements de nœud
* Dossiers de propriété

### Format d'enregistrement de nœud ###

Chaque format d'enregistrement de nœud est nommé et a la disposition de mémoire suivante.


|Taille (octets)|Type de date|Nom
--- | ---|---|
|4|UInt32|DécalageFin
|4|UInt32|NombrePropriétés
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|NomLongueur|car|Nom
|?|?|Propriété[n], où n = 0 :PropertyListLen
|Facultatif| |
|?|?|Liste imbriquée
|13|uint8[]|Enregistrement nul

où:

* `EndOffset` est la distance entre le début du fichier et la fin de l'enregistrement du nœud (c'est-à-dire le premier octet de ce qui vient ensuite). Cela peut être utilisé pour ignorer facilement les enregistrements inconnus ou non requis.
* `NumProperties` est le nombre de propriétés dans le tuple de valeur associé au nœud. Une liste imbriquée comme dernier élément n'est pas comptée comme propriété.
* `PropertyListLen` est la longueur de la liste des propriétés. Il s'agit de la taille requise pour stocker les propriétés ##NumProperties##, qui dépend du type de données des propriétés.
* `NameLen` est la longueur du nom de l'objet, en caractères. Le seul cas où c'est 0 semble être les listes de niveau supérieur.
* `Name` est le nom de l'objet. Il n'y a pas de terminaison zéro.
* `Property[n]` est la nième propriété. Pour le format, voir la propriété de section Format d'enregistrement. Les propriétés sont écrites séquentiellement et sans remplissage.
* `NestedList` est la liste imbriquée, dont la présence est indiquée par un enregistrement NULL à la toute fin.

L'existence d'une entrée de liste imbriquée peut être déterminée en vérifiant s'il reste des octets jusqu'à ce que EndOffset soit atteint. Si tel est le cas, l'enregistrement d'objet suivant doit être lu directement après la dernière propriété. L'enregistrement d'objet suit alors 13 octets zéro, qui se combinent ensuite avec EndOffset. Le but ou l'exigence de l'entrée NULL n'est pas connu et peut pointer vers une fonctionnalité de format.

### Format d'enregistrement de propriété ###

Un enregistrement de propriété contient des détails sur les propriétés qui font partie de Node. Un enregistrement de propriété a la disposition de mémoire suivante :


|Taille (octets)|Type de données|Nom
--- | --- | ---
|1|car|TypeCode
|?|?|Données

TypeCode représente des codes de caractères qui sont classés en groupes nécessitant un traitement similaire. Les TypeCodes peuvent être classés dans les types suivants et TypeCode peut être l'un des codes de caractères parmi ces types.

#### Types primitifs ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Les données dans l'enregistrement de type scalaire primitif sont exactement la représentation binaire de la valeur, dans l'ordre des octets petit boutien.

#### Types de tableau ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Les données pour le type de tableau sont plus complexes et se présentent dans la structure suivante.


|Taille (octets)|Type de données|Nom
--- | --- | ---
|4|Uint32|Longueur du tableau
|4|Uint32|Encodage
|4|Uint32|Longueur compressée
|?|?|Contenu

### Types spéciaux ###

Voici les types spéciaux TypeCodes.

```
S: String
R: raw binary data
```

Ces deux TypeCodes sont représentés comme suit :


|Taille (octets)|Type de données|Nom
--- | --- | ---
|4|Uin32|Longueur
|Longueur| |

La chaîne ne se termine pas par zéro et peut très bien contenir des caractères \0 (ceci est en fait utilisé dans certaines propriétés FBX).

## Références ##

* [FBX - Le SDK Autodesk](https://help.autodesk.com/view/FBX/2017/ENU/)
* [Spécifications du format de fichier binaire FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipédia](https://en.wikipedia.org/wiki/FBX#File_format)

