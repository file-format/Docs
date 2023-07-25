{
  "date" : "2019-10-11",
  "keywords" :[ "shp-fil", "shp-filformat", "vad är en shp-fil", "fil", "exempel på shp", "shp filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"Läs mer om SHP-filformat och API:er som kan skapa och öppna SHP-filer.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är SHP fil?

SHP är filtillägget för en av de primära filtyperna som används för representation av ESRI Shapefile. Den representerar geospatial information i form av vektordata som ska användas av Geographic Information Systems (GIS) applikationer. Formatet har utvecklats som öppna specifikationer för att underlätta interoperabilitet mellan ESRI och andra mjukvaruprodukter.

## Datarepresentation

Som nämnts beskriver ett shapefil-format geospatial information för en datamängd som vektoregenskaper. Dessa vektorfunktioner inkluderar:

* poäng
* linjer
* polygoner

Dessa funktioner i kombination kan representera nästan alla typer av former som vattenbrunnar, landsgränser, rumsliga punkter, floder, sjöar, etc. Varje vektorfunktion kan ha attribut som faktiskt definierar syftet med den egenskapen. Till exempel kan en shapefil som innehåller städer i Los Angeles ha stadsnamn och temperatur som attribut som ger en meningsfull representation till rumsliga data.

## Associerade filer

En fristående shp-fil kan inte användas av mjukvaruapplikationer för att skapa mening med data den innehåller. För att förstå informationen i en sådan fil använder en shapefil följande ytterligare obligatoriska filer.

* shx-fil - indexfil
* dbf-fil - en dBASE-fil som lagrar alla attribut för formerna i huvudfilen
* prj-fil - lagrar projektinformation om filen

Det kan också finnas andra valfria filer som delar samma namn som huvudfilen.

## Specifikationer för SHP-filformat

Öppna specifikationer för shapefile är tillgängliga online från ESRI i form av [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) och utarbetar filens övergripande struktur i detalj. Informationen i .shp-huvudfilen består av rubriker och poster. Filhuvudet med fast längd följs av poster med variabel längd där varje post består av ett posthuvud med fast längd följt av postinnehåll med variabel längd.

### Huvudhuvud för SHP-fil

Huvudfilhuvudet börjar från början av filen och är 100 byte lång. Organisationen av denna huvudfilhuvud tillsammans med byteposition, värde, typ och byteordning är som visas i följande tabell.


|Bytes|Fält|Värde|Typ|Byteordning
---|---|---|---|---|
|0-3|Filkod|9994|Heltal|Big Endian
|4-23|Oanvänd|0|Heltal|Big Endian
|24-27|Fillängd|Fillängd|Heltal|Big Endian
|28-31|Version|1000|Heltal|Lilla Endian
|32-35|Formtyp|Formtyp|Heltal|Lilla Endian
|36-67|Minimum avgränsande rektangel|Xmin, Ymin, Xmax och Ymax|dubbel|Lilla endian
|68-83|Bounding Box|Zmin, Zmax|dubbel|Little Endian
|84-99|Bounding Box|Mmin, Mmax|dubbel|

Det bör noteras att värdet på fillängden är den totala längden av filen i 16-bitars ord som också inkluderar de femtio 16-bitars ord som utgör rubriken.

#### Formtyper

Värdena för fältet formtyper i tabellen ovan är följande:


|Värde|Formtyp
---|---|
|0|Nullform
|1|Punkt
|3|Polyline
|5|Polygon
|8|MultiPoint
|11|PointZ
|13|PolyLineZ
|15|PolygonZ
|18|MultiPointZ
|21|PointM
|23|PolyLineM
|25|PolygonM
|28|MultiPointM
|31|MultiPatch

### Dataposter ###

Huvudfilens rubrik följs av poster med variabel längd där varje post består av ett posthuvud med fast längd följt av postinnehåll med variabel längd.

#### Inspelningshuvud ####

Posthuvudet innehåller information om postnummer och innehållslängd för posten i en fast längd på 8 byte. Organisationen av posthuvudet är som visas:


|Bytes|Fält|Värde|Typ|Byteordning
---|---|---|---|---|
|0-3|Rekordsnummer|Rekordsnummer|Heltal|Stor
|4-7|Rekordslängd|Rekordslängd|Heltal|Stor

#### Spela in innehåll ####

En formfilspostinnehåll består av en formtyp följt av geometriska data för den formen. En formtyp 0 representerar en nollform som inte har några geometriska data för formen. Längden på postinnehållet reflekterar formdelarna och hörnen. Låt oss ta ett exempel på Point Shape-typ för att utveckla hur en post innehåller information om en sådan formtyp.

En punkt representerar en viss geografisk plats i ordningen X,Y där varje koordinat representeras av ett dubbelprecisionsvärde. Följande tabell visar arrangemanget av en punktformstyp.


|Bytes|Formtyp|Värde|Typ|Nummer|Byteordning
---|---|---|---|---|---|
|0-3|Formtyp|1|Heltal|1|Litt
|4-11|X|X|dubbel|1|Litt
|12-19|Y|Y|dubbel|1|Litt

Exempel på andra formtyper finns i ESRI:s tekniska beskrivningsdokument.

## Referenser ##

* [ESRI Shapefile Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) av ESRI

