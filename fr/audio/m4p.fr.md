{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "fichier", "extension", "format", "qu'est-ce que le format de fichier m4p", "musique", "format de fichier m4p", "M4b vs MP3", "spécification du format de fichier m4p "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier M4P et les API qui peuvent créer, convertir et ouvrir des fichiers M4P.",
  "title" :"M4P - Format de fichier de livre audio MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Qu'est-ce qu'un fichier M4P ?
Le fichier avec l'extension .m4p est un fichier audio qui est généralement disponible sur Apple iTunes Store pour téléchargement. En d'autres termes, nous pouvons dire que M4P est un fichier AAC mais protégé contre la copie en utilisant une gestion des droits numériques (DRM). Cela signifie que les fichiers M4P ne peuvent être lus que sur des systèmes ou appareils autorisés. Habituellement, les fichiers M4P sont spécifiques aux appareils multimédia Apple. Ainsi, ces fichiers ne peuvent être lus que sur les macbooks Apple, les podcasts, les téléphones intelligents comme l'iPhone 6 ou l'iPhone 7.

## Format de fichier M4P
Le M4P signifie MPEG 4 Protected (audio), et il encode l'audio avec un codec audio avancé (AAC) et protège le fichier contre l'utilisation non autorisée du fichier. Ce format de fichier est généralement considéré comme le format de fichier audio d'iTunes Music Store. Apple utilise son système FairPlay Digital Rights Management (DRM) pour protéger les fichiers M4P. FairPlay DRM est basé sur une technologie développée par Veridisc. Son mécanisme de protection fonctionne en cryptant le flux audio AAC à l'aide du cryptage AES. L'utilisateur reçoit une clé principale qui est attribuée à son compte pour le décryptage. Ce format de fichier a été introduit en remplacement du format de fichier MP3, car le MP3 n'était pas initialement conçu comme un fichier audio, mais comme couche III dans un fichier vidéo MPEG 1 ou 2.


## Spécifications du format de fichier M4P

Semblables à [M4A](/fr/audio/m4a/), les fichiers M4P se composent également de morceaux consécutifs. Chaque morceau a un en-tête de 8 octets et est subdivisé en :
- Taille de bloc de 4 octets (gros boutien, octet de poids fort en premier)
- Type de bloc de 4 octets - une des signatures prédéfinies : "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt ", "ctab", "ssrc".

Semblable à M4A, le premier morceau de M4P sera de type "ftype" et a un sous-type à l'offset 8. Le M4P défini par sous-type qui doit être "M4P_".

Itérer les morceaux, jusqu'à ce qu'un morceau de type inconnu soit détecté, il composera le fichier M4P (MPEG-4 Audio).

## Références ##

* [MPEG-4 Partie 14 - Par Wikipédia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemple de format et de récupération audio MPEG-4 Partie 14 (M4A, M4B, M4P)] (https://www.file-recovery.com/m4a-signature-format.htm)

