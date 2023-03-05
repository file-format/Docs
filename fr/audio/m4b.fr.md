{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "fichier", "extension", "format", "qu'est-ce que le format de fichier m4b", "musique", "format de fichier m4b", "M4b vs MP3", "spécification du format de fichier m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier M4B et les API qui peuvent créer, convertir et ouvrir des fichiers M4B.",
  "title" :"M4B - Format de fichier de livre audio MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Qu'est-ce qu'un fichier M4B ?

Le fichier avec l'extension .m4b est un livre audio généralement utilisé par les livres Apple et iTunes. L'audio utilisé dans ce format est stocké au format MPEG-4 et compressé à l'aide de l'encodage AAC. Un fichier M4B est très similaire à M4A mais prend en charge les fonctionnalités liées aux livres audio, telles que les signets et les sauts de chapitre. Les fichiers M4B sont disponibles dans les versions compatibles DRM et sans DRM. Les livres audio cryptés par DRM sont généralement des livres audio payants sur iTunes Store. Considérant que, sans DRM peut être trouvé facilement sur Internet.

## Format de fichier M4B

Les fichiers de livres audio contenant des métadonnées, des images, des signets et des hyperliens peuvent être enregistrés avec l'extension .m4a, mais généralement l'extension .m4b est utilisée lors de l'enregistrement, juste pour spécifier que le fichier a un format de fichier de livre audio. Fairplay DRM (Digital Rights Management) est utilisé par Apply pour protéger leurs fichiers M4B. Ainsi, les fichiers téléchargés depuis iTunes ne peuvent être lus que sur des appareils ou des ordinateurs autorisés.


## M4B contre M4A

M4B et [MP3](https://docs.fileformat.com/audio/mp3/) sont des formats de fichiers uniquement audio.

**M4B** : Gagne par rapport au MP3 en termes de qualité s'il encode les deux au même débit binaire. Le M4B est un fichier de livre audio compressé à l'aide de l'encodage AAC. Il est essentiellement associé à "MPEG-4 Audio Layer", les fichiers avec l'extension .m4b sont la couche audio des films MPEG-4 mais avec des fonctionnalités supplémentaires liées aux livres audio. Son objectif est de dépasser le MP3 et de devenir le nouveau standard de compression audio. Il est très proche du MP3 à bien des égards mais développé pour avoir une meilleure qualité dans une taille de fichier identique ou même plus petite. Le format M4B a été introduit pour la première fois par Apple. Le type de format est également réalisé en tant qu'encodeur sans perte Apple (ALE).

Par conséquent, actuellement, le M4B n'a pas pu obtenir le succès grand public du MP3 car le format audio n'est pas encore couramment lisible.

**Mp3** : Un format audio numérique bien connu de tous. Un tout premier format de compression sur la scène et devenu très célèbre parmi les auditeurs de musique. Son succès grand public est si rapide que le type de fichier peut être lu universellement et compatible avec presque tout, matériel ou logiciel. De manière générale, le M4A produira une meilleure qualité sonore, mais beaucoup diront que, que ce soit vrai ou non, la différence sonore n'est pas comparable, et ce serait une perte de temps d'essayer de convertir des fichiers MP3 en fichiers M4A. Enfin, la conversion ne fera que vous faire perdre la qualité sonore d'origine.

## Spécification du format de fichier M4B

Semblables à [M4A](/fr/audio/m4a/), les fichiers M4B se composent également de morceaux consécutifs. Chaque morceau a un en-tête de 8 octets et est subdivisé en :
- Taille de bloc de 4 octets (gros boutien, octet de poids fort en premier)
- Type de bloc de 4 octets - une des signatures prédéfinies : "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

Semblable à M4A, le premier morceau de M4B sera de type "ftype" et a un sous-type à l'offset 8. Le M4B défini par sous-type qui doit être "M4B_".

Itérer les morceaux, jusqu'à ce qu'un morceau de type inconnu soit détecté, il composera le fichier M4B (MPEG-4 Audio).

## Références

* [MPEG-4 Partie 14 - Par Wikipédia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemple de format et de récupération audio MPEG-4 Partie 14 (M4A, M4B, M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

