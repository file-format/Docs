{
  "date" : "2020-03-16",
  "keywords" :[ "Fichier PAT", "Format", "CAO" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier PAT et les API qui peuvent créer et ouvrir des fichiers PAT.",
  "title" :"Format de fichier PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Qu'est-ce qu'un fichier PAT ?

Un fichier avec l'extension .pat est un fichier CAO utilisé par le logiciel AutoCAD. Les applications qui peuvent ouvrir les fichiers PAT utilisent le motif de hachures stocké dans ces fichiers pour obtenir des informations sur la texture/le remplissage d'une zone. Les motifs contenus donnent des informations sur l'apparence du matériau aux objets dessinés. Les fichiers PAT peuvent être ouverts dans des applications telles qu'Autodesk AutoCAD, CorelDRAW Graphics Suite et Ketron Software. Les fichiers PAT peuvent être convertis en différents formats d'image tels que JPG, PNG, BMP, etc.

## Format de fichier PAT

Les fichiers PAT sont écrits au format texte brut et peuvent être ouverts dans n'importe quel éditeur de texte. Les motifs de hachures de ces fichiers sont vectoriels et suivent la syntaxe décrite dans la documentation AutoCAD.

Tous les motifs commencent au point 0,0, le motif est calculé pour couvrir la limite des hachures.

### Définition du motif

Toutes les définitions de modèle se composent des champs suivants :
* Un '\*' de tête
* Un nom - Le nom ne peut pas contenir d'espaces, de signes de ponctuation, de parenthèses ou de barres obliques.
* Une description

Le format standard des motifs de hachures est `<\*><name> <, description>`. Le nom et la description sont séparés par une virgule et les descriptions ne peuvent pas dépasser la longueur de la ligne de quatre-vingts caractères. Les motifs de hachures sont définis après ces informations.

### Exemples de motifs de hachures
Voici un exemple de motif carré
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Un autre exemple montrant un motif en parallélogramme est le suivant.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Références ##

* [Modèles de hachage par Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

