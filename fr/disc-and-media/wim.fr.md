{
  "date" : "2021-08-11",
  "keywords" :[ "fichier wim", "format de fichier wim", "qu'est-ce qu'un fichier wim", "fichier", "exemple wim", "extension de fichier wim","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier WIM et les API qui peuvent créer et ouvrir des fichiers WIM.",
  "title" :"WIM - Fichier de format d'imagerie Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Qu'est-ce qu'un fichier WIM ?
Les fichiers avec les extensions .wim ont été vus pour la première fois dans Windows Vista. Le WIM appartient à un format d'imagerie basé sur des fichiers qui a été généralement introduit dans Microsoft Windows Vista. Il permet de déployer une seule image disque sur différentes plates-formes informatiques. Les fichiers WIM sont utilisés pour gérer des fichiers tels que des mises à jour, des pilotes et des composants sans redémarrer l'image du système d'exploitation. Le fichier AQ WIM contient un ensemble de fichiers et de métadonnées associées très similaires aux autres formats de fichiers de disque.

## Formats de fichiers WIM
Le format de fichier WIM n'est pas comme les formats basés sur des secteurs tels que VHD ou IS, en fait c'est un fichier basé sur ce qui signifie que l'unité fondamentale d'information dans un WIM est un fichier. L'avantage fondamental d'être basé sur des fichiers est qu'un stockage d'instance unique d'un fichier référencé plusieurs fois dans l'arborescence du système de fichiers et l'indépendance matérielle. Cela réduit les frais généraux liés à l'ouverture et à la fermeture de divers fichiers individuellement, car les fichiers sont stockés dans un seul WIM. dossier. Les fichiers WIM peuvent stocker plusieurs images de disque, qui sont référencées soit par leur nom unique, soit par leur index numérique.
### Prise en charge des algorithmes de compression
WIM prend en charge les familles suivantes d'algorithmes de compression en vitesse descendante et en rapport ascendant :
-XPRESS
-LZX
- LZMS
- Solide-compression.
Les trois premières familles sont basées sur LZ77 tandis que la compression solide a été introduite avec LZMS dans WIMGAPI Windows 8 et DISM Windows 8.1.
### Outils pour le format de fichier WIM
Les outils suivants prennent généralement en charge le format de fichier WIM :

- **ImageX** : un outil de ligne de commande utilisé pour modifier, créer et déployer des images de disque Windows au format Windows Imaging. Avec le WIMGAPI pertinent, il est distribué dans le cadre du kit d'installation automatisée Windows gratuit. À partir de Windows Vista, le programme d'installation de Windows utilise l'API WAIK pour installer Windows.
- **DISM** : un outil introduit dans Windows 7 et Windows Server 2008 R2 qui peut effectuer des tâches liées au service sur une image d'installation Windows, qu'il s'agisse d'une image en ligne ou d'une image hors ligne dans un dossier ou un fichier WIM. cet outil était capable de monter et de démonter des images, d'ajouter un pilote de périphérique à une image hors ligne et d'interroger les pilotes de périphérique installés dans une image hors ligne.
 




## Références


* [Format d'imagerie Windows - par Wikipedia] (https://en.wikipedia.org/wiki/Windows_Imaging_Format)


