{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "fil", "tillägg", "filformat", "GPS-plats", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS-platsfilformat",
  "description":"Läs mer om LOC-filformat och API:er som kan skapa och öppna LOC-filer.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Vad är en LOC fil?

En fil med filändelsen .loc är en GPS-platsfil som innehåller geospatiala platser som waypoints. En waypoint är ett par latitud-longitudvärden som refererar till en plats som används av Geographical Information System (GIS) applikationer. GPS-kartläggningsprogram, som DeLorme Topo, använder LOC-filer för att läsa och visa information som finns med dessa LOC-filer som valbara lager av slutanvändare. Dessutom används dessa för att utbyta GPS-data mellan applikationer. LOC-filer kan öppnas med applikationer som [TopoGrafix EasyGPS](https://www.easygps.com/) som visar innehållet i sådana filer som lager och data plottade på kartan vid respektive geolokalisering.

## LOC-filformat - Mer information

LOC-filer har likheter med [GPX](/sv/gis/gpx/)-filer men sparas i annat format. Dessa sparas som [XML](/sv/web/xml/)-filer där innehållet i waypoints och tillhörande information finns i strukturerade taggar. Eftersom XML är ett generaliserat språk för utbyte av data mellan olika applikationer, underlättar detta utbytet av LOC-data med andra applikationer.

## LOC-filformat - Exempel

Följande är rubriken och texten för en waypoint från en LOC-fil. Som kan ses innehåller rubrikinformationen källan till plats för data. Waypointen innehåller information som "ID" och tillhörande innehållsdata som är associerade med waypointen. Slutligen är waypointen en samling av latitud- och longitudvärden och texten som är associerad med just denna waypoint.

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

## Referenser

* [TopGraphic EasyGPS](https://www.easygps.com/)

