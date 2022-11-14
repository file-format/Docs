{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "bestand", "extensie", "bestandsformaat", "GPS-locatie", "Waypoint"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS-locatiebestandsindeling",
  "description":"Meer informatie over LOC-bestandsindeling en API's die LOC-bestanden kunnen maken en openen.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Wat is een LOC-bestand?

Een bestand met de extensie .loc is een GPS-locatiebestand dat georuimtelijke locaties als waypoints bevat. Een waypoint is een paar Latitude-Longitude-waarden die verwijzen naar een locatie die wordt gebruikt door GIS-toepassingen (Geografisch Informatiesysteem). GPS-kaartprogramma's, zoals DeLorme Topo, gebruiken LOC-bestanden om informatie in deze LOC-bestanden te lezen en weer te geven als selecteerbare lagen door eindgebruikers. Daarnaast worden deze gebruikt om GPS-gegevens uit te wisselen tussen applicaties. LOC-bestanden kunnen worden geopend met toepassingen zoals [TopoGrafix EasyGPS](https://www.easygps.com/) die de inhoud van dergelijke bestanden weergeeft als lagen en gegevens die op de kaart zijn uitgezet op de respectieve geolocatie.

## LOC-bestandsindeling - Meer informatie

LOC-bestanden hebben overeenkomsten met [GPX](/nl/gis/gpx/)-bestanden, maar worden in een ander formaat opgeslagen. Deze worden opgeslagen als [XML](/nl/web/xml/)-bestanden waarbij de inhoud van waypoints en bijbehorende informatie is opgenomen in gestructureerde tags. Aangezien XML een algemene taal is voor de uitwisseling van gegevens tussen verschillende toepassingen, vergemakkelijkt dit de uitwisseling van LOC-gegevens met andere toepassingen.

## LOC-bestandsindeling - voorbeeld

Hieronder volgt de kop en tekst van één waypoint uit een LOC-bestand. Zoals te zien is, bevat de kopinformatie de locatiebron voor de gegevens. Het waypoint bevat informatie zoals de 'ID' en bijbehorende inhoudsgegevens die bij het waypoint horen. Ten slotte is het waypoint een verzameling breedte- en lengtegraadwaarden en de tekst die bij dit specifieke waypoint hoort.

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

## Referenties

* [TopGraphic EasyGPS](https://www.easygps.com/)

