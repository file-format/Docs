{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "file", "extension", "file format", "GPS Location", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS helyfájl formátum",
  "description":"További információ a LOC fájlformátumról és az API-król, amelyek LOC fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Mi az a LOC fájl?

A .loc kiterjesztésű fájl egy GPS-helyfájl, amely útipontként térinformatikai helyeket tartalmaz. Az útpont egy szélesség-hosszúság értékpár, amely a földrajzi információs rendszer (GIS) alkalmazásai által használt helyre utal. A GPS-térképező programok, mint például a DeLorme Topo, LOC-fájlokat használnak az ezekben a LOC-fájlokban található információk olvasására és megjelenítésére a végfelhasználók által választható rétegként. Ezenkívül ezeket az alkalmazások közötti GPS-adatok cseréjére használják. A LOC-fájlok megnyithatók olyan alkalmazásokkal, mint például a [TopoGrafix EasyGPS](https://www.easygps.com/), amelyek az ilyen fájlok tartalmát rétegekként és a megfelelő földrajzi hely térképén ábrázolt adatokként jelenítik meg.

## LOC fájlformátum - További információ

A LOC fájlok hasonlóak a [GPX](/hu/gis/gpx/) fájlokhoz, de más formátumban kerülnek mentésre. Ezeket [XML](/hu/web/xml/) fájlként menti a rendszer, ahol az útpontok tartalma és a kapcsolódó információk strukturált címkékben találhatók. Mivel az XML egy általánosított nyelv a különböző alkalmazások közötti adatcseréhez, ez megkönnyíti a LOC adatok cseréjét más alkalmazásokkal.

## LOC fájlformátum - példa

A következő egy útpont fejléce és szövege látható egy LOC fájlból. Amint látható, a fejléc információ tartalmazza az adatok helyének forrását. Az útpont olyan információkat tartalmaz, mint az "azonosító" és az útponthoz társított tartalomadatok. Végül az útpont a szélességi és hosszúsági értékek gyűjteménye, valamint az adott fordulóponthoz tartozó szöveg.

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

## Hivatkozások

* [TopGraphic EasyGPS](https://www.easygps.com/)

