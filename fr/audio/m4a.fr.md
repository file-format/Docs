{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "fichier", "extension", "format", "qu'est-ce que le format de fichier m4a", "musique", "format de fichier m4a", "M4A vs MP3", "spécification du format de fichier m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier M4A et les API qui peuvent créer, convertir et ouvrir des fichiers M4A.",
  "title" :"M4A - Fichier audio MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Qu'est-ce qu'un fichier M4A ?

Le **format de fichier M4A** est un fichier audio créé à l'aide de l'AAC (Advanced Audio Coding) connu sous le nom de compression avec perte. Le mot M4A abrégé en MPEG 4 Audio. Ces fichiers audio ont généralement l'extension de fichier .m4a. Cela est particulièrement vrai pour le contenu non protégé. Il peut stocker divers types de contenu audio, tels que des livres audio, des chansons et des podcasts. M4A est généralement réalisé comme un format plus avancé que MP3, qui n'a généralement pas été conçu uniquement pour l'audio. Il s'agit simplement d'une couche audio dans les fichiers vidéo MPEG 1 ou 2.

Le format M4A est crypté par FairPlay Digital Rights Management, tel qu'il a été vendu via l'iTunes Store, utilisez l'extension .m4p. Les iPhones Apple utilisent l'audio MPEG-4 pour leurs sonneries, mais ces fichiers audio utilisent l'extension .m4r.


## M4A contre MP3

M4A et [MP3](https://docs.fileformat.com/audio/mp3/) sont des formats de fichiers uniquement audio.

**M4A** : meilleur que le MP3 en termes de qualité et de taille lorsqu'il est encodé au même débit binaire. L'extension de fichier .m4a est si courante car elle a été utilisée par Apple pour une utilisation dans l'iTunes Music Store. Le M4A est un fichier audio compressé à l'aide de la technologie MPEG-4 ; un algorithme de compression avec perte. Il est essentiellement associé à "MPEG-4 Audio Layer", les fichiers avec l'extension .m4a sont la couche audio des films MPEG-4. Il est destiné à dépasser le MP3 et à devenir le nouveau standard de compression audio. Il est très proche du MP3 à bien des égards, mais introduit pour avoir une meilleure qualité dans une taille de fichier identique ou même inférieure. Le format M4A a été introduit pour la première fois par Apple. Le type de format est également réalisé en tant qu'encodeur sans perte Apple (ALE).

Par conséquent, actuellement, le M4A n'a pas pu obtenir le succès grand public du MP3 car le format audio n'est généralement pas encore lisible. Il est en quelque sorte limité uniquement à MacOS, iPod et autres produits Apple.

**Mp3** : Le format audio numérique le plus connu. C'était aussi l'un des premiers formats de compression sur la scène et est devenu très populaire parmi les mélomanes. Son succès grand public est si rapide que le type de fichier peut être lu universellement et avec presque tout, matériel ou logiciel. De manière générale, le M4A produira une meilleure qualité sonore, mais beaucoup diront que, que ce soit vrai ou non, la différence sonore ne se distingue pas, et ce serait une perte de temps d'essayer de convertir des fichiers MP3 en fichiers M4A. Finalement, la conversion ne fera que vous faire perdre la qualité sonore d'origine.

## Spécification du format de fichier M4A

Les fichiers M4A sont constitués de morceaux consécutifs. Chaque morceau a un en-tête de 8 octets et est subdivisé en :
- Taille de bloc de 4 octets (gros boutien, octet de poids fort en premier)
- Type de bloc de 4 octets - une des signatures prédéfinies : "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

Le premier morceau sera de type "ftype" et a un sous-type à l'offset 8. Le M4A défini par le sous-type qui doit être "M4A_", pour le sous-type M4B doit être "M4B_" et pour le sous-type M4P doit être "M4P_".

Itérer les morceaux, jusqu'à ce qu'un morceau de type inconnu soit détecté, il composera le fichier M4A (MPEG-4 Audio).

## Références ##

* [MPEG-4 Partie 14 - Par Wikipédia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemple de format et de récupération audio MPEG-4 Partie 14 (M4A, M4B, M4P)] (https://www.file-recovery.com/m4a-signature-format.htm)

