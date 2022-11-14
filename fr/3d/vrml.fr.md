{
  "date" : "2019-10-11",
  "keywords" :[ "fichier vrml", "format de fichier vrml", "qu'est-ce qu'un fichier vrml", "fichier", "exemple vrml", "extension de fichier vrml","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier VRML",
  "description":"En savoir plus sur le format de fichier VRML et les API qui peuvent ouvrir et créer des fichiers VRML.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier VRML ?
Le langage de modélisation de réalité virtuelle (VRML) est un format de fichier pour la représentation d'objets du monde interactifs [3D](/fr/3d/) sur le World Wide Web (www). Il trouve son utilisation dans la création de représentations tridimensionnelles de scènes complexes telles que des illustrations, des définitions et des présentations de réalité virtuelle. Le format a été remplacé par [X3D](/fr/3d/x3d/). De nombreuses applications de modélisation 3D peuvent enregistrer des objets et des scènes au format VRML.

## Format de fichier VRML

VRML est un format de fichier texte qui spécifie des informations telles que les sommets et les bords d'un polygone 3D ainsi que des informations telles que la couleur de la surface, les textures mappées UV, la brillance, la transparence, etc. Il a la capacité de représenter des objets statiques et animés en plus d'avoir des hyperliens vers d'autres médias tels que le son, les films et les images. Cela permet d'ouvrir des éléments hyperliens lorsque l'utilisateur clique sur ces objets.

Les fichiers TVRML dans la terminologie courante sont appelés "mondes" et ont l'extension .wrl. La nature textuelle de ces fichiers permet de réduire la taille du fichier en utilisant des formats de compression tels que gzip, ce qui les rend plus favorables pour un transfert rapide sur Internet. Les spécifications de format de fichier pour [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) servent de référence aux développeurs pour créer des applications compatibles pour lire/écrire ces fichiers.

## Critère de conception ##

L'objectif et la conception de VRML s'articulent autour des exigences suivantes.

* **Authorability** - Permet de développer des générateurs et des éditeurs d'applications, et d'importer des données à partir d'autres formats industriels
* **Exhaustivité** - Fournit toutes les informations nécessaires à la mise en œuvre et propose un ensemble complet de fonctionnalités pour une large acceptation par l'industrie
* **Composabilité** - La possibilité d'utiliser des éléments de VRML en combinaison et ainsi permettre la réutilisation.
* **Extensibilité** - La possibilité d'ajouter de nouveaux éléments.
* **Implémentation** -Capable d'implémentation sur une large gamme de systèmes.
* **Potentiel multi-utilisateurs** - Ne devrait pas empêcher la mise en œuvre d'environnements multi-utilisateurs.
* **Orthogonalité** - Les éléments de VRML doivent être indépendants les uns des autres, ou toute dépendance doit être structurée et bien définie.
* **Performances** - Les éléments doivent être conçus en mettant l'accent sur les performances interactives sur une variété de plates-formes informatiques.
* **Évolutivité** - Les éléments de VRML doivent être conçus pour des compositions infiniment grandes.
* **Pratique standard** - Seuls les éléments qui reflètent la pratique existante, qui sont nécessaires pour soutenir la pratique existante ou qui sont nécessaires pour soutenir les normes proposées doivent être normalisés.
* **Bien structuré** - Un élément doit avoir une interface bien définie et un objectif inconditionnel simplement énoncé. Les éléments polyvalents et les effets secondaires doivent être évités.

## Références ##

* [VRML - Par Wikipédia](https://en.wikipedia.org/wiki/VRML)
* [Spécifications du format de fichier VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)

