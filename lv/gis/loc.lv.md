{
  "date": "2021-07-18",
  "keywords": [
"LOC",
"failu",
"pagarinājumu",
"faila formātā",
"GPS atrašanās vieta",
"Ceļa punkts"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOC — GPS atrašanās vietas faila formāts",
  "description": "Uzziniet par LOC faila formātu un API, kas var izveidot un atvērt LOC failus.",
  "linktitle": "LOC",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-lo-lvc"
}
},
  "lastmod": "2021-07-18"
}

## Kas ir LOC fails?

Fails ar paplašinājumu .loc ir GPS atrašanās vietas fails, kurā kā pieturas punkti ir ģeotelpiskās atrašanās vietas. Pieturas punkts ir platuma-garuma vērtību pāris, kas attiecas uz vietu, ko izmanto ģeogrāfiskās informācijas sistēmas (GIS) lietojumprogrammas. GPS kartēšanas programmas, piemēram, DeLorme Topo, izmanto LOC failus, lai lasītu un parādītu informāciju, kas ietverta šajos LOC failos kā galalietotāju atlasāmos slāņus. Turklāt tos izmanto GPS datu apmaiņai starp lietojumprogrammām. LOC failus var atvērt, izmantojot tādas lietojumprogrammas kā [TopoGrafix EasyGPS](https://www.easygps.com/), kas parāda šādu failu saturu kā slāņus un datus, kas attēloti kartē attiecīgajā ģeogrāfiskajā atrašanās vietā.

## LOC faila formāts — vairāk informācijas

LOC failiem ir līdzības ar [GPX](/gis/gpx/) failiem, taču tie tiek saglabāti citā formātā. Tie tiek saglabāti kā [XML](/web/xml/) faili, kur maršruta punktu saturs un saistītā informācija ir ietverta strukturētos tagos. Tā kā XML ir vispārināta valoda datu apmaiņai starp dažādām lietojumprogrammām, tas atvieglo LOC datu apmaiņu ar citām lietojumprogrammām.

## LOC faila formāts — piemērs

Tālāk ir norādīta viena ceļa punkta galvene un teksts no LOC faila. Kā redzams, galvenes informācija satur datu atrašanās vietas avotu. Maršruta punkts satur tādu informāciju kā ID un saistītie satura dati, kas saistīti ar pieturas punktu. Visbeidzot, maršruta punkts ir platuma un garuma vērtību kolekcija un teksts, kas saistīts ar šo konkrēto pieturas punktu.

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

## Atsauces

* [TopGraphic EasyGPS](https://www.easygps.com/)


