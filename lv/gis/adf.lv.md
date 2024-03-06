{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADF — ESRI ArcInfo binārā režģa formāts",
  "description":"Uzziniet par ADF failu formātu un API, kas var izveidot un atvērt ADF failus.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf-lv",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Kas ir ADF fails?

Fails ar .adf paplašinājumu ir rastra datu faila formāts, ko izmanto ESRI lietojumprogrammas, piemēram, ArcGIS, ArcView un ArcInfo. Telpiskie dati tiek glabāti kā binārs režģis, kas ir native ESRI. Režģi veido šūnu rindas un kolonnas, kas var būt gan veseli skaitļi, gan peldošā komata forma. Veselu skaitļu režģi ADF failā apzīmē diskrētus datus un peldošā komata režģi – nepārtrauktus datus. Vēl viens populārs ESRI faila formāts ir [SHP](/gis/shp/) fails, kas attēlo ģeotelpisko informāciju vektordatu veidā, ko izmantos ģeogrāfiskās informācijas sistēmu (GIS) lietojumprogrammās.

## ADF faila formāts — plašāka informācija

ADF faili tiek saglabāti kā binārie faili diskā binārā režģī. Veseliem režģiem ir atribūti, kas tiek saglabāti vērtību atribūtu tabulā (PVN). Katrai unikālajai vērtībai režģī ir viens PVN ieraksts, kurā ierakstā tiek glabāta unikālā vērtība, un šī vērtība attēlo šūnu skaitu režģī.

Peldošā komata režģī nav PVN.

### Režģa struktūra

ADF failā režģi tiek ieviesti, izmantojot flīžu rastra datu struktūru. Šīs rastra datu struktūras pamatvienība ir taisnstūrveida šūnu bloks. Katrs bloks tiek saglabāts diskā un saspiests mainīga garuma faila struktūrā, ko sauc par flīzi. Katrs bloks tiek saglabāts kā viens mainīga garuma ieraksts.

GRID rastri tiek glabāti darbvietās, kur darbvieta satur vienu informācijas apakšdirektoriju un apakšdirektoriju katram GRID. Ir vairāki faili, kas nosaka ģeogrāfisko atrašanās vietu un atbilstošā režģa atribūtu datus. Informācijas apakšdirektorijā ir vairāki faili, kas darbvietā uztur noteiktu informāciju par GRID un citām datu kopām, piemēram, pārklājumiem.

## Atsauces Nr.

* [ESRI režģa formāts](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)



