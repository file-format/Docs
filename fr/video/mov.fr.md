{
  "date" : "2019-10-11",
  "keywords" :[ "fichier mov", "format de fichier mov", "qu'est-ce qu'un fichier mov", "fichier", "exemple mov", "extension de fichier mov","extension", "format", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier MOV - Format de fichier de film Apple QuickTime",
  "description":"En savoir plus sur le format de fichier MOV et les API qui peuvent créer et ouvrir des fichiers MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Qu'est-ce qu'un fichier MOV ?

Un fichier MOV est un type de fichier vidéo, développé par Apple Inc., qui contient une ou plusieurs pistes. Chaque piste stocke un film, de l'audio, des clips vidéo et des sous-titres. C'est un conteneur multimédia qui peut stocker différents types d'éléments multimédias. Le format vidéo MOV est compatible avec les systèmes Windows et Macintosh. Il utilise le codage MPEG-4 pour la compression et les pistes sont conservées dans des objets appelés atomes qui sont placés dans une structure de données hiérarchique.

## Bref historique du format de fichier MOV

Le format de fichier MPEG-4 a évolué à partir de la spécification QuickTime File Format (**QTFF**) en 2001. L'Organisation internationale de normalisation a approuvé le format et les spécifications des systèmes MPEG-4 Partie 1 ont été publiées en 1999. En 2001, un fichier de révision format [MP4](/fr/video/mp4/) a été publié.

La première version de MP4 a été révisée en 2003 sous le nom de MPEG-4 Part 14 (ISO/IEC 14496-14:2003). En 2004, MP4 a été généralisé pour définir une structure générale pour tous les fichiers multimédias temporels. Par conséquent, il est maintenant utilisé comme base pour divers autres formats de fichiers multimédias.

## Format de fichier QuickTime (QTFF) - Plus d'informations

Afin de travailler avec le multimédia numérique, QTFF peut contenir de nombreux types de données. Il s'agit d'un format idéal pour l'échange de médias numériques, car le format définit les normes de description de tout type de structures médiatiques. Le format de fichier consiste en une collection flexible d'objets orientés objet. Pour le stockage des films sur disques, QuickTime utilise deux structures, à savoir les « atomes » et les « atomes QT ».

### Atomes

Atom est l'unité de base du fichier QuickTime. Il y a deux champs principaux dans tout atome avant tout autre champ : les champs Taille et Type. Le champ de taille indique la taille de l'atome tandis que le champ de type indique le type de données stockées dans l'atome. Par nature, les atomes sont hiérarchiques, ce qui signifie qu'un atome peut contenir d'autres atomes qui peuvent encore en contenir d'autres. La disposition d'un exemple d'atome est illustrée dans l'image suivante.

Chaque atome a deux parties, `header` et `data`. L'en-tête contient les champs de taille et de type et la partie données contient les données réelles. De plus, chaque champ est expliqué ci-dessous :

### Taille de l'atome

L'en-tête et le contenu de l'atome sont indiqués par un nombre entier de 32 bits connu sous le nom de taille de l'atome. Le champ taille contient la taille de l'atome en octets, exprimée dans un entier non signé de 32 bits.

### Type d'atome

Le type de l'atome est également indiqué par un entier 32 bits, qui est principalement traité comme un champ à quatre caractères avec une valeur knémonique, comme 'moov' (0x6D6F6F76) pour un atome de film, ou 'trak' (0x7472616B) pour un atome de piste. Une fois le type d'atome connu, cela permet d'interpréter ses données.

### Atomes QT et conteneurs d'atomes

Les atomes QT fournissent un format de stockage à usage général et ont un en-tête étendu composé des champs Taille, Type, ID d'atome et Nombre d'atomes enfants. Les atomes QT sont enveloppés dans un conteneur d'atomes, une structure de données unique ayant un en-tête avec un nombre de verrous. Il y a un atome racine dans chaque conteneur d'atome qui est l'atome QT. La disposition de l'atome QT est illustrée dans la figure ci-dessous.

L'en-tête du conteneur d'atome QT contient les données suivantes :

Réservé : un élément de 10 octets avec une valeur de 0.

Nombre de verrous : nombre entier de 16 bits avec une valeur de 0.

Les en-têtes d'atomes QT contiennent les données suivantes :

**Taille -** L'en-tête et le contenu de l'atome QT sont indiqués en octets par un entier de 32 bits. Dans le cas d'un atome feuille, alors ce champ contient la taille d'un seul atome.

**Type -** Le type de l'atome est indiqué par un entier de 32 bits. S'il s'agit de l'atome racine, la valeur est définie sur "sean".

**Atom ID -** Il s'agit d'un entier 32 bits qui indique l'ID de l'atome et doit être unique pour tous les frères et sœurs. Atome racine toujours la valeur de l'ID d'atome comme 1.

**Réservé -** Un entier 16 bits qui doit être défini sur 0.

**Child count -** Entier 16 bits indiquant le nombre d'atomes enfants d'un atome.

**Réservé -** Un entier 32 bits qui doit être défini sur 0.

## Structure de fichier des fichiers MOV

Les fichiers MOV sont constitués de morceaux consécutifs. Chaque bloc a un en-tête de 8 octets : taille de bloc de 4 octets (gros boutien, octet de poids fort en premier) et type de bloc de 4 octets - l'une des signatures prédéfinies : "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Le premier morceau est de type "ftype" et a un sous-type à l'offset 8. MOV défini par le sous-type qui doit être "qt". Pour composer un fichier MOV, il est nécessaire d'itérer des morceaux jusqu'à ce qu'un type inconnu soit détecté.

Voici un "exemple d'exemple": En inspectant les données binaires d'un exemple de fichier MOV, il est évident qu'il commence par une signature **ftyp** (hex : 66 74 79 70) à l'offset 4, qui définit le type de fichier conteneur QuickTime. Le sous-type de fichier est **qt~_~_** (hex : 71 74 20 20) qui pointe vers le type de fichier MOV. La taille du premier bloc est de 32 (hex : 00 00 00 20, gros boutien, octet de poids fort en premier), taille située au décalage 0. Au décalage 32 (hex : 20) se trouve le deuxième bloc, qui a une taille de 8 et tapez **mdat** (hexa : 6D 64 61 74).

Le morceau suivant est situé à l'offset 32+8#40 (hex : 28) et a une taille de 3 263 028 (hex : 00 31 CA 34) et le type **mdat** (hex : 6D 64 61 74) à l'offset 44 (hex : 2C). Le morceau suivant est situé à l'offset 40 + 3 263 028#3 263 068 (hex : 00 31 CA 5C) et a une taille de 21 189 (hex : 00 00 52 C5) et le type **moov** (hex : 6D 6F 6F 76) à l'offset 1 836 019 574 (hex : 00 31 CA 60). C'est le dernier morceau, donc la taille totale du fichier est de 3 263 068 + 21 189 # 3 284 257 octets.

## Comment convertir un fichier MOV ?

Il existe de nombreux lecteurs multimédias et éditeurs vidéo logiciels disponibles pour convertir les fichiers MOV en d'autres formats de fichiers vidéo populaires. Certains des lecteurs multimédias capables de convertir des fichiers MOV vers d'autres formats incluent :

* Lecteur multimédia VideoLAN VLC
* Lecteur Eltima Elmedia

Plusieurs lecteurs multimédias et éditeurs vidéo, y compris le lecteur multimédia VideoLAN VLC et Eltima Elmedia Player, peuvent convertir des fichiers MOV vers d'autres formats. Ces logiciels peuvent convertir des fichiers MOV aux formats vidéo suivants.

* Vidéo MPEG-4 - [MP4](/fr/video/mp4/)
* Vidéo WebM - [WEBM](/fr/video/webm/)
* Flux de transport vidéo - [TS](/fr/video/ts/)
* Format des systèmes avancés - [ASF](/fr/video/ts/)
* Audio Ogg Vorbis - [OGG](/fr/audio/ogg/)
* Audio MP3 - [MP3](/fr/audio/mp3/)
* Codec audio sans perte gratuit - [FLAC](/fr/audio/flac/)
* WAVE Audio - [WAV](/fr/audio/wav/)

## API open source pour les fichiers MOV

* [React Native API pour convertir MOV en MP4] (https://github.com/taltultc/react-native-mov-to-mp4)
* [API Python pour réparer les fichiers MOV] (https://github.com/nrosenstein-stuff/movrepair)
* [API Ruby pour convertir MOV en GIF] (https://github.com/skygroundmedia/convert-mov-to-gif)

## Références

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

