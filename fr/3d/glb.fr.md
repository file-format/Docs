{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","fichier", "format", "type de fichier", "extension","qu'est-ce qu'un fichier GLB ?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"En savoir plus sur le format de fichier GLB et les API qui peuvent ouvrir et créer des fichiers GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Qu'est-ce qu'un fichier GLB ?

GLB est la représentation au format de fichier binaire des modèles 3D enregistrés au format de transmission GL ([glTF](/fr/3d/gltf/)). Informations sur les modèles 3D tels que la hiérarchie des nœuds, les caméras, les matériaux, les animations et les maillages au format binaire. Ce format binaire stocke l'actif glTF (JSON, .bin et images) dans un blob binaire. Cela évite également le problème d'augmentation de la taille du fichier qui se produit en cas de glTF. Le format de fichier GLB se traduit par des tailles de fichier compactes, un chargement rapide, une représentation complète de la scène 3D et une extensibilité pour un développement ultérieur. Le format utilise model/gltf-binary comme type MIME.

## Format de fichier GLB - Plus d'informations

Les méthodes de diffusion de contenu utilisées par glTF entraînent un traitement supplémentaire pour décoder les données binaires encodées en base 64 et augmentent également la taille du fichier de 33 %. Ces méthodes de livraison, qui ont contribué à la formation du format de fichier GLB, incluent :

* glTF JSON pointe vers des données binaires externes (géométrie, images clés, skins) et des images.
* glTF JSON intègre des données binaires encodées en base64 et des images en ligne à l'aide d'URI de données.

GLB en tant que format de conteneur a été introduit en tant que format de fichier binaire pour la représentation de l'actif glTF dans un blob binaire afin d'éviter les problèmes causés par glTF. Le format de fichier GLB [spécifications](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) doit être référé pour toute implémentation de lecteur/graveur de celui-ci pour le développement d'applications .

## Structure du fichier GLB

Le format de fichier GLB est basé sur Little Endian et sa structure montre qu'il contient :

* Un préambule de 12 octets, intitulé l'en-tête.
* Un ou plusieurs morceaux contenant du contenu JSON et des données binaires.

#### En-tête GLB

L'en-tête du format de fichier GLB se compose de trois entrées de 4 octets :

* magie uint32 - la magie est égale à 0x46546C67. Il s'agit de la chaîne ASCII glTF et peut être utilisée pour identifier les données en tant que glTF binaire
* version uint32 - indique la version du format de conteneur glTF binaire
* longueur uin32 - la longueur totale du glTF binaire, y compris l'en-tête et tous les morceaux en octets

#### Morceaux

Chaque bloc d'un fichier GLB a la structure suivante :

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - longueur de chunkData en octets
* `chunkType` - indique indique le type de morceau
* `chunkData` - charge utile binaire du morceau

où les types de blocs sont :

|# |Type de segment|ASCII|Description|Occurrences
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Contenu JSON structuré|1
|2.|0x004E4942|BIN|Tampon binaire|0 ou 1

Le début et la fin de chaque bloc doivent être alignés sur une limite de 4 octets et le rembourrage doit être utilisé à cette fin.

##### Contenu JSON structuré

Cela devrait être le tout premier morceau de l'actif glTF binaire et permet à l'implémentation de récupérer progressivement les ressources des morceaux suivants. Cela offre également la possibilité de lire uniquement un sous-ensemble sélectionné de ressources à partir d'un actif glTF binaire, tel que le niveau de détail le plus grossier d'un maillage. Afin de répondre aux exigences d'alignement, ce bloc doit être complété par des caractères d'espacement de fin (0x20).

##### Tampon binaire #####

Ce bloc contient la charge utile binaire pour la géométrie, les images clés d'animation, les habillages et les images. Il doit s'agir du deuxième bloc de l'actif glTF binaire et doit être complété par des zéros à droite (0x00) pour satisfaire aux exigences d'alignement.

## Références ##

* [Spécifications du format de fichier GLB - Khronos](/fr/3D/GLTF/)

