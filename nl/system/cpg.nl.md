{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPG-bestandsindeling - ESRI-codepaginabestand",
  "description":"Meer informatie over CPG-bestandsindelingen en API's die CPG-bestanden kunnen maken en openen.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Wat is een CPG-bestand?

Een CPG-bestand is een optioneel bestand waarvoor het ESRI Shapefile nodig is dat wordt gebruikt om de codepagina op te geven voor het identificeren van de te gebruiken tekenset. Deze worden opgeslagen in platte tekstbestandsindeling en bevatten informatie over de codering die is toegepast voor het maken van het shapefile. Als er geen CPG-bestand beschikbaar is, gebruikt het shapefile de standaard systeemcodering. Een CPG-bestand, indien aanwezig, moet hetzelfde voorvoegsel hebben als dat van het [SHP](/nl/gis/shp/)-bestand, bijvoorbeeld wegen.shp, wegen.cpg.

CPG-bestanden kunnen worden geopend met ESRI ArcGIS Pro.

### CPG-bestandsindeling - Meer informatie

Wanneer u een shapefile bekijkt in ArcCatalog of een andere ArcGIS-toepassing, ziet u alleen de shapefile. Maar in werkelijkheid gebruikt shapefile andere bijbehorende bestanden die naast het hoofdvormbestand worden gelezen. Het CPG-bestand is ook een van deze als het naast het hoofd-SHP-bestand aanwezig is.

## Referenties

* [Shapefile bestandsextensies
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

