{
  "date" : "2019-10-11",
  "keywords" :[ "fichier kmz", "qu'est-ce qu'un fichier kmz", "fichier", "exemple kmz", "extension de fichier kmz","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Format de fichier compressé KML",
  "description":"En savoir plus sur le format de fichier KMZ et les API qui peuvent créer et ouvrir des fichiers KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier KMZ ?

Le fichier KMZ (KML Zipped) est une représentation du fichier [KML](/fr/gis/kml/) compressé qui contient des informations géospatiales visibles dans les applications SIG comme Google Earth. Les informations sur les repères sont représentées dans le fichier sous forme de latitude et de longitude avec un nom personnalisé. Le fichier KMZ unique peut être facilement partagé avec d'autres utilisateurs. Les fichiers KMZ peuvent également inclure des données de modèle 3D pour la géo-représentation du modèle. Un fichier KMZ peut être ouvert dans Google Maps en enregistrant le fichier dans un emplacement en ligne, puis en tapant l'URL dans la zone de recherche Google Maps.

## Structure du fichier ##

Le contenu d'un fichier MKZ se compose d'un fichier KML principal et de zéro ou plusieurs fichiers associés. Il peut être extrait à l'aide d'un utilitaire de décompression standard tel que WinZIP. Le format de fichier KMZ est également compressé dans une archive avec un taux de compression de 10:1. Vous pouvez exporter des données de Google Earth comme des applications directement au format de fichier KMZ. Le fichier KML principal est nommé **doc.kml**. Lors de l'empaquetage d'un fichier KMZ, plusieurs fichiers KML peuvent y être ajoutés, mais cela ne sera d'aucun avantage car Google Earth recherche le premier fichier KML lors de l'ouverture du fichier KMZ et le lit. Il ignore tous les autres fichiers KML trouvés dans l'archive. Afin d'être sûr que le fichier KML souhaité est lu par Google Earth, il est recommandé de ne placer qu'un seul fichier KML dans le fichier KMZ.

Les images, modèles, textures, fichiers audio et autres ressources référencés dans le fichier doc.kml sont placés dans un autre sous-dossier à l'intérieur du dossier principal. Cela peut également impliquer une certaine complexité en fonction du nombre de fichiers à l'appui. Les liens vers ces ressources constitutives peuvent être référencés de manière relative ou via un référencement absolu.

### Référencement relatif ###

Lorsque les ressources sont placées à côté du fichier doc.kml principal dans un sous-dossier du dossier principal, le référencement relatif peut pointer vers ces fichiers de support, comme illustré dans l'exemple suivant (pour l'icône uniquement).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Référencement absolu ###

Les ressources peuvent également être référencées de manière absolue. Les références absolues contiennent l'URL complète du fichier lié. Lorsque les fichiers sont postés sur un serveur central, le référencement absolu permet de s'assurer que ceux-ci restent sans ambiguïté par rapport au référencement relatif. Il n'est pas recommandé de référencer les fichiers locaux de manière absolue car ces liens seront rompus lorsque les fichiers seront déplacés vers un nouveau système. Un exemple de référencement absolu est le suivant :

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Voir également ##

* [GeoJSON](/fr/gis/geojson/)

## Références ##

* [Fichiers Google Earth et KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

