{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier VPK Unreal Static Meshes et les API qui peuvent créer et ouvrir des fichiers VPK.",
  "title" :"Fichier VPK - Fichier de maillages statiques irréels",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Qu'est-ce qu'un fichier VPK ?

Un fichier .vpk est un format de fichier utilisé par **Source Engine**, un moteur de jeu développé par Valve Corporation. Les fichiers VPK sont utilisés pour emballer le contenu du jeu, comme les modèles, les textures et les sons, et sont couramment utilisés dans des jeux comme Team Fortress 2, Left 4 Dead et Counter-Strike : Global Offensive. Les fichiers peuvent être ouverts et extraits à l'aide de divers outils, tels que GCFScape et VPK Tool.

## Format de fichier VPK - Plus d'informations

Les fichiers VPK sont stockés sur le disque sous forme de fichiers binaires. Un seul fichier vpk peut faire partie d'un package VPK ou peut agir comme un fichier VPK brut indépendant. Les informations pouvant être stockées dans un fichier VPK incluent des cartes, des matériaux, du contenu de jeu et des scènes de chorégraphie.

### Comment créer un fichier VPK ?

Il existe plusieurs façons de créer un fichier .vpk, selon les outils disponibles.

1. `Utilisation de l'outil VPK :` Il s'agit d'un outil de ligne de commande qui peut être utilisé pour créer et extraire des fichiers VPK. Un fichier VPK peut être créé à l'aide de la commande suivante :
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Cela créera un fichier VPK à partir du répertoire spécifié et l'enregistrera en tant que fichier de sortie spécifié.

1. "Utilisation de l'éditeur Hammer :" L'éditeur Hammer est un outil inclus avec le SDK Source qui peut être utilisé pour créer et modifier des niveaux pour les jeux qui utilisent le moteur Source. Il inclut également la possibilité de créer des fichiers VPK, en cliquant avec le bouton droit sur un dossier dans l'onglet "Système de fichiers" et en sélectionnant "Créer VPK"

1. "Utilisation du créateur VPK de Valve :" Il s'agit d'un outil développé par Valve qui est utilisé pour emballer et distribuer le contenu du jeu. Cet outil peut être utilisé pour créer des fichiers VPK et c'est aussi l'outil officiel pour créer des fichiers VPK.

## Références

* [Logiciel de vanne](https://www.valvesoftware.com/en/)
* [Ressources du développeur VPK](https://developer.valvesoftware.com/wiki/GCF)

