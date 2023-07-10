{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "fichier", "extension", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur les fichiers GLTF et les API qui peuvent créer et ouvrir des fichiers GLTF.",
  "title" :"GLTF - Format de fichier de transmission GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier GLTF ?

glTF (GL Transmission Format) est un format de fichier 3D qui stocke les informations du modèle 3D au format JSON. L'utilisation de JSON minimise à la fois la taille des actifs 3D et le traitement d'exécution nécessaire pour décompresser et utiliser ces actifs. Il a été adopté pour la transmission et le chargement efficaces de scènes et de modèles 3D par des applications. glTF a été développé par le groupe de travail sur les formats 3D du groupe Khronos et est également décrit comme [JPEG](/fr/image/jpeg/) de 3D par ses créateurs.

Le format de fichier GLTF définit un format de publication extensible et commun pour les outils et services de contenu 3D qui rationalise les flux de travail de création et permet une utilisation interopérable du contenu dans l'industrie. L'intention derrière la création du format de fichier glTF était de définir un format de publication commun et extensible pour les outils et services de contenu 3D qui devrait rationaliser les flux de travail de création et permettre une utilisation interopérable du contenu dans l'industrie. Il minimise le traitement d'exécution par les applications utilisant WebGL et d'autres API.

## Bref historique du fichier GLTF

Les premières spécifications pour le format de fichier glTF 1.0 ont été annoncées en octobre 2015. Il s'agissait d'une série d'efforts qui avaient commencé en mars 2012 par Khronos. Le but de ces efforts était d'évaluer les opportunités autour de la traction WebGL. En conséquence, la première démo du format glTF, basée sur le format JSON, a été présentée lors de la rencontre WebGl en 2012. Le format a été adopté par plusieurs sociétés de temps à autre, notamment Cesium, 3D Tiles, Oculus, Microsoft, Archilogic et d'autres.

glTF 2.0 a été publié le 5 juin 2017 lors de la conférence Web3D 2017. Il existe une longue liste d'entreprises qui ont adopté le format de fichier glTF par la suite.

## Format de fichier GLTF

Les spécifications de format de fichier pour glTF 2.0 sont disponibles [en ligne](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) pour référence et doivent être consultées dans toute implémentation liée à la lecture/écriture pour la prise en charge de format de fichier glTF.

glTF définit les actifs comme des fichiers JSON avec des données externes de prise en charge. Il représente des modèles 3D à l'aide de :

* Description complète de la scène contenue dans un fichier .glTF au format JSON qui comprend des informations sur la hiérarchie des nœuds, les matériaux, les caméras, ainsi que des informations de descripteur pour les maillages, les animations et d'autres constructions
* Fichiers binaires (.bin) contenant des données de géométrie et d'animation, ainsi que d'autres données basées sur un tampon
* Fichiers image ([.jpg](/fr/image/jpeg/), [.png](/fr/image/png/)) pour les textures

Tous les actifs externes tels que les images sont stockés dans des fichiers externes référencés via URI. Ces URI sont stockés à côté du conteneur GLB ou intégrés directement dans le JSON à l'aide d'URI de données. Chaque glTF valide doit spécifier sa version.

glTF a été conçu pour obtenir une petite taille de fichier, un chargement rapide, une représentation complète de la scène 3D et une extensibilité. Ces objectifs de conception uniques sont les principales raisons de la popularité du format de fichier glTF dans le domaine 3D. Voici les types mime pris en charge par le format de fichier glTF pour différents types de fichiers :

* Les fichiers .gltf utilisent model/gltf+json
* Les fichiers .bin utilisent application/octet-stream
* Les fichiers de texture utilisent le type officiel image/* basé sur le format d'image spécifique. Pour la compatibilité avec les navigateurs Web modernes, les formats d'image suivants sont pris en charge : image/jpeg, image/png.

### Encodage JSON

glTF impose les restrictions supplémentaires suivantes sur le format de fichier JSON

Pour simplifier l'implémentation côté client, glTF a des restrictions supplémentaires sur le format et l'encodage JSON.

1. JSON doit utiliser l'encodage UTF-8 sans BOM.
1. Toutes les chaînes définies dans cette spécification (noms de propriétés, énumérations) utilisent uniquement le jeu de caractères ASCII et doivent être écrites en texte brut, par exemple, "buffer" au lieu de `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Les noms (clés) dans les objets JSON doivent être uniques, c'est-à-dire que les clés en double ne sont pas autorisées.

### URI

Les tampons et les ressources d'image sont référencés via des URI. Les deux types d'URI suivants doivent être pris en charge par les clients.

** URI de données : ** Les URI de données sont tels que définis par la RFC 2397 et sont utilisés par glTF pour intégrer des ressources dans le JSON.

**Chemins d'URI relatifs :** ou path-noscheme tel que défini par la RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — sans schéma, autorité ou paramètres. Les caractères réservés doivent être codés en pourcentage, conformément à RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Références ##

* [Spécifications glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Format de fichier glTF - Par Wikipedia](https://en.wikipedia.org/wiki/GlTF)

