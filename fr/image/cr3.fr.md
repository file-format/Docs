{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier CR3 - Fichier image Canon Raw 3",
  "description":"En savoir plus sur le format de fichier CR3 et les API qui peuvent créer et ouvrir des fichiers CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Qu'est-ce qu'un fichier CR3 ?

Un fichier CR3 est un format de fichier d'image Canon RAW créé par certains appareils photo numériques Canon. Il a été introduit par Canon pour remplacer le format de fichier CR2 et est utilisé par certains appareils numériques Canon. Les fichiers CR3 stockent les données d'image originales non traitées sans perte capturées par l'appareil photo. L'utilisation de ces images brutes fournit des images de haute qualité et laisse beaucoup de place pour l'édition aux photographes. En plus des données d'image principales, les fichiers CR3 stockent également des informations de métadonnées sur l'image.

## Format de fichier CR3

Les fichiers CR3 sont stockés sur le disque en tant que fichier binaire au format de fichier multimédia de base ISO (ISO/IEC 14496-12) et incluent également des [balises Canon] personnalisées (https://exiftool.org/TagNames/Canon.html#uuid). Il inclut également le [codec Canon 'crx'](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) qui est un mélange de JPEG-LS (Rice-Golomb + RLE codage) et JPEG-2000 (LeGall 5/3 DWT + quantification).

## Balises personnalisées CR3

Les fichiers CR3 contiennent des balises personnalisées à des fins différentes. Certaines de ces balises sont les suivantes.

|Identifiant de balise| Nom de la balise| Inscriptible |Valeurs / Notes|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Balises Canon CCTP|
|'CMT1' |IFD0| - |--> Balises EXIF|
|'CMT2' |ExifIFD| - |--> Balises EXIF|
|'CMT3' |MarkerNoteCanon| - |--> Balises Canon|
|'CMT4' |InfoGPS| - |--> Balises GPS|
|'CNCV' |Version Compresseur| non | |
|'CNOP' |CanonCNOP| - |--> Balises Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Balises Canon CNTH|
|'THMB' |ThumbnailImage| non | |

## Références

* [Format de fichier CR2] (http://lclevy.free.fr/cr2/)
* [Balises Canon](https://exiftool.org/TagNames/Canon.html#uuid)

