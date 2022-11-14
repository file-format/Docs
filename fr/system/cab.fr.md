{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extension", "fichier", "format", "système", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Fichier Cabinet Windows",
  "description":"En savoir plus sur le format de fichier CAB et les API qui peuvent créer et ouvrir des fichiers CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Qu'est-ce qu'un fichier CAB ? ##

Un fichier avec une extension .cab appartient à un fichier cabinet Windows qui appartient à la catégorie des fichiers système. Il s'agit d'un fichier enregistré au format de fichier d'archive dans les versions de Microsoft Windows prenant en charge les algorithmes de données compressées, tels que [LZX](/fr/compression/lzx/), Quantum et [ZIP](/fr/compression/zip/ ). Le fichier est d'une utilisation vitale lorsqu'un utilisateur ou un développeur souhaite contenir et partager des données et des fichiers d'installation de logiciels. Les fonctionnalités de compression de données sans perte et la certification numérique incluses dans ces fichiers rendent ce fichier parfait pour stocker et partager de tels fichiers. Il prend en charge différents installateurs Microsoft tels que Device Installer, SetUp API et AdvPak.

## Bref historique ##

Le fichier CAB est un type de fichier de compression de données développé par Microsoft. Il s'appelait initialement "Diamond", mais il est ensuite devenu populaire sous le nom de fichier CAB, abréviation du mot "Cabinet".

## Spécification technique ##

Un fichier CAB peut généralement contenir jusqu'à un maximum de 65535 dossiers, qui peuvent, à leur tour, contenir un maximum de 65536 fichiers chacun. Le mécanisme de stockage de fichiers CAB est économe en temps et en espace car il enregistre chaque dossier sous forme de bloc compressé au lieu de compresser et de stocker chaque fichier séparément. Les dossiers vides ne peuvent pas être stockés dans les dossiers d'archive CAB. Le fichier CAB a d'abord été développé par Microsoft et est utilisé dans divers programmes d'installation, tels que InstallShield avec un format légèrement différent. Les fichiers CAB sont généralement connectés à des programmes auto-extractibles. Les fichiers Microsoft CAB sont facilement reconnaissables grâce à leur marqueur unique qui aide à identifier le format. Le marqueur unique pour tous les fichiers Microsoft CAB est un préfixe de quatre mots, MSCF. En voyant ce code, un utilisateur peut facilement distinguer un fichier Microsoft CAB d'autres fichiers et l'utiliser en conséquence dans des compresseurs ou des versions. Les fichiers peuvent être compressés avec plus de données d'installations logicielles, ou les données actuelles peuvent être décompressées à l'aide du bon logiciel.


## CAB Exemple ##

L'exemple suivant illustre la relation entre les fichiers et les dossiers dans une structure de fichiers CAB :

{{< figure src="../cab.png" alt="Format de fichier CAB" >}}

## Référence ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
