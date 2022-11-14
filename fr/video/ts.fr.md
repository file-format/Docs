{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier TS - Fichier de flux de transport vidéo",
  "keywords" :[ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"Découvrez ce qu'est un fichier TS et les API qui peuvent créer et ouvrir des fichiers TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Qu'est-ce qu'un fichier TS ?

Un fichier avec l'extension .ts est un flux vidéo qui stocke les données sur des DVD. Il utilise l'algorithme de compression MPEG-2 ([.mpeg](/fr/video/mpg/)) pour atteindre une efficacité et une compatibilité maximales sur différents types de médias tels que le streaming et la diffusion sur Internet. Le format de fichier TS a été créé pour pouvoir être lu sur des appareils avec de mauvaises connexions Internet, comme la smart TV.

## Format de fichier TS - Plus d'informations

Les données d'un fichier TS sont similaires au fichier [MP4](/fr/video/mp4/), mais elles sont divisées en petits morceaux. Chaque morceau se compose d'un petit morceau de vidéo, suivi d'un petit morceau d'audio et d'une légende facultative. Un seul fichier TS se compose de plusieurs de ces morceaux. En plus de la vidéo, de l'audio et des sous-titres, chaque bloc comprend également des données supplémentaires pour détecter les erreurs dans le bloc. Pour cette raison, les fichiers TS sont un peu plus volumineux.

### Pourquoi utiliser le format de fichier TS ?

Donc, si les fichiers TS sont assez volumineux, quel avantage offre-t-il de les utiliser à la place d'autres formats de fichiers ? Eh bien, en radiodiffusion, les minuscules morceaux de vidéo et d'audio peuvent être envoyés sur les supports de communication (câblés ou radio) en temps réel. Les données supplémentaires dans les blocs sont utilisées par le récepteur pour ignorer les blocs sujets aux erreurs.

De plus, les fichiers TS sont utilisés car le système de diffusion n'a pas besoin de tout le flux pour le lire. La transmission peut être captée et exploitée en temps réel en assemblant l'audio et la vidéo.

## Comment lire des fichiers TS ?

Eh bien, les fichiers TS peuvent être ouverts et lus dans le populaire [lecteur multimédia VideoLAN VLC] (https://www.videolan.org/vlc/features.html) qui est disponible gratuitement en téléchargement.

## Références ##

* [Flux de transport MPEG - Wikipédia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

