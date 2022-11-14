{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "fichier vdw", "format de fichier vdw", "type de fichier vdw", "fichier", "type", "qu'est-ce qu'un fichier vdw"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Format de fichier du service graphique Visio",
  "description":"En savoir plus sur le format de fichier VDW et les API qui peuvent créer et ouvrir des fichiers VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Qu'est-ce qu'un fichier VDW ?

VDW est le format de fichier Visio Graphics Service qui spécifie les flux et les stockages requis pour le rendu d'un dessin Web. Un dessin Web est une collection de pages de dessin, de formes, de polices, d'images, de connexions de données et d'informations de mise à jour de diagramme qui peuvent être rendues sous forme de dessin vectoriel ou raster. Les fichiers VDW peuvent également être ouverts dans Microsoft Visio, mais sont principalement enregistrés pour une utilisation sur le Web. Microsoft Visio offre la possibilité de convertir des fichiers Visio dans un certain nombre de formats de fichiers différents, notamment [PNG](/fr/Image/PNG/), [BMP](/fr/Image/BMP/), [PDF](/fr/pdf/) et autres.

## **VDW** Format de fichier

Les spécifications techniques du format de fichier VDW sont disponibles en ligne par [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) et peuvent être référencées par les développeurs pour créer applications. Le document technique décrit les données contenues dans un fichier composé qui contient des stockages et des flux. La représentation d'un Web Drawing est rendue possible grâce à un flux, nommé VisioServerData, via une archive ZIP. Une partie XML ShapGraphic dans l'archive décrit les éléments graphiques affichés dans le dessin Web et sont exprimés en langage XAML (Extensible Application Markup Language). Une collection de parties XML dans l'archive ZIP décrit la connexion de données du dessin Web, des informations sur sa forme et la logique de mise à jour du diagramme. Ces parties sont exprimées en XML. La partie DataGraphic XML décrit les propriétés recalculées qui doivent être évaluées après que les données du dessin Web ont été actualisées à partir de la source de données. Les éléments supplémentaires de l'archive ZIP contiennent des informations sur les polices et les images utilisées dans le dessin Web.

|![Implémentation possible d'un fichier](/fr/web/vdw.png "Implémentation possible d'un fichier")

## Références

* [[MS-VGSFF] : format de fichier du service graphique Visio (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

