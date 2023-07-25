{
  "date" : "2019-10-11",
  "keywords" :[ "fichier gpx", "qu'est-ce qu'un fichier gpx", "fichier", "exemple gpx", "extension de fichier gpx","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - Format de fichier d'échange GPX",
  "description":"En savoir plus sur le format de fichier GPX et les API qui peuvent créer et ouvrir des fichiers GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier GPX ?

Les fichiers avec l'extension GPX représentent le format GPS Exchange pour l'échange de données GPS entre les applications et les services Web sur Internet. Il s'agit d'un format de fichier XML léger qui contient des données GPS, c'est-à-dire des points de cheminement, des itinéraires et des pistes à importer et à lire par plusieurs programmes. Le format de fichier GPX est ouvert et est pris en charge par une variété d'applications et d'appareils GPS. Les données GPS de ces fichiers peuvent être chargées pour être affichées sur des applications de cartographie à des fins géospatiales.

## Format de fichier GPX ##

Un fichier GPX se compose de données de localisation de latitude et de longitude, de valeurs d'altitude et d'autres informations descriptives éventuellement. Les données de localisation sont exprimées en degrés décimaux et l'altitude est exprimée en mètres. L'heure dans un fichier GPX est en temps universel coordonné (UTC) au format ISO 8601. Les avantages de l'utilisation d'un fichier GPX sont les suivants :

* GPX vous permet d'échanger des données avec une liste croissante de programmes pour Windows, MacOS, Linux, Palm et PocketPC.
* GPX peut être transformé en d'autres formats de fichiers à l'aide d'une simple page Web ou d'un programme de conversion.
* GPX est basé sur la norme XML, de sorte que bon nombre des nouveaux programmes que vous utilisez (Microsoft Excel, par exemple) peuvent lire les fichiers GPX.
* GPX permet à n'importe qui sur le Web de développer facilement de nouvelles fonctionnalités qui fonctionneront instantanément avec vos programmes préférés.

Le [schéma GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) montre la représentation du format de fichier GPX pour référence.

### Données essentielles ###

Voici les données essentielles qui font partie d'un fichier GPX pour la représentation des données GPS.

* **Waypoints** : un waypoint est une coordonnée WGS84 (GPS) d'un point et représente une couche d'entités de type OGR wkbPoint
* **Routes** : Représentent une couche de fonctionnalités de type OGR wkbLineString. Il comprend une liste de points de trace, qui sont des points de cheminement montrant un virage ou des points d'étape qui mènent à une destination
* **Tracks** : les pistes représentent une couche d'entités de type OGR wkbMultiLineString. Il est composé d'au moins un segment contenant des waypoints dans une liste ordonnée de points décrivant un chemin. Il se compose d'une liste de points de trace qui représentent une trace GPS continue.

### Exemple de fichier GPX ###

Le fichier GPX suivant montre l'organisation des données GPS dans un fichier GPX et peut donner une bonne idée du contenu d'un fichier GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Références ##

* [Format de fichier GPX](https://www.topografix.com/gpx.asp)
* [GPX - Par Wikipédia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

