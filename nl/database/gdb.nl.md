{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDB-bestandsindeling - ESRI-bestand Geodatabase-bestand",
  "description":"Meer informatie over de GDB-bestandsindeling en API's die GDB-bestanden kunnen maken en openen.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Wat is een GDB-bestand?

ESRI-bestand Geodatabase (FileGDB) is een verzameling bestanden in een map op schijf die gerelateerde georuimtelijke gegevens bevatten, zoals functiegegevenssets, functieklassen en bijbehorende tabellen. Het vereist dat bepaalde andere bestanden naast het .gdb-bestand in dezelfde map worden bewaard om te kunnen werken. Query's kunnen worden uitgevoerd op het .gdb-bestand om zowel ruimtelijke als niet-ruimtelijke gegevens te beheren.

## GDB-bestandsindeling - Meer informatie

Bestandsgeodatabases bestaan uit zeven systeemtabellen plus gebruikersgegevens. Gebruikersgegevens kunnen worden opgeslagen in de volgende soorten datasets:

* Functieklasse
* Functiegegevensset
* Mozaïek dataset
* Rastercatalogus
* Rastergegevensset
* Schematische dataset
* Tabel (niet-ruimtelijk)
* Gereedschapskisten

Functiegegevenssets kunnen zowel functieklassen als de volgende typen gegevenssets bevatten:

* Bijlagen
* Aan functies gekoppelde annotatie
* Geometrische netwerken
* Netwerkgegevenssets
* Pakketstoffen
* Relatie lessen
* Terreinen
* Topologieën

De standaard maximale grootte van datasets in bestandsgeodatabases is 1 TB. De maximale grootte kan worden verhoogd tot 256 TB voor grote datasets (meestal raster). Dit wordt beheerd door een configuratiesleutelwoord. Zie Configuratiesleutelwoorden voor bestandsgeodatabases voor meer informatie.

Bestandsgeodatabases kunnen ook subtypes en domeinen bevatten en deelnemen aan checkout/check-in replicatie en one-way replica's.

Een bestandsgeodatabase kan tegelijkertijd door meerdere gebruikers worden geopend. Als de gebruikers aan het bewerken zijn, moeten ze verschillende datasets bewerken.

## Specificaties GDB-bestandsindeling ##

Bestand GDB is een eigen formaat van ESRI en de specificaties ervan zijn niet publiekelijk beschikbaar. Om deze reden konden de details van het bestandsformaat voor FIle GDB nergens anders worden gedocumenteerd dan sommige bronnen die het [gedeeltelijk] (https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) hebben gedaan door reverse engineering .

## Referenties ##

* [FGDB-specificaties](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

