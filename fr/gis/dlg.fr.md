{
  "date" : "2021-07-30",
  "keywords" :[ "fichier dlg", "format de fichier dlg", "qu'est-ce qu'un fichier dlg", "fichier", "exemple dlg", "extension de fichier dlg","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Format d'index de forme de fichier de formes",
  "description":"En savoir plus sur le format de fichier DLG et les API qui peuvent créer et ouvrir des fichiers DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Qu'est-ce qu'un fichier DLG ?
Un fichier avec l'extension .dlg contient le Digital Line Graph qui est une caractéristique de carte cartographique affichée sous forme vectorielle numérique qui est administrée par l'US Geological Survey (USGS). Les fichiers DLG sont disponibles dans deux formats différents :
1. **Format facultatif** : format simple à utiliser qui intègre une longueur d'enregistrement logique de 80 octets, le système de coordonnées au sol UTM et les liens topologiques contenus dans les éléments de ligne, de nœud et de zone.
2. **Format SDTS (Spatial Data Transfer Standard)** : format qui facilite le transfert de données spatiales entre différents systèmes informatiques.

## Format de fichier DLG
Le format de fichier DLG est conçu pour les cartes USGS et est transmis à grande, moyenne et petite échelle avec jusqu'à neuf catégories différentes d'entités. Les fichiers DLG sont disponibles dans des formats facultatifs et SDTS (Spatial Data Transfer Standard) ayant une structure topologique pour une utilisation dans les applications de cartographie et SIG.
### Spécifications du format de fichier DLG
Les fichiers DLG sont distribués à trois échelles différentes :

1. **Grande échelle** - correspond normalement à :
- L'USGS 7,5 par 7,5 minutes
- Série de cartes quadrilatères topographiques à l'échelle 1:24 000 et 1:25 000
- Échelle 1:63 360 pour l'Alaska
- Échelle 1:30 000 pour Porto Rico
 

2. **Échelle intermédiaire** - dérivée de l'USGS :

- 30- par 60 minutes

- Série de cartes à l'échelle 1:100 000
3. **Petite échelle** - dérivée des cartes en coupe USGS à l'échelle 1:2 000 000 de l'Atlas national des États-Unis
### Catégories de données
Neuf catégories différentes de couches, ou fonctionnalités, sont disponibles dans les fichiers DLG :
1. Système de cadastre public (PLSS)
2. Limites (BD)
3. Transport (TR)
4. Hydrographie (HY)
5. Hypsographie (HP)
6. Caractéristiques non végétatives (NV)
7. Contrôle d'arpentage et marqueurs (SM)

8. Éléments artificiels (MS)

9. Couverture végétale de surface (SC)

Les fichiers DLG à grande échelle offrent les neuf couches, tandis que les fichiers à échelle intermédiaire offrent les cinq couches de PLSS, BD, TR, HY et HP. Les DLG à petite échelle offrent les cinq couches de PLSS, BD, TR, HY et MS.

## Références

* [Graphique linéaire numérique - par Wikipedia)] (https://en.wikipedia.org/wiki/Digital_line_graph)


