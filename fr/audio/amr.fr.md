{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "fichier", "extension", "format", "qu'est-ce qu'un fichier amr", "musique", "format de fichier amr", "fichier amr","convertir le fichier amr en mp3", "lire le fichier amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier AMR et les API qui peuvent créer, convertir et ouvrir des fichiers AMR.",
  "title" :"AMR - Fichier de codec multi-débit adaptatif",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Qu'est-ce qu'un fichier AMR ?
Le fichier avec l'extension .amr est un format de données audio pertinent pour le codec audio **Adaptive Multi-Rate** ; se compose d'un codec vocal à bande étroite multidébit qui code les signaux à bande étroite à un débit binaire de 4,75 à 12,2 kbit/s avec une voix de qualité interurbaine commençant à 7,4 kbit/s ; utilise l'adaptation de liaison pour sélectionner l'un des huit débits binaires différents.

## Format de fichier AMR
Le format de fichier AMR utilise de nombreuses techniques de codage, l'algorithme ACELP (Algebraic Code Excited Linear Prediction) l'une des meilleures techniques ; conçu pour compresser l'audio parlé par l'homme d'une manière plus efficace. L'AMR a été défini comme codec vocal ou vocal standard par 3GPP en 1999. Le format de fichier AMR est également utilisé pour stocker l'audio parlé en utilisant le codec audio **Adaptive Multi-Rate** qui est utilisé par de nombreux téléphones intelligents pour stocker les enregistrements. discours.

### Structure du format de fichier
L'AMR (Adaptive Multi-Rate) est un format audio ; largement utilisé dans diverses applications et appareils mobiles, généralement dans les lecteurs/enregistreurs audio ou dans les applications de type VoIP. La RAM peut en outre être classée comme :

1. RAM-NB (bande étroite)
2. AMR-WB (large bande)

Habituellement, RAM fait référence à RAM-NB. Le format de fichier AMR a la structure suivante :

Chaque fichier AMR contient un en-tête de 6 octets qui reconnaît le fichier en tant qu'audio AMR. Cet en-tête est toujours défini sur :
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Ceci est généralement similaire dans tous les fichiers AMR-NB. Si l'en-tête suit une norme, il est probable que le fichier soit corrompu et ne doit pas être utilisé. le fichier AMR se compose d'un nombre entier de trames audio compressées. Ces trames composent chacune 20 ms d'audio. Chaque image peut être encodée à l'aide de l'un des modes AMR-NB valides (0-7, 8 SID en mode DTX). Étant donné que les trames peuvent être codées à différents débits binaires, cette méthode typique est appelée Adaptive Multi-Rate (AMR).
#### Modes AMR
Voici les différents modes AMR et leurs débits correspondants :

|MODE| TAUX DE BITS |
---|---|
|0| AMR 4.75 - Encode à 4.75kbit/s |
|1 | AMR 5.15 - Encode à 5.15kbit/s |
|2 | AMR 5.9 - Encode à 5,9 kbit/s |
|3 | AMR 6.7 - Encode à 6,7 kbit/s |
|4 | AMR 7.4 - Encode à 7,4 kbit/s |
|5 | AMR 7.95 - Encode à 7.95kbit/s |
|6 | AMR 10.2 - Encode à 10,2 kbit/s |
|7 | AMR 12.2 - Encode à 12,2 kbit/s |

La taille de trame des modes AMR en octets (y compris l'octet d'en-tête) est indiquée ci-dessous :

|CMR |MODE |TAILLE DE TRAME( en octets)|
---|---|---|
|0 |RAM 4.75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |RAM 6.7 |18|
|4 |RAM 7.4 |20|
|5 |RMA 7.95 |21|

## Références ##

* [Codec audio multi-débit adaptatif - Par Wikipedia] (https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Format de charge utile RTP et format de stockage de fichiers pour les codecs audio AMR et AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

