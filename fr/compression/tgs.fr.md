{
  "date" : "2019-10-11",
  "keywords" :[ "fichier tgs", "format de fichier tgs", "qu'est-ce qu'un fichier tgs", "fichier", "exemple tgs", "extension de fichier tgs","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Format de fichier d'autocollant animé Telegram",
  "description":"En savoir plus sur le format de fichier TGS et les API qui peuvent créer et ouvrir des fichiers TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Qu'est-ce qu'un fichier TGS ?

Un fichier avec l'extension .tgs est un fichier d'autocollant animé qui a été introduit par le service de messagerie multiplateforme, [Telegram](https://core.telegram.org/stickers#animated-stickers). Les autocollants animés sont utilisés par les utilisateurs d'applications de messagerie pour envoyer un contenu plus amélioré et plus vivant dans les messages, contrairement aux graphiques statiques qui sont des images fixes. Telegram utilisait initialement le format de fichier [WEBP](/fr/image/webp/) pour les autocollants d'images fixes. Le format de fichier TGS peut stocker des données d'animation à des résolutions plus élevées et une taille de fichier plus petite par rapport aux autocollants WEBP statiques. Les fichiers TGS peuvent être ouverts à l'aide d'applications telles que Telegram, 7-zip, Apple Archive Utility et Corel WinZip.

## Format de fichier TGS

Telegram a introduit le format de fichier TGS en juillet 2019 basé sur la bibliothèque Lottie. Un fichier TGS se compose de texte [JSON](/fr/web/json/) qui est exporté à partir d'une animation dans Adobe After Effects. Le texte JSON exporté est compressé à l'aide de la compression gzip qui réduit la taille du fichier. Les informations JSON sur le fichier texte sont stockées dans un fichier texte qui devient la base des taux de compression élevés.

### Spécifications des autocollants TGS

Le format de fichier TGS impose certaines limitations à la création d'autocollants animés TGS. Un fichier animé TGS :

* La taille de l'autocollant/de la toile doit être de 512х512 pixels.
* Les objets autocollants ne doivent pas quitter la toile.
* La durée de l'animation ne doit pas dépasser 3 secondes.
* Toutes les animations doivent être en boucle.
* La taille de l'autocollant ne doit pas dépasser 64 Ko après le rendu dans Bodymovin.
* Toutes les animations doivent fonctionner à 60 images par seconde.

### Exemple de texte JSON TGS

Un exemple d'autocollant animé, une fois décompressé, contient le contenu textuel JSON suivant.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Références ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipédia](https://en.wikipedia.org/wiki/Gzip)

