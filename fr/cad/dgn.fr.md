{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Fichier", "Formater", "Ouvrir", "Lire", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - Format de fichier de conception CAO MicroStation",
  "description" :"En savoir plus sur le format de fichier DGN et les API qui peuvent créer et ouvrir des fichiers DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Qu'est-ce qu'un fichier DGN ?

Un fichier avec une extension .dgn (Design) est un fichier de dessin créé et pris en charge par des applications de CAO telles que MicroStation et Intergraph Interactive Graphics Design System. Il est utilisé pour créer et enregistrer des conceptions pour des projets de construction tels que des autoroutes, des ponts et des bâtiments. Le format est similaire au format de fichier [DWG](/fr/cad/dwg/) d'Autodesk et est considéré comme son concurrent. Les fichiers DNG peuvent être enregistrés au format de fichier standard Intergraph ou V8 DGN. DGN peut être converti en plusieurs autres formats tels que DWG, [BMP](/fr/image/bmp/), [JPEG](/fr/image/jpeg/), [PDF](/fr/pdf/), [GIF](/fr/image/ gif/) et autres. Il peut être ouvert avec Autodesk AutoCAD, Bentley View et Bentley Systems MicroStation en plus d'autres applications logicielles telles que les versions Corel PaintShop Photo Pro et IMSI TurboCAD Deluxe.

## Format de fichier DGN V8

Un fichier DGN MicroStation V8 est composé d'un ou plusieurs modèles. Un modèle est un conteneur d'éléments. Le DGN V8 supprime toutes les contraintes basées sur le format de fichier qui étaient présentes dans les versions précédentes de MicroStation. Voici une liste des améliorations apportées au format de fichier DGN.

* La limite du nombre de niveaux dans un fichier DGN a été supprimée, et chaque niveau est nommé et stocké en tant qu'élément.
* La taille physique maximale du fichier DGN n'a aucune limitation et n'est limitée que par le système d'exploitation (comme la limite NT est de 4 Go)
* La taille maximale d'un seul élément est de 128 Ko.
* Il n'y a pas de limite à la taille maximale d'une cellule.
* Les noms de cellule sont limités à environ 500 caractères.
* Il n'y a pas de limite au nombre de références pouvant être jointes à un fichier DGN.
* Une ligne brisée, une forme ou une courbe de points peut avoir jusqu'à 5 000 sommets.
* Il n'y a pas de limite au nombre de composants dans une chaîne complexe ou une forme complexe.
* Il n'y a pas de limite au nombre de groupes graphiques dans un fichier DGN.
* La clôture est parallèle à la vue dans laquelle elle est placée.
* Une seule ligne de texte peut contenir 65 535 caractères.
* Il n'y a pas de limite à la taille maximale d'un nœud de texte.
* Il n'y a pas de limite au nombre de nœuds de texte dans un fichier DGN.
* Chaque élément possède un identifiant 64 bits unique qui ne change pas tout au long du cycle de vie de l'élément.
* Chaque élément a un horodatage qui indique l'heure de la modification la plus récente.

## Références

* [DNG - Par Wikipédia](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [Format de fichier DGN MicroStation V8] (https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

