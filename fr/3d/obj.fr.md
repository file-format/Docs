{
  "date" : "2019-10-11",
  "keywords" :[ "fichier obj", "format de fichier obj", "qu'est-ce qu'un fichier obj", "fichier", "exemple obj", "extension de fichier obj","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier OBJ",
  "description":"En savoir plus sur le format de fichier OBJ et les API qui peuvent ouvrir et créer des fichiers OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier OBJ ?

Les fichiers **OBJ** sont utilisés par l'application Advanced Visualizer de Wavefront pour définir et stocker les objets géométriques. La transmission en amont et en aval des données géométriques est rendue possible grâce aux fichiers OBJ. La géométrie polygonale comme les points, les lignes, les sommets de texture, les faces et la géométrie de forme libre (courbes et surfaces) sont prises en charge par le format OBJ. Ce format ne prend pas en charge l'animation ou les informations relatives à la lumière et à la position des scènes.

Un fichier OBJ est généralement un produit final du processus de modélisation 3D généré par une CAO (conception assistée par ordinateur). L'ordre par défaut pour stocker les sommets est dans le sens inverse des aiguilles d'une montre, évitant ainsi la déclaration explicite des normales de face. Bien que les fichiers OBJ déclarent des informations d'échelle dans une ligne de commentaire, aucune unité n'a été déclarée pour les coordonnées OBJ.

## Historique du format 3D OBJ

Wavefront Technologies a créé le format de fichier OBJ pour son application Advanced Visualizer afin de stocker des objets géométriques et des données 3D. Sa version 2.11 est remplacée par une version 3 nouvellement documentée. Le format de fichier est ouvert et a été implémenté par d'autres fournisseurs pour leur application graphique 3D. Wavefront Technologies a gardé ce format de fichier open source et neutre.

## Format de fichier OBJ

Dans les objets 3D, l'encodage de la géométrie de surface est un travail difficile que le format de fichier OBJ a très bien accompli. Ce format est assez polyvalent car il offre un certain nombre de choix pour encoder la géométrie de surface. Voici trois formats autorisés ayant leurs propres avantages et inconvénients :

### Tessellation avec des faces polygonales

Le format de fichier OBJ permet à l'utilisateur de tesseller une surface de modèle 3D à l'aide de formes géométriques simples ou complexes. Pour l'encodage de la géométrie de surface d'un modèle, un fichier stocke les sommets et la normale à chaque polygone. Bien que la tessellation augmente la grossièreté du modèle, il est néanmoins nécessaire de découvrir le juste équilibre entre la taille d'un fichier et sa qualité d'impression.

### Courbe de forme libre

Le format de fichier OBJ permet aux courbes de surface de forme libre définies par l'utilisateur de spécifier la géométrie de surface d'un modèle. Comme les courbes de forme libre sont plus complexes que les faces polygonales car, avec peu de paramètres mathématiques, les lignes courbes peuvent être mieux définies par des courbes de forme libre. Par conséquent, avec moins de données par rapport aux pavages polygonaux, les courbes de forme libre sont utilisées pour générer un codage de haute qualité de n'importe quel modèle 3D sans augmenter la taille du fichier.

### Surfaces de forme libre

Le format de fichier OBJ spécifie également le pavage de la géométrie de surface avec des patchs de surface de forme libre. Ce type de patchs de surface de forme libre (NURBS) est très approprié pour les surfaces sans dimensions radiales rigides comme le corps d'un camion, les ailes d'un hélicoptère ou la coque d'un bateau. L'utilisation de surfaces de forme libre est très avantageuse car elles sont plus précises pour conserver des tailles de fichiers plus petites avec une plus grande précision. Ces surfaces sont une partie essentielle de l'industrie aérospatiale et automobile où la faible précision est impitoyable.

Les mots-clés suivants sont organisés par type de données pour définir la géométrie de surface.


|Éléments|Instructions de corps de courbe/surface de forme libre|Attributs de courbe/surface de forme libre
---|---|---|
|p|Point|parm|Valeurs des paramètres|deg|Degré
|l|Ligne|trim|Boucle de découpage externe|bmat|Matrice de base
|f|Face|trou|Boucle de coupe intérieure|pas|Taille du pas
|curv|Courbe|scrv|Courbe spéciale|cstype|Type de courbe ou de surface
|curv2|Courbe 2D|sp|Point spécial|**Connectivité et groupement de surfaces**
|surf|Surface|end|Fin de l'instruction|con|connect
|**Attributs d'affichage/de rendu**|g|Nom du groupe
|bevel|Interpolation de biseau|shadow_obj|Shadow casting|s|Groupe de lissage
|lod|Niveau de détail|trace_obj|Ray tracing|mg|Groupe fusionné
|d_interp|Dissoudre l'interpolation|ctech|Technique d'approximation de courbe|o|Nom de l'objet
|c_interp|Interpolation de couleur|stech|Technique d'approximation de surface|
|usemtl|Nom du matériau|mtllib|Bibliothèque de matériaux|
|**Sommets géométriques**|
|v|Sommets géométriques|vn|Normales sommets|
|vt|Sommets de la texture|vp|Sommets de l'espace des paramètres|

### Couleur et Texture

Le fichier OBJ permet de stocker les informations de couleur et de texture dans un format de fichier associé appelé Material Template Library (MTL). Les modèles géométriques multicolores sont rendus en utilisant ces deux fichiers ensemble. Les fichiers MTL sont basés sur ASCII et facilitent le rendu informatique en décrivant les propriétés de réflexion de la lumière d'une surface à l'aide du modèle de réflexion de Phong. La norme a été adoptée par un grand nombre d'éditeurs de logiciels qui en profitent pour l'échange de matériaux. Le format MTL est légèrement obsolète car il ne prend pas en charge les dernières technologies telles que les cartes spéculaires et de parallaxe.

## Références

* [Fichier Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

