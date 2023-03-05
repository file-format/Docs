
{
  "date" : "2023-01-05",
  "keywords" :[ "fichier pov", "format de fichier pov", "qu'est-ce qu'un fichier pov", "fichier", "exemple pov", "extension de fichier pov","extension", "format" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier POV et les API qui peuvent ouvrir et créer des fichiers POV.",
  "title" :"POV - Persistance du fichier de vision",
  "linktitle" : "POV",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2023-01-05"
}

## Qu'est-ce qu'un fichier POV ?

Un fichier POV est un fichier texte brut qui contient des instructions pour le logiciel de traçage de rayons POV-Ray. Ces instructions sont écrites dans un langage de script spécial propre à POV-Ray. Il spécifie la scène à rendre, y compris les objets 3D, les matériaux, l'éclairage et d'autres propriétés qui définissent l'apparence de la scène. Les fichiers POV utilisent un langage de script spécial spécifique à POV-Ray et peuvent être utilisés pour créer des scènes 3D complexes et détaillées. L'extension de fichier d'un fichier POV est généralement ".pov" ou ".povray". Lorsque vous ouvrez un fichier POV dans POV-Ray, le logiciel lit les instructions du fichier et les utilise pour générer une image rendue de la scène.

Les fichiers .pov sont souvent utilisés par les artistes et les concepteurs pour créer des graphiques et des animations 3D pour une variété d'applications, notamment le cinéma, la télévision, les jeux vidéo et les supports marketing.

## Format de fichier PDV

Le fichier **.pov** commence généralement par une série d'instructions **#include**, qui sont utilisées pour inclure des bibliothèques de couleurs, de textures et d'autres ressources prédéfinies pouvant être utilisées dans la scène. Ensuite, le fichier définit les objets, les matériaux et les autres propriétés de la scène à l'aide d'une série de blocs. Il existe de nombreux autres types d'objets, de matériaux et d'autres propriétés que vous pouvez spécifier dans un fichier .pov, et vous pouvez utiliser des boucles et des instructions conditionnelles pour créer des scènes plus complexes et détaillées.

## Applications logicielles pour POV

Le format de fichier .pov est utilisé par le logiciel de traçage de rayons POV-Ray, de sorte que l'application principale pour ouvrir les fichiers .pov est le logiciel POV-Ray lui-même. Vous pouvez télécharger la dernière version de POV-Ray sur le site officiel à l'adresse https://www.povray.org/.

En plus de POV-Ray, il existe un certain nombre d'autres applications qui peuvent ouvrir et modifier des fichiers .pov, notamment :

- BRL-CAD : Un logiciel de modélisation 3D open-source qui peut importer et exporter des fichiers .pov
- MeshLab : Un logiciel de traitement de maillage 3D qui peut importer et exporter des fichiers .pov
- Blender : un logiciel graphique 3D open source populaire qui peut importer et exporter des fichiers .pov

Il peut y avoir d'autres applications logicielles qui peuvent également ouvrir les fichiers .pov, vous pouvez donc essayer d'utiliser un visualiseur de fichiers ou un outil de conversion si vous ne parvenez pas à ouvrir un fichier .pov avec les applications ci-dessus.

## Exemple de PDV

Par exemple, voici un exemple de fichier .pov qui définit une scène avec un seul cylindre bleu :

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Dans cet exemple, le bloc caméra spécifie la position et l'orientation de la caméra dans la scène, le bloc "light_source" déclare une source de lumière et spécifie sa position et sa couleur, et le bloc "cylinder" déclare un objet cylindre et spécifie ses extrémités, le rayon et les propriétés des matériaux. Lorsque vous ouvrez ce fichier .pov dans le logiciel POV-Ray, il rendra l'image d'un seul cylindre bleu.

## Références
* [POV-Ray - Wikipédia](https://en.wikipedia.org/wiki/POV-Ray)
* [Site Web de documentation POV-Ray](http://www.povray.org/documentation/)

