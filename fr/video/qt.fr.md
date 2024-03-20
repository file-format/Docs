{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier QT - Fichier vidéo rapide",
  "keywords" :["QT", "QuickTime vidéo", "format qt", "comment lire des fichiers qt", "Quick Movie File", "QTFF", "vidéo", "Apple" ],
  "description":"En savoir plus sur le format de fichier QT et les API qui peuvent créer et ouvrir des fichiers QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Qu'est-ce qu'un fichier QT ?

Un fichier avec une extension .qt est un fichier conteneur multimédia utilisé par le framework QuickTime pour stocker le contenu du fichier multimédia. Développé par Apple Inc., le format de fichier QuickTime (QTFF) est un fichier conteneur multimédia qui contient de l'audio, de la vidéo ou du texte pour une lecture ultérieure. C'est le format de choix pour l'échange de médias numériques entre les appareils, les applications et les systèmes d'exploitation. Les fichiers QT sont également enregistrés au format [MOV](/fr/video/mov/) qui a également été développé par Apple Inc. Certaines des applications qui peuvent ouvrir les fichiers QT incluent le lecteur Apple QuickTime, le lecteur multimédia VLC et Media Player Classic avec K- Pack de codecs léger.

## Format de fichier QT

Le QTFF est orienté objet et expose une collection flexible d'objets pour faciliter l'analyse et l'expansion. Chaque piste d'un fichier QT contient un flux multimédia codé numériquement ou une référence de données au flux multimédia situé dans un autre fichier. La structure de données hiérarchique composée d'objets appelés atomes agit comme des conteneurs de pistes. Les spécifications de format de fichier pour [format de fichier QT](https://developer.apple.com/documentation/quicktime-file-format) sont officiellement disponibles par Apple Inc pour la référence du développeur.

### Description du média

La description multimédia d'un fichier QuickTime est stockée séparément des données multimédias. Des informations telles que le nombre de pistes, le format de compression vidéo et les informations de synchronisation sont stockées dans la description du média (également appelée ressource de film, atome de film ou simplement le film). Les données multimédias sont référencées par un index dans cette structure multimédia. Les données multimédias sont les données d'échantillon réelles, telles que les images vidéo et les échantillons audio, utilisées dans le film.

### Atomes

Atom est l'unité de base du fichier QuickTime. Il y a deux champs principaux dans tout atome avant tout autre champ : les champs Taille et Type. Le champ de taille indique la taille de l'atome tandis que le champ de type indique le type de données stockées dans l'atome. Par nature, les atomes sont hiérarchiques, ce qui signifie qu'un atome peut contenir d'autres atomes qui peuvent encore en contenir d'autres. La disposition d'un exemple d'atome est illustrée dans l'image suivante.

Chaque atome a deux parties, un en-tête et des données. L'en-tête contient les champs de taille et de type et la partie données contient les données réelles. De plus, chaque champ est expliqué ci-dessous :

#### Taille de l'atome

L'en-tête et le contenu de l'atome sont indiqués par un nombre entier de 32 bits connu sous le nom de taille de l'atome. Le champ taille contient la taille de l'atome en octets, exprimée dans un entier non signé de 32 bits.

#### Type d'atome

Le type de l'atome est également indiqué par un entier 32 bits, qui est principalement traité comme un champ à quatre caractères avec une valeur knémonique, comme 'moov' (0x6D6F6F76) pour un atome de film, ou 'trak' (0x7472616B) pour un atome de piste. Une fois le type d'atome connu, cela permet d'interpréter ses données.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Structure du fichier ##

Les fichiers QT/MOV sont constitués de morceaux consécutifs. Chaque bloc a un en-tête de 8 octets : taille de bloc de 4 octets (gros boutien, octet de poids fort en premier) et type de bloc de 4 octets - l'une des signatures prédéfinies : "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Le premier morceau est de type "ftype" et a un sous-type à l'offset 8. MOV défini par le sous-type qui doit être "qt". Pour composer un fichier MOV, il est nécessaire d'itérer des morceaux jusqu'à ce qu'un type inconnu soit détecté.

Voici un exemple : En inspectant les données binaires d'un exemple de fichier MOV, il est évident qu'il commence par une signature **ftyp** (hex : 66 74 79 70) à l'offset 4, qui définit le type de fichier conteneur QuickTime. Le sous-type de fichier est **qt~_~_** (hex : 71 74 20 20) qui pointe vers le type de fichier MOV. La taille du premier bloc est de 32 (hex : 00 00 00 20, gros boutien, octet de poids fort en premier), taille située au décalage 0. Au décalage 32 (hex : 20) se trouve le deuxième bloc, qui a une taille de 8 et tapez **mdat** (hexa : 6D 64 61 74).

Le morceau suivant est situé à l'offset 32+8#40 (hex : 28) et a une taille de 3 263 028 (hex : 00 31 CA 34) et le type **mdat** (hex : 6D 64 61 74) à l'offset 44 (hex : 2C). Le morceau suivant est situé à l'offset 40 + 3 263 028#3 263 068 (hex : 00 31 CA 5C) et a une taille de 21 189 (hex : 00 00 52 C5) et le type **moov** (hex : 6D 6F 6F 76) à l'offset 1 836 019 574 (hex : 00 31 CA 60). C'est le dernier morceau, donc la taille totale du fichier est de 3 263 068 + 21 189 # 3 284 257 octets.

## Références ##

* [Format de fichier QT - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [Format de fichier QuickTime - Wikipédia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

