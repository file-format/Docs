{
  "date": "2022-05-08",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDB-filformat - ESRI-fil Geodatabase-fil",
  "description": "Lær om GDB-filformat og API'er, der kan oprette og åbne GDB-filer.",
  "linktitle": "GDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-gd-dab"
}
},
  "lastmod": "2022-05-08"
}

## Hvad er en GDB fil?

ESRI-fil Geodatabase (FileGDB) er en samling af filer i en mappe på disk, der indeholder relaterede geospatiale data såsom funktionsdatasæt, funktionsklasser og tilknyttede tabeller. Det kræver, at visse andre filer opbevares ved siden af .gdb-filen i samme mappe, for at den kan fungere. Forespørgsler kan udføres på .gdb-filen for at administrere rumlige såvel som ikke-rumlige data.

## GDB-filformat - flere oplysninger

Fil geodatabaser er opbygget af syv systemtabeller plus brugerdata. Brugerdata kan gemmes i følgende typer datasæt:

* Funktionsklasse

* Funktionsdatasæt

* Mosaikdatasæt

* Rasterkatalog

* Rasterdatasæt

* Skematisk datasæt

* Tabel (ikke-rumlig)

* Værktøjskasser


Funktionsdatasæt kan indeholde funktionsklasser såvel som følgende typer datasæt:

* Vedhæftede filer

* Feature-linked annotation

* Geometriske netværk

* Netværksdatasæt

* Pakkestoffer

* Relationsklasser

* Terræner

* Topologier


Den maksimale standardstørrelse af datasæt i filgeodatabaser er 1 TB. Den maksimale størrelse kan øges til 256 TB for store datasæt (normalt raster). Dette styres af et konfigurationsnøgleord. Se Konfigurationsnøgleord til filgeodatabaser for mere information.

Fil geodatabaser kan også indeholde undertyper og domæner og deltage i checkout/check-in replikering og envejs replikaer.

En fil geodatabase kan tilgås samtidigt af flere brugere. Hvis brugerne redigerer, skal de redigere forskellige datasæt.

## GDB-filformatspecifikationer ##

Fil GDB er ESRI proprietært format og dens specifikationer er ikke offentligt tilgængelige. Af denne grund kunne filformatdetaljerne for FIL GDB ikke dokumenteres andre steder end nogle kilder, der har gjort det [partially](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) ved omvendt konstruktion.

## Referencer ##

* [FGDB-specifikationer](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)


