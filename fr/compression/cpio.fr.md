{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier CPIO - Format de fichier d'archive Unix CPIO",
  "description":"Apprenez à savoir ce qu'est un fichier CPIO et les API qui peuvent créer et ouvrir des fichiers CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Qu'est-ce qu'un fichier CPIO ?

Un fichier CPIO est un fichier d'archive créé au format CPIO (Copy In Copy Out) d'Unix. Il est similaire au format de fichier TAR, à la différence qu'il n'est pas compressé. Les fichiers CPIO peuvent stocker des fichiers de périphérique, des liens symboliques et des attributs de fichiers étendus.

## Format de fichier CPIO

Une archive CPIO est créée sous la forme d'un fichier binaire non lisible par l'homme. Il stocke la collection de fichiers et de répertoires. Le contenu d'une archive CPIO est identifié par des informations de métadonnées telles que les noms de fichiers, les autorisations, la propriété et les horodatages. Ces informations de métadonnées sont également stockées dans le fichier d'archive pour un accès latéral par le système.

## Format des archives CPIO

Un fichier CPIO comprend un ou plusieurs fichiers membres concaténés. Chaque fichier de l'archive se compose d'un en-tête éventuellement suivi du contenu du fichier comme mentionné dans l'en-tête. L'archive contient un autre en-tête à la fin qui est décrit par un fichier vide nommé TRAILER !!.

### Types d'archives CPIO

Il existe deux types d'archives CPIO. Ceux-ci ne diffèrent que par le style de l’en-tête.

* Archives ASCII - Ces archives CPIO ont un en-tête imprimable qui devient partie intégrante de l'archive CPIO si l'archive elle-même est constituée de fichiers ASCII.
* Archives binaires - Ces archives CPIO ont des en-têtes binaires.

## Travailler avec les archives CPIO

### Comment créer des archives CPIO ?

Vous pouvez créer un CPIO sur les systèmes de type Unix à l'aide de la commande **cpio**. La commande suivante trouvera tous les fichiers et répertoires du répertoire actuel et de ses sous-répertoires. Cette sortie est ensuite redirigée vers la commande cpio qui générera une nouvelle archive CPIO nommée archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Comment extraire des fichiers des archives CPIO ?

La commande suivante extrait les fichiers d'une archive existante.

```
cpio -id < archive_cpio.cpio
```
Il lira le fichier archive.cpio à partir de l’entrée standard et extraira les fichiers dans le répertoire actuel.


## Les références

* [CPIO - Par Wikipédia](https://en.wikipedia.org/wiki/Cpio)
* [Format de fichier CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

