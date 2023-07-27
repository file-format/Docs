{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier MK3D",
  "keywords" :[ "mk3d", "vidéo matroska", "format mkv", "3d stéréoscopique", "StereoMode", "vidéo", "fichier", "format" ],
  "description":"En savoir plus sur le format de fichier MK3D pour les vidéos 3D stéréoscopiques créées par Matroska et les API qui peuvent créer et ouvrir des fichiers MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Qu'est-ce qu'un fichier MK3D ? ##

Les fichiers MK3D appartiennent à la famille des formats vidéo Matroska. Ces fichiers sont en fait des vidéos **3D stéréoscopiques** créées à l'aide du format Matroska 3D. Le conteneur de fichiers MKV utilise la valeur d'un champ StereoMode pour définir le type de contenu vidéo 3D stéréoscopique. Une valeur StereoMode est également disponible pour afficher les anciennes vidéos 3D stéréo en séparant les couleurs cyan et rouge (AnaGlyph)

## Détails techniques ##
Les vidéos 3D peuvent être compressées des deux manières suivantes :

- Piste séparée pour chaque œil.
- Combinez chaque suivi oculaire en une seule piste.

Le conteneur de fichiers MKV prend en charge les deux.

Pour les vidéos à piste unique qui sont plus faciles avec le matériel 3D à l'intérieur, vous devez définir le champ **StereoMode** qui décide si les plans sont assemblés dans la piste combinée mono ou gauche droite. Vous pouvez utiliser l'une des valeurs de champ StereoMode suivantes :

|Valeur | Descriptif |
|---|---|
|0| mono|
|1| côte à côte (l'œil gauche est le premier) |
|2| haut-bas (l'œil droit est le premier) |
|3| haut-bas (l'œil gauche est le premier) |
|4| damier (la droite est la première) |
|5| damier (la gauche est la première) |
|6| rangée entrelacée (la droite est la première) |
|7| rangée entrelacée (la gauche est la première) |
|8| colonne entrelacée (la droite est la première) |
|9| colonne entrelacée (la gauche est la première) |
|10| anaglyphe (cyan/rouge)|
|11| côte à côte (l'œil droit est le premier) |
|12| anaglyphe (vert/magenta) |
|13| les deux yeux liés dans un bloc (l'œil gauche est le premier) (mode séquentiel de champ) |
|14| les deux yeux liés dans un bloc (l'œil droit est le premier) (mode séquentiel de champ) |

Pour les pistes multiples, le conteneur MKV doit décider de la fonctionnalité de chaque piste séparément. Le **TrackOperation** avec **TrackCombinePlanes** sont utilisés pour faire le travail.


## Références ##

- [Notes de spécification Matroska](https://www.matroska.org/technical/notes.html)
- [Prise en charge du conteneur de fichiers MKV pour la vidéo 3D stéréo et les fichiers MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

