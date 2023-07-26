{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier TGZ - Fichier tar gzippé",
  "description":"En savoir plus sur le format de fichier TGZ et les API qui peuvent créer et ouvrir des fichiers TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Qu'est-ce qu'un fichier TGZ ?

Un fichier avec l'extension .tgz est un fichier d'archive TAR, composé de plusieurs fichiers et dossiers, qui a été compressé à l'aide du logiciel de compression Gnu Zip (gzip). Un fichier [TAR](/fr/compression/tar/) combine généralement plusieurs fichiers en un seul fichier pour la sauvegarde ou la distribution sur Internet. Il s'agit d'un fichier décompressé jusqu'à ce qu'il soit compressé à l'aide du logiciel gzip, après quoi il devient le fichier TGZ. Les fichiers TGZ, étant des fichiers compressés, occupent moins d'espace sur le disque et sont facilement transférables via Internet via e-mail. Certaines applications pouvant ouvrir les fichiers TGZ incluent WinZip, Apple Archive Utility, 7-Zip et WinRAR. Les fichiers TGZ sont principalement utilisés dans les systèmes UNIX et Linux.

## Format de fichier TGZ

Les fichiers TGZ sont enregistrés sous forme de fichiers binaires compressés à l'aide de l'algorithme de compression [GZ](/fr/compression/gz/).

## Comment décompresser le fichier .tgz sous Linux

Sur Linux/Unix OS, la commande suivante peut être utilisée pour décompresser les fichiers TGZ à partir de la ligne de commande.

```
tar zxvf tgzCompressedFile.tgz
```

La commande ci-dessus décompresse le fichier TGZ compressé et extrait ses fichiers de l'archive TAR sur le disque.
## Références ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipédia](https://en.wikipedia.org/wiki/Gzip)

