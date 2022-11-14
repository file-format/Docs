{
  "date" : "2019-10-11",
  "keywords" :[ "fichier qml", "format de fichier qml", "qu'est-ce qu'un fichier qml", "fichier", "exemple qml", "extension de fichier qml","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - Le format de fichier de style QGIS",
  "description":"En savoir plus sur le format de fichier QML et les API qui peuvent créer et ouvrir des fichiers QML.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Qu'est-ce qu'un fichier QML ?

Un fichier avec l'extension .qml est un fichier XML qui stocke les informations de style de couche pour les couches QGIS. QGIS est une application SIG multiplateforme open source utilisée pour afficher des données géospatiales avec la capacité d'organiser les données sous forme de couches. Les fichiers QML contiennent des informations utilisées par QGIS pour rendre les géométries d'entités, notamment les définitions de symboles, les tailles et les rotations, l'étiquetage, l'opacité, le mode de fusion, etc. Contrairement aux fichiers QLR, les fichiers QML contiennent toutes les informations de style en eux-mêmes. Les fichiers QML peuvent être ouverts dans n'importe quel éditeur de texte tel que Notepad++.

## Format de fichier QML

QLR, similaire à [QGS](/fr/gis/qgs/) et [QLR](/fr/gis/qlr/), est un fichier XML qui contient des informations de style pour les couches.

La figure ci-dessous montre les balises de niveau supérieur d'un fichier QML (avec uniquement renderer_v2 et sa balise de symbole développée).

{{< figure src="../qml.png" title="" >}}

## Références

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

