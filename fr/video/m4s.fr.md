{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier M4S - Qu'est-ce qu'un fichier M4S ?",
  "description":"En savoir plus sur le format de fichier M4S et les API qui peuvent créer et ouvrir des fichiers M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Qu'est-ce qu'un fichier M4S ?

Un fichier M4S est un petit segment d'une vidéo diffusé sur Internet à l'aide de la technique de diffusion **MPEG-DASH**. Il contient un segment vidéo sous forme de données binaires. L'application réceptrice (généralement un navigateur Web ou des lecteurs multimédias) lit ces segments dans l'ordre dans lequel ils sont reçus. Le premier segment M4S est identifié par les données d'initialisation qu'il contient. En **résumé**, les fichiers M4S sont de petits segments multimédias individuels d'un fichier complet.

## Format de fichier M4S

Les fichiers M4S sont basés sur le [format ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Ces petits segments d'un gros fichier peuvent être téléchargés indépendamment via HTTP. Ainsi, si vous avez un fichier vidéo [MP4](/fr/video/mp4/) volumineux, il peut être diffusé à l'aide de la technique MPEG-DASH (Dynamic Adaptive Streaming over HTTP) en le segmentant en fichiers de segment M4S. Si ce fichier vidéo volumineux est téléchargé sur le disque en tant que M4S, plusieurs fichiers M4S sont téléchargés. Si tous ces segments .m4s sont concaténés, un fichier lisible complet est produit. Les lecteurs multimédias ne peuvent lire le fichier que si le premier segment d'initialisation est également disponible avec le fichier.

## À propos de la diffusion MPEG-DASH

MPEG-DASH utilise une technique de streaming à débit binaire adaptatif qui permet de diffuser du contenu multimédia de haute qualité sur Internet. Cela se fait en divisant le contenu en une séquence de petits segments qui sont diffusés via HTTP. Les fichiers multimédias volumineux tels que les films, les podcasts ou la diffusion en direct d'un événement sportif peuvent être diffusés de cette manière. Ces segments sont codés à différents débits binaires. Les lecteurs multimédia compatibles MPEG-DASH sélectionnent automatiquement le segment avec le débit binaire le plus élevé à l'aide d'un algorithme d'adaptation du débit binaire. Cela évite de bloquer ou de remettre en mémoire tampon des événements dans la lecture.

### API Open Source pour les fichiers M4S

Il existe des API open source disponibles qui peuvent être utilisées pour lire et convertir des fichiers M4S.

* [libdash](https://github.com/bitmovin/libdash) - API .NET pour les fichiers M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Client Javascript pour le fichier M4S
* [Go Library pour créer des fichiers Dash] (https://github.com/zencoder/go-dash)

### API Open Source pour convertir M4S en MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Références ###

* [Format de fichier multimédia de base ISO (ISOBMFF)] (https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* Dynamic Adaptive Streaming over HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

