{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier VPK - Format de fichier du package d'application PlayStation Vita",
  "description":"En savoir plus sur le format de fichier VPK et les API qui peuvent créer et ouvrir des fichiers VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Qu'est-ce qu'un fichier VPK ?

Un fichier avec l'extension .vpk est un fichier de package d'archive compressé utilisé pour installer des applications tierces sur la console de jeu Sony PlayStation Vita. Ces fichiers ne peuvent être installés que sur jailbreak Vita PlayStation par HENkaku qui a permis à la PS Vita et à la PSTV d'utiliser du contenu personnalisé créé par l'utilisateur. Un fichier d'archive VPK contient tout le contenu qui compose le jeu, y compris les images telles que les fichiers [PNG](/fr/image/png/), les fichiers de configuration tels que [.bin](/fr/disc-and-media/bin/) et toutes les configurations au format de fichier [XML](/fr/web/xml/).

## Format de fichier VPK

Les fichiers VPK sont enregistrés sur le disque en tant qu'archives standard compressées [ZIP](/fr/compression/zip/). Ceux-ci peuvent contenir plusieurs dossiers et autres fichiers associés pour les applications tierces à installer sur Vita Gaming Console. Pour afficher le contenu du fichier de package VPK, renommez son extension de .vpu en .zip et extrayez le contenu à l'aide d'utilitaires de décompression standard tels que WinZip ou WinRAR.

Valvesoftware dispose d'informations détaillées sur le [format de fichier VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) qui peuvent être référencées du point de vue du développeur.

## Comment installer les fichiers VPK ?

Les fichiers VPK peuvent être installés à partir de l'utilitaire de ligne de commande VPK.exe. Sur le système d'exploitation Windows, les fichiers peuvent être déposés sur le fichier vpk.exe qui renvoie un \*.vpk contenant tous les fichiers empaquetés. Alternativement, l'outil de ligne de commande peut être utilisé comme suit.

### Créer un VPK et ajouter des fichiers

```
vpk <dirname>
```

### Extraire les fichiers VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Lecteur VPK

* [Visionneuse VRF VPK] (https://github.com/SteamDatabase/ValveResourceFormat)

## Références

* [Format de fichier VPK] (https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [Fichiers VPK] (https://developer.valvesoftware.com/wiki/VPK)

