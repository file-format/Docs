{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","fichier", "format", "type de fichier", "extension","qu'est-ce qu'un fichier ASE ?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier ASE et les API qui peuvent ouvrir et créer des fichiers ASE.",
  "title" :"ASE - Fichier d'exportation de scène Autodesk ASCII",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Qu'est-ce qu'un fichier ASE ?

Un fichier avec une extension .ase est un format de fichier d'exportation de scène Autodesk ASCII qui est une représentation ASCII d'une scène, contenant des informations 2D ou 3D lors de l'exportation de données de scène à l'aide d'Autodesk. Autodesk propose des options permettant d'inclure des composants de scène lors de l'exportation de données de scène. Vous pouvez inclure la définition du maillage avec les informations sur les sommets et les faces, la description du matériau, les données d'animation de transformation pour les objets, la définition complète du maillage de toutes les n images, les données d'animation pour les caméras et les lumières et les paramètres de joint IK.

## Format de fichier ASE - Plus d'informations

Les fichiers ASE sont des fichiers texte stockés au format ASCII qui peuvent être ouverts dans n'importe quel éditeur de texte. Un fichier ASE peut contenir les types d'informations suivants fournis par Autodesk.

### Options de sortie

* `Mesh Definition` - Exporte la définition de chaque maillage, y compris les informations de sommet et de face pour les objets géométriques. De plus, l'activation de cette option active les éléments de la zone de groupe Options de maillage, décrites ci-dessous.
* `Matériaux` - Inclut la description du matériau. Si un matériau n'est pas affecté à un objet, sa couleur filaire est exportée. Tous les niveaux d'une arborescence de matériaux sont inclus, ce qui peut produire beaucoup de texte.
* `Transform Animation Keys` - Inclut les données d'animation de transformation pour les objets. Si l'objet est une caméra cible ou un projecteur, cela inclura les données d'animation cible.
* `Animated Mesh` - Exporte une définition complète du maillage de toutes les n images. La fréquence est spécifiée par la molette de sortie du contrôleur, décrite ci-dessous. Chaque bloc contient les mêmes informations spécifiées dans la zone de groupe Options de maillage, décrite ci-dessous. L'activation de cette option peut entraîner la création d'un fichier volumineux, même pour les petites scènes.
* `Animated Camera/Light Settings` - Exporte les données d'animation pour les caméras et les lumières, telles que la couleur, l'intensité, l'atténuation, le biais de la carte, etc. Génère un bloc toutes les n images, comme spécifié par la flèche de sortie du contrôleur.
* `Joints cinématiques inverses` - Exporte les paramètres de joint IK dans la branche Hiérarchie.

### Types d'objets

Les éléments ici vous permettent de spécifier la catégorie d'objet que vous souhaitez inclure dans la sortie. Vous pouvez inclure des objets géométriques, des formes, des caméras, des lumières et des objets auxiliaires.

* Géométrique
* Formes
* Appareils photo
* Lumières
* Aides

### Options de maillage

* `Mesh Normals` - Exporte les normales de face et de sommet. La normale de la face est répertoriée en premier, suivie des normales des trois sommets supportant la face. L'activation de cette option donne un fichier beaucoup plus volumineux.
* "Coordonnées de mappage" - Exporte une liste de sommets et de faces de mappage, conformément aux structures TVert et TVFace décrites dans le kit de développement logiciel 3ds Max. Si un objet utilise le mappage de visages, une liste de mappages de visages est exportée contenant les coordonnées UVW pour chaque visage.
* `Vertex Colors` - Exporte les couleurs des sommets.

### Sortie du contrôleur

* `Utiliser les clés` - Exporte les valeurs des clés. Si le contrôleur n'utilise pas de clés, la méthode Force Sample est utilisée. Dans le cas des contrôleurs de transformation, l'option Utiliser les clés ne fonctionne que si tous les contrôleurs de transformation sont linéaires/TCB ou Bézier. Si l'une des pistes de transformation utilise un type de contrôleur différent, la méthode Forcer l'échantillonnage est utilisée pour toutes les pistes de transformation.
* `Force Samples` - Échantillonne les valeurs du contrôleur en fonction de la fréquence spécifiée dans les Frames per Sample Controller.

## Références

* [Autodesk - Exportation vers ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

