{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Fichier GCODE - Qu'est-ce qu'un fichier .gcode et comment l'ouvrir ?",
   "description":"Découvrez le format de fichier GCODE et les API permettant de créer et d'ouvrir des fichiers GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-fr",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Qu'est-ce qu'un fichier GCODE ?

Un **fichier GCODE** est un fichier texte brut qui contient des instructions pour contrôler les machines-outils informatisées et les imprimantes 3D ; Le G-code, ou « Code géométrique », est un langage utilisé pour contrôler les mouvements et les actions des machines **CNC (Computer Numerical Control)** ; Les machines CNC comprennent les fraiseuses, les tours, les routeurs et les imprimantes 3D.

Les commandes G-code sont écrites dans une syntaxe spécifique composée généralement de lettres et de chiffres ; chaque commande demande à la machine d'effectuer une action spécifique telle que déplacer l'outil vers une position particulière, changer d'outil ou ajuster la vitesse.

Le G-code est souvent généré par le logiciel **CAM (Computer-Aided Manufacturing)** ; Le logiciel de FAO prend un modèle 3D ou une conception 2D et génère les parcours d'outils et les instructions G-code correspondants ; le fichier G-code est ensuite chargé dans une machine CNC ou une imprimante 3D pour exécution.

Les fichiers G-code ont généralement l'extension de fichier « .nc » ou « .gcode », par exemple « program.nc » ou « print.gcode ».

## Structure du fichier GCODE :

Les fichiers GCODE sont des fichiers texte brut dont chaque ligne contient une commande spécifique ; ces commandes vont du contrôle du mouvement de la machine au réglage de la température, de la vitesse et d'autres paramètres cruciaux pour la fabrication d'un objet.

La syntaxe de GCODE implique une combinaison de lettres et de chiffres ; chacun représentant une action ou un paramètre distinct ; les commandes courantes incluent G0 et G1 pour le mouvement, M3 et M5 pour le contrôle de la broche, et S et F pour les réglages de la vitesse et de l'avance respectivement.

## Génération GCODE :

Les logiciels de découpage tels que **Simplify3D** et **Slic3r** traduisent les dessins de conception assistée par ordinateur (CAO) en GCODE ; Un logiciel de CAO est utilisé pour créer des modèles 3D, qui sont ensuite exportés dans des formats comme STL ; le logiciel de découpage prend ces modèles et génère un fichier GCODE spécifiant des détails tels que la hauteur de la couche, la vitesse d'impression et les paramètres de température.

## Exemple de GCODE

Voici un exemple simple de G-code pour déplacer une machine CNC :

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Comment ouvrir un fichier GCODE ?

Pour ouvrir un fichier G-code vous pouvez utiliser différents types de logiciels en fonction de vos besoins.

Si vous avez généré du G-code pour une imprimante 3D ; vous pouvez l'ouvrir à l'aide du logiciel fourni avec votre imprimante 3D ou d'un logiciel de découpage dédié ; les exemples incluent **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** ou **Repetier-Host** ; ces programmes ont souvent une interface conviviale qui vous permet de charger et de visualiser le G-code.

Les fichiers GCODE sont du texte brut, vous pouvez donc les ouvrir avec n'importe quel éditeur de texte ; les éditeurs de texte courants incluent **Notepad (sous Windows)**, **TextEdit (sous macOS)** ou **Gedit (sous Linux)** ; **cliquez simplement avec le bouton droit** sur le fichier G-code, choisissez **Ouvrir avec** et sélectionnez un éditeur de texte.

