{
  "date" : "2019-10-11",
  "keywords" :[ "fichier emz", "format de fichier emz", "qu'est-ce qu'un fichier emz", "fichier", "exemple emz", "extension de fichier emz","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier EMZ - Un fichier méta amélioré compressé Windows",
  "description":"En savoir plus sur le format de fichier EMZ et les API qui peuvent créer et ouvrir des fichiers EMZ.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Qu'est-ce qu'un fichier EMZ ?

Un fichier avec l'extension .emz est un conteneur compressé de métafichier amélioré (fichier [EMF](/fr/image/emf/)). Ceux-ci sont compressés à l'aide de la technique de compression [GZIP](/fr/compression/gz/) qui est la méthode de compression couramment utilisée sur les systèmes d'exploitation UNIX et LINUX. Unlink ZIP (/fr/compression/zip/), GZIP compresse l'archive dans son ensemble au lieu de compresser des fichiers individuels. Les fichiers EMZ sont plus petits que les fichiers EMF et permettent un transfert rapide lors du partage de fichiers en ligne. Certaines des applications pouvant ouvrir les fichiers EMZ incluent Microsoft Visio 2019, Microsoft Office 2019, XnView MP et File Viewer Plus.

## Format de fichier EMZ

Les fichiers EMZ sont [Gzip](/fr/compression/gz/) compressés et contiennent [EMF](/fr/image/emf/). Gzip utilise l'algorithme DEFLATE pour la compression de l'archive et est différent dans l'application de la compression. Un fichier EMZ peut être décompressé à l'aide d'utilitaires de compression GZip tels que GNU Zip. Le format de fichier se compose de :

* En-tête de fichier
* En-têtes facultatifs
* Données compressées
* Pied de page du fichier

Le format de fichier GZIP [spécifications version 4.3](http://tools.ietf.org/html/rfc1952) publié par Internet Engineering Task Force (IETF) contient des informations détaillées sur le format de fichier.

## Références

* [RFC1952 : spécification du format de fichier GZIP](http://tools.ietf.org/html/rfc1952), par [IETF](https://www.ietf.org/)
* [Métafichier Windows - Wikipédia](https://en.wikipedia.org/wiki/Windows_Metafile)

