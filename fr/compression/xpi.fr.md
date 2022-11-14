{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - Fichier de package d'installation multiplateforme",
  "description":"En savoir plus sur le format de fichier XPI et les API qui peuvent créer et ouvrir des fichiers XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Qu'est-ce qu'un fichier XPI ?

Un fichier XPI est une archive d'installation qui est compressée pour réduire la taille du fichier. Il est utilisé par les applications Mozilla pour l'installation de plugins et de fichiers complémentaires. Il contient un script d'installation ou un manifeste à la racine du fichier ainsi qu'un certain nombre de fichiers de données. Un fichier XPI peut contenir des thèmes, une boîte à outils ou des plugins Firefox que l'utilisateur peut installer pour faire partie du navigateur Firefox, Thunderbird ou SeaMonkey.

## Format de fichier XPI - Plus d'informations

Les fichiers XPI sont enregistrés sur le disque en tant qu'archives [ZIP](/fr/compression/zip/) qui combinent plusieurs fichiers en un seul fichier compressé. Les fichiers à l'intérieur d'un fichier XPI peuvent inclure un fichier de script d'installation tel que JS et des fichiers Web tels que [CSS](/fr/web/css/), [HTML](/fr/web/html/) et [JSON](/fr/web/json/ ). Parfois, il peut également contenir des fichiers image [PNG](/fr/image/png/) à utiliser comme icônes par le module complémentaire.

### Comment afficher le contenu du fichier XPI ?

Un fichier XPI est pratiquement une archive ZIP dont le contenu peut être visualisé en suivant les étapes suivantes.

* Changer l'extension du fichier de XPI à ZIP
* Extrayez le contenu du fichier à l'aide de n'importe quel utilitaire de décompression standard tel que WinZip (Windows, Mac), 7-Zip (Windows) ou Apple Archive Utility (Mac).

### Installer le fichier XPI sur Firefox Android

La plupart des gens sont curieux de savoir si les fichiers XPI peuvent être installés dans Firefox sur les appareils Android. Sur Android, vous pouvez installer un module complémentaire à partir d'un fichier XPI en localisant le fichier et en l'ouvrant avec Firefox.

## Références

* [XPInstall - Wikipédia](https://en.wikipedia.org/wiki/XPInstall)
* [Comment puis-je ouvrir une extension de fichier XPI ?] (https://support.mozilla.org/en-US/questions/1009049)

