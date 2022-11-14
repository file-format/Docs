{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier B3D ; utilisé dans les jeux blitz3d et les API qui peuvent ouvrir et créer des fichiers B3D.",
  "title" :"B3D - Fichier de modèle d'entité Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Qu'est-ce qu'un fichier B3D ?

Un fichier avec l'extension .b3d est un fichier de modèle utilisé par Blitz3D qui peut contenir des modèles de jeux vidéo pour les personnages, les bâtiments, le terrain et d'autres objets. Le Blitz3D est un langage de programmation utilisé pour créer des **jeux blitz3d**. Blitz3D est un langage de programmation puissant, flexible et facile à utiliser conçu dans le seul but d'écrire des jeux vidéo. Les développeurs peuvent créer des jeux 3D bourrés d'action, des puzzles 2D, des aventures, des RPGS, etc. en utilisant simplement Blitz3D.

Le Blitz3D est basé sur le langage de programmation BASIC ; qui est également facile à apprendre et à utiliser. Tous ces faits rendent Blitz idéal pour les débutants comme pour les programmeurs plus expérimentés. Bien que ses fonctionnalités soient considérées comme quelque peu désuètes par rapport à la plupart des moteurs 3D modernes, Blitz3D continue d'être utilisé par de nombreux programmeurs de jeux dans le monde entier.

## Bref historique de Blitz3D

Le Blitz3D a été essentiellement publié pour le système d'exploitation Microsoft Windows en septembre 2001, pour concurrencer d'autres langages de développement de jeux similaires. Blitz3D était une version améliorée du moteur 2D précédent BlitzBasic, qui étendait son jeu de commandes avec l'ajout d'une API pour un moteur 3D basé sur DirectX 7. Les utilisateurs de Blitz3D devraient également comparer BlitzMax, qui est un moteur plus récent de BlitzBasic. Le BlitzMax est une version complexe mais plus puissante de Blitz3D, qui prend en charge les langages de programmation orientés objet. Il s'agit d'une API graphique mise à jour pour mieux s'adapter aux caractères Unicode, OpenGL et exporter vers OSX et Linux au lieu de Windows uniquement.

## Exemple B3D
Un fichier b3d contenant 1 morceau TEXS, 1 morceau BRUS et 1 morceau NODE ressemblera à ceci :

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
Un maillage simple, non animé et non texturé ressemblera à ceci :

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## Références
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

