{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier CUBE - Fichier Cube Gaussien - Qu'est-ce que le fichier .cube et comment l'ouvrir?",
  "description" : "En savoir plus sur le fichier Cube gaussien et comment l'ouvrir.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-fr-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Qu'est-ce qu'un fichier CUBE ?

Le format de fichier CUBE, également connu sous le nom de fichier Gaussian Cube (.cube), est utilisé en chimie computationnelle pour stocker des données moléculaires, en particulier des informations sur la densité électronique résultant de calculs de chimie quantique. Ce format est généralement associé au **progiciel gaussien**, largement utilisé pour effectuer des calculs de structure électronique ab initio.

Les fichiers Gaussian Cube stockent des données tridimensionnelles, représentant généralement la densité électronique ou d'autres propriétés des molécules, obtenues grâce à des calculs de chimie quantique. Le fichier contient une section d'en-tête avec des métadonnées (telles que l'origine, le nombre de points de données le long de chaque axe et l'espacement), suivies d'une grille de valeurs numériques représentant la propriété d'intérêt (par exemple, la densité électronique) à chaque point de la grille dans l'espace.

Le fichier Gaussian Cube (.cube) est un fichier texte brut avec une structure spécifique. L'en-tête contient des informations sur le système moléculaire et la grille de données, et les valeurs des données sont disposées sous forme de grille tridimensionnelle. Les fichiers Gaussian Cube sont souvent utilisés pour visualiser les propriétés moléculaires à l'aide d'un logiciel de visualisation moléculaire. Des programmes tels que **VMD (Visual Molecular Dynamics)** ou **PyMOL** peuvent lire les fichiers Cube gaussien pour afficher les surfaces moléculaires, la densité électronique ou d'autres propriétés calculées.

## Exemple simplifié de fichier Cube Gaussien :

```
Exemple de fichier cube
Généré par Gaussien
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,00000000000000000E+00
  50 0,0000000000000000E+00 0,1000000000000000E+01 0,00000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (valeurs de données pour la densité électronique à chaque point de la grille)
```

## À propos de la Gaussienne

Gaussian est une suite d'applications logicielles pour la chimie quantique et la chimie computationnelle. L'objectif principal de Gaussian est les méthodes de chimie quantique ab initio, qui sont des approches très précises mais gourmandes en calcul pour étudier la structure électronique des molécules. Le logiciel est largement utilisé dans les milieux de la recherche et universitaires pour diverses applications, notamment la prévision des propriétés moléculaires, l'étude des mécanismes de réaction et l'exploration des structures moléculaires.

## À propos de NWChem

NWChem est un logiciel de chimie informatique open source conçu pour les simulations de chimie quantique haute performance. Il utilise des méthodes ab initio telles que Hartree-Fock et la théorie fonctionnelle de la densité, prend en charge le calcul parallèle pour des calculs efficaces sur les clusters et trouve des applications dans divers domaines scientifiques, notamment la chimie computationnelle, la biochimie et la science des matériaux. NWChem est connu pour sa polyvalence, permettant aux chercheurs d'étudier divers systèmes chimiques, et sa nature open source encourage les contributions et la personnalisation de la communauté.

## À propos de VMD

VMD, qui signifie Visual Molecular Dynamics, est un programme de visualisation moléculaire puissant et largement utilisé pour afficher, analyser et animer des trajectoires de dynamique moléculaire (MD), ainsi que des structures moléculaires statiques. Il est particulièrement populaire dans les domaines de la chimie computationnelle, de la biologie moléculaire et de la bioinformatique structurale. VMD excelle dans la visualisation des structures moléculaires, fournissant des rendus 3D de haute qualité de molécules et de complexes moléculaires. Il prend en charge une variété de formats de fichiers moléculaires.

## À propos de PyMOL

PyMOL est un système de visualisation moléculaire et un outil logiciel utilisé pour la visualisation tridimensionnelle des structures moléculaires. Il est particulièrement populaire dans les domaines de la biologie structurale, de la bioinformatique et de la chimie computationnelle. PyMOL fournit des rendus 3D de haute qualité de structures moléculaires, permettant aux utilisateurs de visualiser et d'explorer les formes, les surfaces et les interactions des macromolécules biologiques.

## Comment ouvrir le fichier CUBE?

Le fichier CUBE peut être ouvert et référencé à l’aide des programmes suivants.

- **NWChem** (gratuit) pour (Windows, MAC, Linux)

## Les références
* [Format de fichier cube gaussien](https://paulbourke.net/dataformats/cube/)
