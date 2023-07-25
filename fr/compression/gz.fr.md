{
  "date" : "2019-10-11",
  "keywords" :[ "fichier gz", "format de fichier gz", "qu'est-ce qu'un fichier gz", "fichier", "exemple gz", "extension de fichier gz","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier GZ - Fichier d'archive compressé GNU",
  "description":"Découvrez ce qu'est un fichier GZ et les API qui peuvent créer et ouvrir des fichiers GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier GZ ?

Un fichier GZ est une archive compressée créée à l'aide de l'algorithme de compression standard [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Il peut contenir plusieurs fichiers compressés, répertoires et stubs de fichiers. Ce format a été initialement développé pour remplacer les formats de compression sur les systèmes UNIX. et reste l'un des types d'archives les plus courants sur les systèmes Linux. Des applications telles que [WinZip](https://www.winzip.com/en/) peuvent ouvrir des fichiers GZ pour afficher leur contenu sur Windows et MacOS.

## Format de fichier GZ - Plus d'informations

Gzip utilise l'algorithme [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) pour la compression de l'archive et diffère du format d'archive [ZIP](/fr/compression/zip/) en appliquant l'algorithme de compression sur l'archive complète plutôt que des fichiers individuels. La version 4.3 des spécifications du format de fichier GZIP publiée par Internet Engineering Task Force (IETF) contient des informations détaillées sur le format de fichier. Le format de fichier se compose de :

* En-tête de fichier
* En-têtes facultatifs
* Données compressées
* Pied de page du fichier

## En-tête de fichier GZ ##

L'en-tête du fichier GZ se compose de 10 octets comme suit :

|Décalage|Taille|Valeur|Description
---|---|---|---|
|0|2|0x1f 0x8b|Numéro magique identifiant le type de fichier
|2|1| |Méthode de compression * 0-7 (réservé) * 8 (dégonfler)
|3|1| |Drapeaux de fichier
|4|4| |horodatage 32 bits
|8|1| |Drapeaux de compression
|9|1| |Identifiant du système d'exploitation

### Indicateurs de fichier ###

|Valeur|Identifiant|Description
---|---|---|
|0x01|FTEXT|Si défini, les données non compressées doivent être traitées comme du texte au lieu de données binaires. Cet indicateur suggère une conversion de fin de ligne pour les fichiers texte multiplateformes mais ne l'applique pas.
|0x02|FHCRC|Le fichier contient une somme de contrôle d'en-tête (CRC-16)
|0x04|FEXTRA|Le fichier contient des champs supplémentaires
|0x08|FNAME|Le fichier contient une chaîne de nom de fichier d'origine
|0x10|FCOMMENT|Le fichier contient un commentaire
|0x20| |Réservé
|0x40| |Réservé
|0x80| |Réservé

### Système opérateur ###

|Valeur|Description
---|---|
|0|Système de fichiers FAT (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (ou OpenVMS)
|3|Unix
|4|VM/CMS
|5|Conditions d'utilisation Atari
|6|Système de fichiers HPFS (OS/2, NT)
|7|Macintosh
|8|Système Z
|9|CP/M
|10|TOP-20
|11|Système de fichiers NTFS (NT)
|12|QDOS
|13|Gland RISCOS
|255|inconnu

## En-têtes optionnels GZ ##

Les en-têtes supplémentaires facultatifs sont ceux indiqués par les drapeaux de fichier et incluent des informations telles que le nom de fichier d'origine, des champs supplémentaires, des commentaires et la somme de contrôle de l'en-tête.

## Données compressées ##

Cette section contient les données compressées à l'aide de l'algorithme de compression DEFLATE.

## Pied de page du fichier GZ ##

Le pied de page du fichier a une taille de 8 octets et contient les informations suivantes.

|Décalage|Taille|Description
---|---|---|
|0|4|Somme de contrôle (CRC-32)
|4|4|Valeur de la taille des données non compressées en octets

## Références ##

* [gzip - Wikipédia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952 : spécification du format de fichier GZIP](https://datatracker.ietf.org/doc/html/rfc1952), par l'IETF.

