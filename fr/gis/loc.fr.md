{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "fichier", "extension", "format de fichier", "Localisation GPS", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Format de fichier de localisation GPS",
  "description":"En savoir plus sur le format de fichier LOC et les API qui peuvent créer et ouvrir des fichiers LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Qu'est-ce qu'un fichier LOC ?

Un fichier avec l'extension .loc est un fichier de localisation GPS qui contient des emplacements géospatiaux en tant que points de cheminement. Un waypoint est une paire de valeurs latitude-longitude qui fait référence à un emplacement utilisé par les applications du système d'information géographique (SIG). Les programmes de cartographie GPS, tels que DeLorme Topo, utilisent des fichiers LOC pour lire et afficher les informations contenues dans ces fichiers LOC sous forme de couches sélectionnables par les utilisateurs finaux. De plus, ceux-ci sont utilisés pour échanger des données GPS entre les applications. Les fichiers LOC peuvent être ouverts à l'aide d'applications telles que [TopoGrafix EasyGPS](https://www.easygps.com/) qui affiche le contenu de ces fichiers sous forme de couches et de données tracées sur la carte à la géolocalisation respective.

## Format de fichier LOC - Plus d'informations

Les fichiers LOC présentent des similitudes avec les fichiers [GPX](/fr/gis/gpx/) mais sont enregistrés dans un format différent. Ceux-ci sont enregistrés sous forme de fichiers [XML](/fr/web/xml/) où le contenu des waypoints et les informations associées sont contenus dans des balises structurées. Comme XML est un langage généralisé pour l'échange de données entre différentes applications, cela facilite l'échange de données LOC avec d'autres applications.

## Format de fichier LOC - Exemple

Voici l'en-tête et le texte d'un waypoint d'un fichier LOC. Comme on peut le voir, les informations d'en-tête contiennent la source d'emplacement des données. Le waypoint contient des informations telles que l'"ID" et les données de contenu associées associées au waypoint. Enfin, le waypoint est une collection de valeurs de latitude et de longitude et du texte associé à ce waypoint particulier.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Références

* [Top Graphic EasyGPS](https://www.easygps.com/)

