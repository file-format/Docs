{
  "date": "2019-10-11",
  "keywords": [
"shp fil",
"shp filformat",
"hvad er en shp-fil",
"fil",
"shp eksempel",
"shp filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHP - ESRI Shapefil",
  "description": "Lær om SHP-filformat og API'er, der kan oprette og åbne SHP-filer.",
  "linktitle": "SHP",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-dap"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en SHP fil?

SHP er filtypenavnet for en af de primære filtyper, der bruges til repræsentation af ESRI Shapefile. Det repræsenterer geospatial information i form af vektordata, der skal bruges af Geographic Information Systems (GIS) applikationer. Formatet er udviklet som åbne specifikationer for at lette interoperabilitet mellem ESRI og andre softwareprodukter.

## Datarepræsentation

Som nævnt beskriver et shapefile-format geospatial information om et datasæt som vektortræk. Disse vektorfunktioner inkluderer:

* point

* linjer

* polygoner


Disse funktioner i kombination kan repræsentere næsten enhver form for former som vandbrønde, landegrænser, rumlige punkter, floder, søer osv. Hver vektorfunktion kan have attributter, der faktisk definerer formålet med denne funktion. For eksempel kan en shapefil, der indeholder byer i Los Angeles, have bynavn og temperatur som attributter, der giver meningsfuld repræsentation af de rumlige data.

## Tilknyttede filer

En selvstændig shp-fil kan ikke bruges af softwareapplikationer til at give mening med de data, den indeholder. For at give mening med informationen indeholdt i en sådan fil, gør en shapefil brug af følgende yderligere obligatoriske filer.

* shx-fil - indeksfil

* dbf-fil - en dBASE-fil, der gemmer alle attributterne for figurerne i hovedfilen

* prj fil - gemmer projektinformation om filen


Der kan også være andre valgfrie filer, der deler samme navn som hovedfilen.

## SHP filformatspecifikationer

Åbne specifikationer for shapefile er tilgængelige online fra ESRI i form af [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) og uddyber den overordnede struktur af filen i detaljer. Oplysninger i .shp-hovedfilen består af overskrifter og poster. Filheaderen med fast længde efterfølges af poster med variabel længde, hvor hver post består af en postoverskrift med fast længde efterfulgt af postindhold med variabel længde.

### Hoved SHP-filoverskrift

Hovedfiloverskriften starter fra begyndelsen af filen og er 100 bytes lang. Organiseringen af denne hovedfiloverskrift sammen med byteposition, værdi, type og byterækkefølge er som vist i følgende tabel.


|Bytes|Felt|Værdi|Type|Byterækkefølge
---|---|---|---|---|
|0-3|Filkode|9994|Heltal|Big Endian
|4-23|Ubrugt|0|Heltal|Big Endian
|24-27|Fillængde|Fillængde|Heltal|Big Endian
|28-31|Version|1000|Heltal|Lille Endian
|32-35|Formtype|Formtype|Heltal|Lille endian
|36-67|Minimum afgrænsende rektangel|Xmin, Ymin, Xmax og Ymax|dobbelt|Lille endian
|68-83|Bounding Box|Zmin, Zmax|dobbelt|Lille Endian
|84-99|Bounding Box|Mmin, Mmax|dobbelt|

Det skal bemærkes, at værdien af fillængden er den samlede længde af filen i 16-bit ord, som også inkluderer de halvtreds 16-bit ord, der udgør headeren.

#### Formtyper

Værdierne for feltet formtyper i ovenstående tabel er som følger:


|Værdi|Formtype
---|---|
|0|Nul form
|1|Punkt
|3|Polyline
|5|Polygon
|8|MultiPoint
|11|PointZ
|13|PolyLineZ
|15|PolygonZ
|18|MultiPointZ
|21|Punkt M
|23|PolyLineM
|25|PolygonM
|28|MultiPointM
|31|MultiPatch

### Dataposter ###

Hovedfilens header efterfølges af poster med variabel længde, hvor hver post består af en postoverskrift med fast længde efterfulgt af postindhold med variabel længde.

#### Optagehoved ####

Recordheader indeholder information om postnummeret og indholdslængden af posten i en fast længde på 8 bytes. Organiseringen af posthovedet er som vist:


|Bytes|Felt|Værdi|Type|Byterækkefølge
---|---|---|---|---|
|0-3|Rekordnummer|Rekordnummer|Heltal|Stort
|4-7|Recordlængde|Recordlængde|Heltal|Stor

#### Optag indhold ####

En shapefile-postindhold består af en formtype efterfulgt af de geometriske data for den pågældende form. En formtype på 0 repræsenterer en nulform, der ikke har nogen geometriske data for formen. Længden af postens indhold afspejler formdelene og hjørnerne. Lad os tage et eksempel på Point Shape-type for at uddybe, hvordan en post indeholder information om en sådan formtype.

Et punkt repræsenterer en bestemt geografisk placering i rækkefølgen X,Y, hvor hver koordinat er repræsenteret af en dobbelt-præcisionsværdi. Følgende tabel viser arrangementet af en punktformtype.


|Bytes|Formtype|Værdi|Type|Nummer|Byterækkefølge
---|---|---|---|---|---|
|0-3|Formtype|1|Heltal|1|Lille
|4-11|X|X|dobbelt|1|Lille
|12-19|Y|Y|dobbelt|1|Lille

Examples of other shape types can be found the ESRI technical description document.

## Referencer ##

* [ESRI Shapefile Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) af ESRI


