{
  "date": "2021-07-18",
  "keywords": [
"LOC",
"fil",
"udvidelse",
"filformat",
"GPS-placering",
"Waypoint"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOC - GPS-placeringsfilformat",
  "description": "Lær om LOC-filformat og API'er, der kan oprette og åbne LOC-filer.",
  "linktitle": "LOC",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-lo-dac"
}
},
  "lastmod": "2021-07-18"
}

## Hvad er en LOC fil?

En fil med filtypen .loc er en GPS-placeringsfil, der indeholder geospatiale placeringer som waypoints. Et waypoint er et par Latitude-Longitude værdier, der refererer til en placering, der bruges af Geographical Information System (GIS) applikationer. GPS-kortlægningsprogrammer, såsom DeLorme Topo, bruger LOC-filer til at læse og vise information indeholdt med disse LOC-filer som valgbare lag af slutbrugere. Derudover bruges disse til at udveksle GPS-data mellem applikationer. LOC-filer kan åbnes ved hjælp af applikationer som f.eks. [TopoGrafix EasyGPS](https://www.easygps.com/), der viser indholdet af sådanne filer som lag og data plottet på kortet ved respektive geolokation.

## LOC-filformat - flere oplysninger

LOC-filer har ligheder med [GPX](/gis/gpx/)-filer, men gemmes i andet format. Disse gemmes som [XML](/web/xml/) filer, hvor indholdet af waypoints og tilhørende information er indeholdt i strukturerede tags. Da XML er et generaliseret sprog til udveksling af data mellem forskellige applikationer, letter dette udvekslingen af LOC-data med andre applikationer.

## LOC-filformat - Eksempel

Følgende er overskriften og teksten til et waypoint fra en LOC-fil. Som det kan ses, indeholder headerinformationen kilden til placeringen af dataene. Waypointet indeholder information såsom ID og tilhørende indholdsdata knyttet til waypointet. Endelig er waypointet en samling af bredde- og længdegradsværdier og den tekst, der er knyttet til dette særlige waypoint.

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

## Referencer

* [TopGraphic EasyGPS](https://www.easygps.com/)


