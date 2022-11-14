{
  "date" : "2019-10-11",
  "keywords" :[ "fichier wmz", "format de fichier wmz", "qu'est-ce qu'un fichier wmz", "fichier", "exemple wmz", "extension de fichier wmz","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier WMZ - Métafichier Windows compressé",
  "description":"En savoir plus sur le format de fichier WMZ et les API qui peuvent créer et ouvrir des fichiers WMZ.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Qu'est-ce qu'un fichier WMZ ?

Un fichier avec l'extension .wmz est une version compressée de [WMF](/fr/image/wmf/) et est utilisé pour stocker des métafichiers. Il s'agit d'un fichier de niveau intermédiaire généré par les anciennes versions des applications Microsoft Office et qui n'est pas très utilisé. Les fichiers WMZ sont générés lors de l'enregistrement des documents au format [HTML](/fr/web/html/). Ceux-ci peuvent également être générés lors de l'envoi par courrier électronique de documents contenant des images clipart intégrées, des équations, etc. Les applications pouvant ouvrir des fichiers WMZ incluent (mais sans s'y limiter) Corel Winzip et Apple Archive Utility.

## Format de fichier WMZ

Les fichiers WMZ sont [Gzip](/fr/compression/gz/) compressés et contiennent [WMF](/fr/image/WMF/). Gzip utilise l'algorithme DEFLATE pour la compression de l'archive. GZIP est différent du format d'archive [ZIP](/fr/compression/zip/) car il applique un algorithme de compression à l'archive complète plutôt qu'aux fichiers individuels. Le format de fichier se compose de :

* En-tête de fichier
* En-têtes facultatifs
* Données compressées
* Pied de page du fichier

Le format de fichier GZIP [spécifications version 4.3](http://tools.ietf.org/html/rfc1952) publié par Internet Engineering Task Force (IETF) contient des informations détaillées sur le format de fichier.

## Références

* [RFC1952 : spécification du format de fichier GZIP](http://tools.ietf.org/html/rfc1952), par [IETF](https://ietf.org)
* [Métafichier Windows - Wikipédia](https://en.wikipedia.org/wiki/Windows_Metafile)

