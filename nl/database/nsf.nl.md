{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over NSF-bestandsindelingen en API's die NSF-bestanden kunnen maken en openen.",
  "title" :"NSF-bestandsindeling - Lotus Notes-databaseindeling",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Wat is een NSF-bestand?

Een bestand met de extensie .nsf (Notes Storage Facility) is een databasebestandsindeling die wordt gebruikt door de [IBM Notes-software](https://en.wikipedia.org/wiki/HCL_Domino), die voorheen bekend stond als Lotus Notes. Het definieert het schema om verschillende soorten objecten op te slaan, zoals e-mails, afspraken, documenten, formulieren en weergaven. Al deze informatie is opgenomen in een enkel NSF-bestand voor zakelijke samenwerking, vergelijkbaar met een PST/OST-bestand. Enkele van de toepassingen die NSF-bestanden kunnen openen, zijn IBM Lotus Notes en IBM Domino.

## Specificaties NSF-bestandsindeling

NSF-bestanden zijn binair van aard en hun specificaties zijn beschikbaar door Joachim Metz op [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Volgens deze details bestaat een NSF-bestand uit:

* Bestandskoptekst
* Databasekoptekst

Daarnaast bestaat het uit:

* Superblok
* Bucket-descriptorblok
* Bitmap
* Record Relocation Vector-emmer
* Overzicht emmers
* Niet-samenvattende buckets


### NSF-bestandskop

De kop van het NSF-bestand is 6 bytes groot. Het bestaat uit:

|Offset|Grootte|Waarde|Beschrijving|
---|---|---|---|
0|2|0x1a 0x00|Handtekening|
2|4| |De grootte van de databasekop|

### Databasekoptekst

De koptekst van de NSD-database bevat de volgende bevestigde waarden.

* Database-informatie
* Database-ID (DBID)
* Replicatie-informatie
* Database-informatiebuffervlaggen
* Titel
* Categorieën
* Klas
* Ontwerpklasse (sjabloonnaam)
* Speciale notitie-ID's
* Opvulling
* Database-informatie 2
* Database-informatie 3
* Database-informatie 4
* Database-informatie 5
* Opvulling
* Database-instantie-ID (DBIID)
* Replicatiegeschiedenis

## Referenties

* [NSF-indeling - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

