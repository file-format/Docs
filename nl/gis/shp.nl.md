{
  "date" : "2019-10-11",
  "keywords" :[ "shp file", "shp file format", "wat is een shp file", "file", "shp example", "shp file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI-vormbestand",
  "description":"Meer informatie over SHP-bestandsindelingen en API's die SHP-bestanden kunnen maken en openen.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een SHP-bestand?

SHP is de bestandsextensie voor een van de primaire bestandstypen die worden gebruikt voor de weergave van ESRI Shapefile. Het vertegenwoordigt ruimtelijke informatie in de vorm van vectorgegevens die kunnen worden gebruikt door toepassingen van geografische informatiesystemen (GIS). Het formaat is ontwikkeld als open specificaties om de interoperabiliteit tussen ESRI en andere softwareproducten te vergemakkelijken.

## Data weergave

Zoals vermeld, beschrijft een shapefile-indeling geospatiale informatie van een dataset als vectorkenmerken. Deze vectorkenmerken omvatten:

* punten
* lijnen
* veelhoeken

Deze elementen in combinatie kunnen bijna elk type vorm vertegenwoordigen, zoals waterputten, landsgrenzen, ruimtelijke punten, rivieren, meren, enz. Elk vectorelement kan attributen hebben die het doel van dat element definiëren. Een shapefile met steden in Los Angeles kan bijvoorbeeld de naam en temperatuur van de stad als attributen hebben, wat een zinvolle weergave van de ruimtelijke gegevens geeft.

## Bijbehorende bestanden

Een op zichzelf staand SHP-bestand kan niet door softwaretoepassingen worden gebruikt om betekenis te geven aan de gegevens die het bevat. Om de informatie in een dergelijk bestand te begrijpen, maakt een shapefile gebruik van de volgende aanvullende verplichte bestanden.

* shx-bestand - indexbestand
* dbf-bestand - een dBASE-bestand dat alle attributen van de vormen in het hoofdbestand opslaat
* prj-bestand - slaat projectinformatie van het bestand op

Er kunnen ook andere optionele bestanden zijn die dezelfde naam hebben als het hoofdbestand.

## Specificaties SHP-bestandsindeling

Open specificaties van shapefile zijn online beschikbaar bij ESRI in de vorm van [Technische beschrijving](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) en werken de algemene structuur van het bestand in detail uit. De informatie in het hoofd-.shp-bestand bestaat uit headers en records. De bestandskop met een vaste lengte wordt gevolgd door records met een variabele lengte, waarbij elk record bestaat uit een recordkop met een vaste lengte, gevolgd door de inhoud van een record met een variabele lengte.

### Hoofd SHP-bestandskop

De hoofdbestandskop begint vanaf het begin van het bestand en is 100 bytes lang. De organisatie van deze hoofdbestandskop, samen met bytepositie, waarde, type en bytevolgorde, is zoals weergegeven in de volgende tabel.


|Bytes|Veld|Waarde|Type|Bytevolgorde
---|---|---|---|---|
|0-3|Bestandscode|9994|Geheel getal|Big Endian
|4-23|Ongebruikt|0|Geheel getal|Big Endian
|24-27|Bestandslengte|Bestandslengte|Geheel getal|Big Endian
|28-31|Versie|1000|Geheel getal|Little Endian
|32-35|Vormtype|Vormtype|Geheel getal|Little Endian
|36-67|Minimale begrenzingsrechthoek|Xmin, Ymin, Xmax en Ymax|dubbel|Little Endian
|68-83|Begrenzingsvak|Zmin, Zmax|dubbel|Little Endian
|84-99|Begrenzingsvak|Mmin, Mmax|dubbel|

Opgemerkt moet worden dat de waarde van de bestandslengte de totale lengte van het bestand in 16-bits woorden is, inclusief de vijftig 16-bits woorden die de kop vormen.

#### Vormtypen

De waarden van het veld met vormtypen in de bovenstaande tabel zijn als volgt:


|Waarde|Vormtype
---|---|
|0|Nullvorm
|1|Punt
|3|Polylijn
|5|Veelhoek
|8|Meerpunts
|11|PuntZ
|13|PolyLineZ
|15|PolygoonZ
|18|MultiPointZ
|21|PuntM
|23|PolyLineM
|25|PolygoonM
|28|MultiPointM
|31|MultiPatch

### Gegevensrecords ###

De kop van het hoofdbestand wordt gevolgd door records met een variabele lengte, waarbij elk record bestaat uit een recordkop met een vaste lengte, gevolgd door de inhoud van een record met een variabele lengte.

#### Koptekst opnemen ####

Recordheader bevat informatie over het recordnummer en de inhoudslengte van het record in een vaste lengte van 8 bytes. De organisatie van de recordkop is als volgt:


|Bytes|Veld|Waarde|Type|Bytevolgorde
---|---|---|---|---|
|0-3|Recordnummer|Recordnummer|Geheel getal|Groot
|4-7|Recordlengte|Recordlengte|Geheel getal|Groot

#### Inhoud opnemen ####

De inhoud van een shapefile-record bestaat uit een vormtype gevolgd door de geometrische gegevens voor die vorm. Een vormtype 0 vertegenwoordigt een nulvorm die geen geometrische gegevens voor de vorm heeft. De lengte van de recordinhoud is een weerspiegeling van de vormdelen en hoekpunten. Laten we een voorbeeld nemen van het puntvormtype om uit te leggen hoe een record informatie over een dergelijk vormtype bevat.

Een punt vertegenwoordigt een bepaalde geografische locatie in de volgorde X,Y waarbij elke coördinaat wordt weergegeven door een waarde met dubbele precisie. De volgende tabel toont de rangschikking van een puntvormtype.


|Bytes|Vormtype|Waarde|Type|Getal|Bytevolgorde
---|---|---|---|---|---|
|0-3|Vormtype|1|Geheel getal|1|Klein
|4-11|X|X|dubbel|1|Klein
|12-19|Y|Y|dubbel|1|Klein

Voorbeelden van andere vormtypes zijn te vinden in het technische beschrijvingsdocument van ESRI.

## Referenties ##

* [ESRI Shapefile technische beschrijving](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) door ESRI

