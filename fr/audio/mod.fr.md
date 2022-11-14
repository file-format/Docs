{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "fichier", "extension", "format", "qu'est-ce que le format de fichier mod", "musique", "format de fichier mod", "mod vs MP3", "spécification du format de fichier mod "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier MOD et les API qui peuvent créer, convertir et ouvrir des fichiers MOD.",
  "title" :"MOD - Fichier de module de musique",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Qu'est-ce qu'un fichier MOD ?
Un fichier avec l'extension .mod est un fichier de module de musique créé en utilisant le format de module de musique standard, qui est basé sur le **format de module Amiga** développé par Karsten Obarski et publié avec le logiciel **Ultimate Soundtracker** pour le Commodore Système Amiga. Semblable à un fichier [MIDI](/fr/audio/mid/), il se compose de motifs de notes et d'échantillons sonores, représentant différents instruments qui sont reproduits en fonction des notes. Les fichiers MOD sont particulièrement utilisés dans les jeux vidéo comme musique de fond et dans la sous-culture de l'art informatique **demoscene**.

## Format de fichier MOD

Le MOD est un format de fichier informatique utilisé sa fonction de base est de représenter la musique, et c'était le premier format de fichier de module. Les fichiers MOD utilisent l'extension de fichier .mod, sauf sur l'**Amiga** qui lit l'en-tête d'un fichier pour déterminer le type de fichier, il ne s'appuie donc pas sur les extensions de nom de fichier. Un fichier MOD consiste en un ensemble de divers instruments sous forme d'échantillons, un certain nombre de modèles spécifiant comment et quand les échantillons doivent être joués, et une liste des modèles à jouer dans quel ordre.

### Spécifications du format de fichier MOD

Un modèle de fichier MOD est en fait conçu dans une interface utilisateur de séquenceur comme un tableau avec une colonne par canal, donc ce tableau a quatre colonnes (une pour chaque canal matériel Amiga. Chaque colonne a 64 lignes).

Une cellule du tableau peut provoquer l'une des actions suivantes sur le canal de sa colonne lorsque l'heure de sa ligne est atteinte :

- Démarrer un instrument jouant une nouvelle note dans ce canal à un volume donné, éventuellement avec un effet spécial appliqué dessus
- Modifier le volume ou l'effet spécial appliqué à la note actuelle
- Modifier le flux de modèle ; sauter à une position de chanson ou de motif spécifique ou boucler à l'intérieur d'un motif
- Ne fais rien; toute note existante jouant dans ce canal continuera à jouer

Un instrument est un échantillon unique accompagné d'une spécification facultative indiquant quelle partie de l'échantillon peut être répétée pour contenir une note solide.

### Horaire
Le délai minimum était de 0,02 seconde dans le fichier MOD d'origine, ou un intervalle de « suppression verticale » (VSync), car le logiciel d'origine utilisait la synchronisation VSync du moniteur fonctionnant à 50 Hz (pour PAL) ou 60 Hz (pour NTSC) pour le chronométrage.

## Références

* [MOD (format de fichier) - Par Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

