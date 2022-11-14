{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier SY_ - Fichier SYS compressé",
  "description":"En savoir plus sur le format de fichier SY_ et les API qui peuvent créer et ouvrir des fichiers SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Qu'est-ce qu'un fichier SY_ ?

Un fichier SY_ est un fichier .sys compressé utilisé par les installateurs de logiciels pour réduire la taille des fichiers d'installation contenus dans le programme d'installation. Cela réduit la taille globale du programme d'installation. Les fichiers SY_ peuvent être décompressés à l'aide de l'utilitaire de ligne de commande Microsoft Expand qui décompose un ou plusieurs fichiers compressés.

## Format de fichier SY_ - Plus d'informations

Les fichiers SY_ sont enregistrés sur le disque sous forme de fichiers binaires compressés. Cependant, leur format de fichier interne n'est pas disponible publiquement. L'utilitaire de ligne de commande Microsoft Expand peut étendre les fichiers SY_ à l'aide de l'une des lignes de commande suivantes.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Une fois dépliés, les fichiers SY_ sont convertis en fichier [SYS](https://docs.fileformat.com/system/sys/).

Les fichiers SY_ sont similaires aux fichiers EX_ et DL_.

## Références

* [StuffIt - Par Wikipédia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

