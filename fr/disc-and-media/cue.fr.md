{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "fichier", "extension", "format", "qu'est-ce qu'un fichier cue", "musique", "format de fichier cue", "spécification du format de fichier cue", "feuille cue", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier CUE et les API qui peuvent créer, convertir et ouvrir des fichiers CUE.",
  "title" :"CUE - Fichier de feuille de repère",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Qu'est-ce qu'un fichier CUE ?

Un fichier avec l'extension .cue, également connu sous le nom de fichier de feuille de repère, est un fichier de métadonnées qui contient des informations sur la disposition des pistes sur un CD ou un DVD. Ceux-ci sont pris en charge par les lecteurs multimédias et les applications de création de disques optiques. Les principales données audio stockées sur le CD sont référencées par le fichier de repère, ainsi que les spécifications des longueurs de piste, des titres de disque et des interprètes. Ainsi, si un seul fichier audio contient plusieurs pistes, le fichier de repère peut être utilisé pour diviser l'audio en plusieurs fichiers ou référencer différentes pistes.

## Format de fichier CUE

Les fichiers CUE ou cue sheet sont stockés dans un format texte brut lisible par l'homme. Les informations contenues dans un fichier cue sont des commandes avec un ou plusieurs paramètres. Ces commandes s'appliquent soit à l'ensemble du fichier, soit à une piste individuelle, selon la commande particulière et le contexte. Le guide de l'utilisateur CDRWIN décrit les spécifications de la syntaxe et de la sémantique de la feuille de repère.

## Commandes essentielles de la feuille CUE

|Commande|Description|
---|---|
|FICHIER| Fait référence au fichier contenant les données et à son format tel que [MP3](/fr/audio/mp3/), [WAV](/fr/audio/wav/), ou image de disque binaire ordinaire)|
|SUIVI| Définit les informations de contexte de piste telles que son numéro et son type ou son mode.|
|INDICE| Représente la position sous la forme d'un index dans le FICHIER. Le format est mm:ss:ff (image minute-seconde).|
|PREGAP et POSTGAP|Indique le prégap ou le post-gap d'une piste, qui n'est stocké dans aucun fichier de données. La longueur est spécifiée dans le même format d'image minute-seconde que pour INDEX.|

### Exemple de fiche CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Références

* [Fichier .cda - Par Wikipédia](https://en.wikipedia.org/wiki/.cda_file)

