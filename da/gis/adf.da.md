{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADF - ESRI ArcInfo Binary Grid Format",
  "description":"Lær om ADF-filformat og API'er, der kan oprette og åbne ADF-filer.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf-da",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Hvad er en ADF fil?

En fil med filtypenavnet .adf er et rasterdatafilformat, der bruges af ESRI-softwareprogrammer såsom ArcGIS, ArcView og ArcInfo. Geografiske data gemmes som et binært gitter, der er hjemmehørende i ESRI. Gitteret består af rækker og kolonner af celler, der kan være heltal såvel som flydende komma. Heltalsgitter i en ADF-fil repræsenterer diskrete data, og flydende kommagitter repræsenterer kontinuerlige data. Et andet populært ESRI-filformat er [SHP](/gis/shp/) fil, der repræsenterer geospatial information i form af vektordata, der skal bruges af Geographic Information Systems (GIS) applikationer.

## ADF-filformat - flere oplysninger

ADF-filer gemmes som binære filer på disk i et binært gitter. Heltalsgitter har attributter, der er gemt i en værdiattributtabel (moms). Hver unik værdi i gitteret har én post i moms, hvor posten gemmer den unikke værdi, og antallet af celler i gitteret er repræsenteret af denne værdi.

Flydende kommagitter har ikke moms.

### Gitterstruktur

Inde i ADF-filen implementeres gitter ved hjælp af en flisebelagt rasterdatastruktur. Den grundlæggende enhed i denne rasterdatastruktur er en rektangulær blok af celler. Hver blok er gemt på disk og komprimeret i en filstruktur med variabel længde, kaldet en flise. Hver blok er gemt som én variabel længde record.

GRID-rastere gemmes i arbejdsområder, hvor et arbejdsområde indeholder én info-undermappe og en undermappe for hvert GRID. Der er flere filer, der geografisk placerer og tilskriver data for det tilsvarende gitter. Info-undermappen indeholder flere filer, som vedligeholder visse oplysninger om GRID og andre datasæt, såsom dækninger, i arbejdsområdet.

## Referencer ##

* [ESRI Grid Format](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)



