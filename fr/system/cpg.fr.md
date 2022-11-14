{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier CPG - Fichier de page de code ESRI",
  "description":"En savoir plus sur le format de fichier CPG et les API qui peuvent créer et ouvrir des fichiers CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Qu'est-ce qu'un fichier CPG ?

Un fichier CPG est un fichier facultatif requis par le fichier de forme ESRI qui est utilisé pour spécifier la page de code permettant d'identifier le jeu de caractères à utiliser. Ceux-ci sont stockés au format de fichier texte brut et contiennent des informations sur l'encodage appliqué pour créer le fichier de formes. Si un fichier CPG n'est pas disponible, le fichier de formes utilise l'encodage par défaut du système. Un fichier CPG, s'il est présent, doit avoir le même préfixe que celui du fichier [SHP](/fr/gis/shp/), par exemple, roads.shp, roads.cpg.

Les fichiers CPG peuvent être ouverts avec ESRI ArcGIS Pro.

### Format de fichier CPG - Plus d'informations

Lorsque vous affichez un fichier de formes dans ArcCatalog ou toute autre application ArcGIS, vous ne voyez que le fichier de formes. Mais en réalité, shapefile utilise d'autres fichiers associés qui sont lus à côté du fichier de forme principal. Le fichier CPG en fait également partie s'il est présent à côté du fichier SHP principal.

## Références

* [Extensions de fichiers de formes
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

