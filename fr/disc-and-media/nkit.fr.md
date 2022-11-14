{
  "date" : "2022-04-01",
  "keywords" :[ "fichier nkit", "format de fichier nkit", "qu'est-ce qu'un fichier nkit", "fichier", "exemple nkit", "extension de fichier nkit","extension", "format", "pied de page nkit", "fichier format de nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier NKIT et les API qui peuvent créer et ouvrir des fichiers NKIT.",
  "title" :"NKIT - Format de fichier d'image disque",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Qu'est-ce qu'un fichier NKIT ?

Un fichier NKIT est une image disque de données extraites des jeux NintendoWii et GameCube. NKIT est pour le format Nintendo Toolkit. Le fichier de compression [ISO](/fr/compression/iso/) qui en résulte utilise les principales données de ces jeux pour être exécutés avec des programmes d'émulation tels que Dolphin, Swiss et Nintendont. NKit est disponible dans des formats de fichiers bruts (iso) et compressés (gcz) qui ont tous deux été conçus en tenant compte de la lisibilité et de la taille.

## Format de fichier NKIT

Le format de fichier NKit est un format sans perte et est utilisé pour réduire et restaurer les images Nintendo Wii et GameCube. Les formats sont disponibles aux formats de fichier ISO et GCZ pour chacun des jeux GameCube et Wii.

|Système |Format |Matériel pris en charge |Dolphin pris en charge |Restauration 1:1 |Remarques|
---|---|---|---|---|---|
|GameCube| nkit.iso| Oui |Oui| Oui | Identique à l'iso GameCube compacté |
|GameCube| nkit.gcz| Non | Oui | Oui |GCZ est le propre format de compression recherchable par bloc de Dolphin|
|Wii| nkit.iso| Non Oui| Oui| Format RVT-H jouable uniquement dans Dolphin |
|Wii| nkit.gcz| Non Oui| Oui| RVT-H en GCZ jouable en Dolphin uniquement |

### En-tête NKIT

L'en-tête du format de fichier NKIT est le suivant.

|Décalage |Longueur |Nom|
---|---|---|
|0x200 |0x4 |En-tête NKit 'NKIT'|
|0x204 |0x4 |Version NKit ' v01'|
|0x208 |0x4 |Image source originale CRC32|
|0x20C |0x4 |NKit CRC - rend le fichier NKit CRC32 égal au CRC source à 0x208 (à 0x4 dans GCZ)|
|0x210 |0x4 |Longueur de l'image source|
|0x214 |0x4 |Forced Junk ID (Lorsque l'ID de disque diffère - rare - GameCube uniquement)|
|0x218 |0x4 |Wii Mettre à jour la partition CRC32 si supprimée lors de la conversion|

## Références ##

* [Format de fichier NKIT - par gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

