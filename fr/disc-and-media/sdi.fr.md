{
  "date" : "2021-08-13",
  "keywords" :[ "fichier sdi", "format de fichier sdi", "qu'est-ce qu'un fichier sdi", "fichier", "exemple sdi", "extension de fichier sdi","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier SDI et les API qui peuvent créer et ouvrir des fichiers SDI.",
  "title" :"SDI - Fichier image de déploiement du système Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Qu'est-ce qu'un fichier SDI ?
Le fichier avec l'extension .sdi contient un blob de chargement, un blob de démarrage et un blob de partie ; couramment utilisé par Windows Embedded Studio pour créer des disques RAM ou des disques de démarrage pour le chargement et l'installation de Windows. Le SDI est l'abréviation de System Deployment Image. Le Windows Embedded Studio est un programme utilisé pour créer des images de disque pour Windows. En fait, ce programme contient le programme SDI File Manager et un outil de ligne de commande appelé ** sdimgr.exe **, les deux peuvent être utilisés pour déployer, créer et éditer des images SDI.

## Format de fichier SDI
Le format de fichier SDI est largement utilisé pour permettre l'utilisation d'un disque virtuel pour démarrer un système. Certaines versions de Microsoft Windows permettent le **démarrage RAM**, ce qui est important pour charger un fichier SDI en mémoire, puis démarrer à partir de celui-ci. Le format de fichier SDI s'active également pour le démarrage réseau en utilisant le PXE (Preboot Execution Environment). Il est également utilisé pour l'imagerie du disque dur.
### Sections de fichier SDI
Le fichier SDI lui-même peut être subdivisé dans les sections suivantes :
- **Boot BLOB** : contient le programme de démarrage réel, STARTROM.COM. Il s'agit d'un secteur analogue au secteur de démarrage d'un disque dur.
- **Load BLOB** : contient généralement NTLDR et est lancé par le BLOB de démarrage.
- **Partie BLOB** : elle contient le temps d'exécution réel du démarrage ; inclut également les fichiers boot.ini et ntdetect.com qui doivent se trouver dans le répertoire racine du runtime.
- **Disk BLOB** : il s'agit d'une image HDD plate commençant par un MBR. Il est utilisé pour l'imagerie du disque dur au lieu de démarrer. De plus, seuls les BLOB de disque peuvent être montés avec les utilitaires de Microsoft.


## Références

* [Image de déploiement du système - par Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


