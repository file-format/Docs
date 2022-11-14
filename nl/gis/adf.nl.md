{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo binair rasterformaat",
  "description":"Meer informatie over ADF-bestandsindelingen en API's die ADF-bestanden kunnen maken en openen.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Wat is een ADF-bestand?

Een bestand met de extensie .adf is een bestandsindeling voor rastergegevens die wordt gebruikt door ESRI-softwaretoepassingen zoals ArcGIS, ArcView en ArcInfo. Ruimtelijke gegevens worden opgeslagen als een binair raster dat eigen is aan ESRI. Het raster bestaat uit rijen en kolommen met cellen die zowel een geheel getal als een zwevend punt kunnen zijn. Integer-rasters in een ADF-bestand vertegenwoordigen discrete gegevens en zwevende-kommarasters vertegenwoordigen continue gegevens. Een ander populair ESRI-bestandsformaat is het [SHP](/nl/gis/shp/)-bestand dat geospatiale informatie vertegenwoordigt in de vorm van vectorgegevens voor gebruik door geografische informatiesystemen (GIS)-toepassingen.

## ADF-bestandsindeling - Meer informatie

ADF-bestanden worden opgeslagen als binaire bestanden op schijf in een binair raster. Integer grids hebben attributen die zijn opgeslagen in een value attribute table (BTW). Elke unieke waarde in het raster heeft één btw-record waarin het record de unieke waarde opslaat en het aantal cellen in het raster wordt weergegeven door die waarde.

Drijvende-kommaroosters hebben geen btw.

### Rasterstructuur

In het ADF-bestand worden rasters geïmplementeerd met behulp van een betegelde rastergegevensstructuur. De basiseenheid binnen deze rastergegevensstructuur is een rechthoekig blok cellen. Elk blok wordt op schijf opgeslagen en gecomprimeerd in een bestandsstructuur met variabele lengte, een tegel genoemd. Elk blok wordt opgeslagen als één record met variabele lengte.

GRID-rasters worden opgeslagen in werkruimten, waar een werkruimte één info-submap en een submap voor elk GRID bevat. Er zijn verschillende bestanden met geografische locatie en attribuutgegevens voor het bijbehorende raster. De submap Info bevat verschillende bestanden die bepaalde informatie over de GRID en andere datasets, zoals dekkingen, in de werkruimte bewaren.

## Referenties ##

* [ESRI-rasterindeling](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [FAQ: Wat is de bestandsstructuur van een Arc/INFO Grid?](https://support.esri.com/en/technical-article/000008526)

