{
  "date" : "2019-12-09",
  "keywords" :[ "fichier zip", "format de fichier zip", "qu'est-ce qu'un fichier zip", "fichier", "exemple de zip", "extension de fichier zip","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIP",
  "description":"Qu'est-ce qu'un fichier ZIP et les API qui peuvent créer et ouvrir des fichiers ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Qu'est-ce qu'un fichier ZIP ?

Un fichier avec l'extension .zip est une archive qui peut contenir un ou plusieurs fichiers ou répertoires. L'archive peut avoir une compression appliquée aux fichiers inclus afin de réduire la taille du fichier ZIP. Le format de fichier ZIP a été rendu public en février 1989 par Phil Katz pour réaliser l'archivage des fichiers et des dossiers. Le format a été intégré à l'utilitaire [PKZIP](https://www.pkware.com/pkzip), créé par PKWARE, Inc. Juste après la disponibilité des [spécifications disponibles](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), de nombreuses entreprises ont intégré le format de fichier ZIP à leurs utilitaires logiciels, notamment Microsoft (depuis Windows 7), Apple (Mac OS X) et bien d'autres.

## Bref historique du format de fichier ZIP

L'histoire du format de fichier ZIP remonte à l'événement de la poursuite intentée par System Enhancement Associates (SEA) contre PKWARE pour avoir utilisé son utilitaire ARC sans autorisations pour sa marque et les droits d'auteur de l'apparence et de l'interface utilisateur du produit. Avant cela, Phil Katz avait réécrit le code source de SEA et publié PKXARC, un extracteur ARC, et PKARC, un compresseur de fichiers, en tant que logiciels gratuits pour les systèmes MS-DOS. Perdant face au procès, PKWARE ne pouvait plus utiliser quoi que ce soit lié à l'ARC. C'est là qu'est née la création d'une nouvelle compression de fichiers, nommée ZIP, qui a été intégrée à l'utilitaire PKZIP de PKWARE, Inc.

Katz a publié les spécifications du format de fichier ZIP dans le domaine public, tout en conservant les droits de propriété sur son utilitaire de compression et d'extraction, à savoir PKZIP. Le système de compression ZIP était (et est) capable d'archiver des fichiers dans un dossier au moyen d'un algorithme de contrôle de redondance cyclique 32 bits ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) pour compresser le fichier tailles. Contrairement à ARC, les dossiers .ZIP comprenaient un fichier de répertoire qui jouait le rôle d'un livre de codes de cryptographe, contenant les informations nécessaires pour rendre les fichiers compressés.

## Méthodes de compression prises en charge dans ZIP

Conformément aux spécifications du format de fichier .ZIP, les méthodes de compression suivantes sont prises en charge.

* Store - n'implique aucune compression
* Rétrécir
* Réduction (Cela implique des facteurs de compression allant du niveau 1 au niveau 4)
* Imploser
* Dégonfler
* Deflat64
* BZIP2
* LZMA (EFS)
* Pack Wav
* PPMd version I, Rev 1

DEFLATE est la méthode de compression couramment utilisée qui est un algorithme de compression de date sans perte qui utilise une combinaison du codage LZ77 et Huffman et est détaillé dans [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Spécifications du format de fichier ZIP

Les fichiers ZIP ont la capacité de stocker plusieurs fichiers en utilisant différentes techniques de compression tout en prenant en charge le stockage d'un fichier sans aucune compression. Chaque fichier est stocké/compressé individuellement, ce qui permet de les extraire ou d'en ajouter de nouveaux, sans appliquer de compression ou de décompression à l'intégralité de l'archive.

### Format de fichier ZIP global

Chaque fichier Zip est structuré de la manière suivante :


|Format de fichier ZIP
---|
|En-tête de fichier local 1
|Données de fichier 1
|Descripteur de données 1
|En-tête de fichier local 2
|Données de fichier 2
|Descripteur de données 2
| ....
| ....
|En-tête de fichier local N
|Données de fichier N
|Descripteur de données N
|En-tête de déchiffrement d'archive
|Archive d'enregistrement de données supplémentaires
|Répertoire central

Le format de fichier ZIP utilise l'algorithme CRC 32 bits à des fins d'archivage. Afin de restituer les fichiers compressés, une archive ZIP contient un répertoire à sa fin qui conserve l'entrée des fichiers contenus et leur emplacement dans le fichier d'archive. Il joue ainsi le rôle d'encodage pour encapsuler les informations nécessaires au rendu des fichiers compressés. Les lecteurs ZIP utilisent le répertoire pour charger la liste des fichiers sans lire l'intégralité de l'archive ZIP. Le format conserve des copies doubles de la structure du répertoire pour fournir une meilleure protection contre la perte de données.

Chaque fichier dans une archive ZIP est représenté comme une entrée individuelle où chaque entrée se compose d'un en-tête de fichier local suivi des données du fichier compressé. Le répertoire à la fin de l'archive contient les références à toutes ces entrées de fichier. Les lecteurs de fichiers ZIP doivent éviter de lire les en-têtes de fichiers locaux et toutes sortes de listes de fichiers doivent être lues à partir du répertoire. Ce répertoire est la seule source d'entrées de fichiers valides dans l'archive, car les fichiers peuvent également être ajoutés vers la fin de l'archive. C'est pourquoi si un lecteur lit les en-têtes locaux d'une archive ZIP depuis le début, il peut également lire des entrées invalides (supprimées) qui ne font pas partie du répertoire en cours de suppression de l'archive.

L'ordre des entrées de fichier dans le répertoire central n'a pas besoin de coïncider avec l'ordre des entrées de fichier dans l'archive.

### Entrées de fichiers ZIP

Les entrées du fichier ZIP sont disposées les unes après les autres, chaque entrée se composant de :

* En-tête de fichier local
* Champs de données supplémentaires facultatifs
* Données utilisateur (éventuellement compressées/éventuellement cryptées)

L'en-tête de fichier local de chaque entrée représente des informations sur le fichier telles que le commentaire, la taille du fichier et le nom du fichier. Les champs de données supplémentaires (facultatifs) peuvent contenir des informations pour les options d'extensibilité du format ZIP.

#### En-tête de fichier local

L'en-tête de fichier local a une structure de champ spécifique composée de valeurs multi-octets. Toutes les valeurs sont stockées dans l'ordre des octets little-endian où la longueur du champ compte la longueur en octets. Toutes les structures d'un fichier ZIP utilisent des signatures à 4 octets pour chaque entrée de fichier. La fin de la signature du répertoire central est 0x06054b50 et peut être distinguée à l'aide de sa propre signature unique. Voici l'ordre des informations stockées dans l'en-tête de fichier local.


|Décalage|Octets|Description
---|---|---|
|0|4|Signature d'en-tête de fichier local # 0x04034b50 (lu comme un nombre petit boutien)
|4|2|Version nécessaire pour extraire (minimum)
|6|2|Indicateur de bit à usage général
|8|2|Méthode de compression
|10|2|Heure de la dernière modification du fichier
|12|2|Date de la dernière modification du fichier
|14|4|CRC-32
|18|4|Taille compressée
|22|4|Taille non compressée
|26|2|Longueur du nom de fichier (n)
|28|2|Longueur de champ supplémentaire (m)
|30|n|Nom de fichier
|30+n|m|Champ supplémentaire

#### En-tête du fichier du répertoire central


|Décalage|Octets|Description
---|---|---|
|0|4|Signature d'en-tête de fichier de répertoire central # 0x02014b50
|4|2|Version faite par
|6|2|Version nécessaire pour extraire (minimum)
|8|2|Indicateur de bit à usage général
|10|2|Méthode de compression
|12|2|Heure de la dernière modification du fichier
|14|2|Date de la dernière modification du fichier
|16|4|CRC-32
|20|4|Taille compressée
|24|4|Taille non compressée
|28|2|Longueur du nom de fichier (n)
|30|2|Longueur de champ supplémentaire (m)
|32|2|Longueur du commentaire de fichier (k)
|34|2|Numéro de disque où le fichier commence
|36|2|Attributs du fichier interne
|38|4|Attributs de fichier externe
|42|4|Décalage relatif de l'en-tête du fichier local. Il s'agit du nombre d'octets entre le début du premier disque sur lequel le fichier apparaît et le début de l'en-tête du fichier local. Cela permet au logiciel de lire le répertoire central pour localiser la position du fichier à l'intérieur du fichier ZIP.
|46|n|Nom de fichier
|46+n|m|Champ supplémentaire
|46+n+m|k|Commentaire de fichier

#### Fin de l'enregistrement du répertoire central


|Décalage|Octets|Description
---|---|---|
|0|4|Fin de la signature du répertoire central # 0x06054b50
|4|2|Numéro de ce disque
|6|2|Disque où démarre le répertoire central
|8|2|Nombre d'enregistrements du répertoire central sur ce disque
|10|2|Nombre total d'enregistrements du répertoire central
|12|4|Taille du répertoire central (octets)
|16|4|Décalage du début du répertoire central, par rapport au début de l'archive
|20|2|Longueur du commentaire (n)
|22|n|Commentaire

## Références

* [Spécifications du format de fichier PKWARE ZIP](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Structure du fichier PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
