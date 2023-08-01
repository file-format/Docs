{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo Binary Grid Format",
  "description":"Läs mer om ADF-filformat och API:er som kan skapa och öppna ADF-filer.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Vad är en ADF-fil?

En fil med filtillägget .adf är ett rasterdatafilformat som används av ESRI-program som ArcGIS, ArcView och ArcInfo. Rumslig data lagras som ett binärt rutnät som är inbyggt i ESRI. Rutnätet består av rader och kolumner med celler som kan vara heltal såväl som flyttal. Heltalsrutnät i en ADF-fil representerar diskreta data och flyttalsrutnät representerar kontinuerliga data. Ett annat populärt ESRI-filformat är [SHP](/sv/gis/shp/) fil som representerar geospatial information i form av vektordata som ska användas av Geographic Information Systems (GIS) applikationer.

## ADF-filformat - Mer information

ADF-filer sparas som binära filer på skiva i ett binärt rutnät. Heltalsrutnät har attribut som lagras i en värdeattributtabell (moms). Varje unikt värde i rutnätet har en post i moms där posten lagrar det unika värdet och antalet celler i rutnätet representeras av det värdet.

Flyttalsnät har ingen moms.

### Rutnätsstruktur

Inuti ADF-filen implementeras rutnät med hjälp av en sidalad rasterdatastruktur. Den grundläggande enheten inuti denna rasterdatastruktur är ett rektangulärt block av celler. Varje block lagras på skiva och komprimeras i en filstruktur med variabel längd, som kallas en bricka. Varje block lagras som en post med variabel längd.

GRID-raster lagras i arbetsytor, där en arbetsyta innehåller en informationsunderkatalog och en underkatalog för varje GRID. Det finns flera filer som geografiskt placerar och tillskriver data för motsvarande rutnät. Underkatalogen Info innehåller flera filer som upprätthåller viss information om GRID och andra datauppsättningar, såsom täckningar, i arbetsytan.

## Referenser ##

* [ESRI Grid Format](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)
