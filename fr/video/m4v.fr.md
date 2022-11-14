{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "fichier", "extension", "format", "MPEG-4", "Gestion des droits numériques", "DRM", "Apple", "vidéo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"En savoir plus sur le format de fichier M4V et les API qui peuvent créer et ouvrir des fichiers M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Qu'est-ce qu'un fichier M4V ?

Le format de fichier **M4V**, développé par Apple, est un conteneur vidéo éventuellement protégé par la protection contre la copie Digital Rights Management (DRM) pour protéger la confidentialité ou la copie. Les vidéos et les pistes audio sont enveloppées dans des fichiers conteneurs pour indexer et organiser les flux de lecture. De plus, les conteneurs offrent également la fonctionnalité de chapitres similaires à ceux des DVD. Apple utilise M4V pour encoder des vidéos dans son iTunes Store. Il protège la reproduction non autorisée grâce à la protection contre la copie FairPlay d'Apple en permettant aux fichiers M4V d'être lus uniquement sur les ordinateurs autorisés ayant les comptes utilisés pour acheter la vidéo. Cependant, si la protection DRM est supprimée des fichiers M4V, ces fichiers peuvent être lus dans d'autres lecteurs vidéo en changeant l'extension de .m4v à .mp4, c'est pourquoi les fichiers M4V sont associés à MPEG-4. M4V utilise H.264 pour la vidéo et **[AAC](/fr/audio/aac/)** et Dolby Digital pour l'encodage et le décodage audio.

## Structure du fichier M4V ##

Les fichiers M4V ont des morceaux continus avec un en-tête de 8 octets, une taille de morceau de 4 octets et un type de morceau de 4 octets dans chaque morceau. Le premier morceau est "ftype" et a un sous-type à l'offset 8. M4V défini par le sous-type qui doit être "M4V_". D'autres types de morceaux sont des signatures prédéfinies : "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PICT". En itérant les morceaux, jusqu'à ce qu'un type inconnu soit détecté, nous composons le fichier M4V.

Voici un examen d'un exemple : Les données binaires d'un exemple de fichier m4v sont inspectées via Hex Viewer et on peut observer qu'elles commencent par une signature **ftyp** (hex : 66 74 79 70) à l'offset 4, qui définit QuickTime Type de fichier conteneur. Le sous-type de fichier est **M4V_** (hex : 4D 34 56 20) qui pointe vers le type de fichier M4V (MPEG-4). La taille du premier bloc est 32 (hex : 00 00 00 20, gros boutien, octet de poids fort en premier), taille située au décalage 0. Au décalage 32 (hex : 20) se trouve le deuxième bloc, qui a une taille de 30 322 (hex : 00 00 76 72, gros-boutiste, octet inférieur en premier) et tapez **moov** (hex : 6D 6F 6F 76). Le morceau suivant est situé au décalage 32+30 322#30 354 (hex : 00 00 76 92) et a une taille 8 (hex : 00 00 00 08) et le type **free** (hex : 66 72 65 65).
### Codecs utilisés dans M4V ###

#### Codec vidéo H.264 ####

H.264 est une norme de compression vidéo qui convertit la vidéo numérique dans un format qui nécessite moins d'espace lors de la transmission ou du stockage requis. M4V utilise H.264 pour la compression vidéo. Son application va du DVD, de la télévision, de la vidéoconférence et du streaming vidéo sur Internet. H.264 se compose de deux parties principales : Encoder – qui compresse la vidéo, Decoder – qui décompresse la vidéo compressée. Dans la figure ci-dessous, les processus de codage et de décodage sont mis en évidence, et d'autres processus sont couverts par la norme H.264.

##### Processus de codage et de décodage vidéo en H.264 #####

Pour le flux binaire H.264 compressé, l'encodeur vidéo exécute le processus de prédiction, de transformation et d'encodage. En même temps, le décodeur exécute le processus inverse de décodage, de transformation inverse et de reconstruction pour restituer le fichier vidéo. H.264 prend la moitié de la taille du MPEG.

#### Un codec audio ####

Advanced Audio Coding (AAC) est un codec audio pour la compression audio numérique avec perte et est utilisé dans un conteneur M4V. AAC est le successeur du format [MP3](/fr/audio/mp3/) et offre une meilleure qualité que le MP3 avec le même débit. Le format AAC jette certaines informations pendant le processus de compression, ce qui est de moindre importance. AAC est un codec basé sur des blocs à débit binaire variable (VBR) où chaque bloc décode jusqu'à 1024 échantillons de domaine temporel.

### Références ###

* [Wikipédia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipédia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

