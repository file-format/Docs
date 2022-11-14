{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Format de fichier", "Ouvrir", "Lire", "Créer", "CAO" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier HPGL et les API qui peuvent créer et ouvrir des fichiers HPGL.",
  "title" :"Format de fichier HPGL - Apprenez des experts en format de fichier !",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Qu'est-ce qu'un fichier HPGL ?

Un fichier HPGFL (Hewlett-Packard Graphics Language) contient un jeu d'instructions pour le contrôle du traceur développé par HP. Les traceurs HP utilisent ce fichier pour dessiner et imprimer du contenu vectoriel et raster sur le papier.

### Commande HPGL

Une commande HPGL comprend les éléments suivants.
* Une section de commande de l'alphabet de deux caractères
* Une section de paramètres
* Section de terminaison

Chaque paramètre du fichier doit être séparé par un séparateur en cas de paramètres multiples.

### Exemple de commande HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Système de coordonnées

Les systèmes de coordonnées comprennent des indicateurs de mesure bidimensionnels pour localiser n'importe quel emplacement spécifique. Le HPGL utilise à la fois les coordonnées du traceur et le système de coordonnées de l'utilisateur à cette fin.

#### Système de coordonnées du traceur

Ce système de coordonnées est utilisé pour tracer des dessins en fonction du mouvement du traceur. Une unité XY typique du mouvement minimal du traceur est de 0,025 mm. La gamme possible de dessins change avec les types de traceurs.

#### Système de coordonnées utilisateur

Le système de coordonnées spécifié par l'utilisateur peut être configuré à l'aide de l'échelle et de l'origine. Celles-ci sont converties en coordonnées de traceur à l'aide de la commande IP et de la commande SC. Les coordonnées du système de traceur sont utilisées par défaut si cette conversion n'est pas effectuée.

## Format de fichier HPGL
Les fichiers HPGL sont au format ASCII (fichier texte) et commencent par quelques commandes de configuration. Cela définit certains paramètres pour le traceur pour le traçage. Un fichier HPGL typique se présente comme suit.

|Commande|Signification
---|---|
|IN;|initialiser, démarrer une tâche de traçage|
|IP;|régler les points de mise à l'échelle (P1 et P2) à leurs positions par défaut|
|SP1;|sélectionner la plume 1|
|PU0,0;|levez le stylo et déplacez-vous au point de départ pour l'action suivante|
|PD100,0,100,100,0,100,0,0;|posez le stylet vers le bas et déplacez-vous aux emplacements suivants (dessinez un cadre autour de la page)|
|PU50,50;|Stylo vers le haut et déplacement vers les coordonnées X,Y 50,50|
|CI25;|dessiner un cercle de rayon 25|
|SS;|sélectionnez le jeu de caractères standard|
|DT*,1;|définissez le délimiteur de texte sur l'astérisque, et ne les imprimez pas (le 1, signifiant "vrai")|
|PU20,80;|levez le stylo et déplacez-vous à 20,80|
|LBHello World*;|dessine une étiquette|

## Références
* [HPGL par Wikipédia](https://en.wikipedia.org/wiki/HP-GL)
* [Guide de référence HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

