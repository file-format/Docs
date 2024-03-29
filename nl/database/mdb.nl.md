{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over MDB-bestandsindelingen en API's die MDB-bestanden kunnen maken en openen.",
  "title" :"MDB-bestandsindeling - een Microsoft Access-databasebestand",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Wat is een MDB-bestand?

Een bestand met de extensie .mdb is een Microsoft Access-databasebestand dat een relationeel databasebeheersysteem (RDBMS) is. Het slaat gegevens op in databasetabellen die via primaire en externe sleutels aan elkaar zijn gekoppeld. Het MDB-bestand bevat de volledige structuur van de databasetabellen, query's, opgeslagen procedures. MDB is de standaard bestandsindeling voor Microsoft Access 2003. De laterale versies van Microsoft Access gebruiken de [ACCDB](/nl/database/accdb/) bestandsindelingen, de meest recente bestandsindeling tot nu toe. MDB-bestanden kunnen worden geopend met toepassingen zoals Microsoft Access, MDB Viewer, MDBOpener en kunnen worden geconverteerd naar ACCDB, [CSV](/nl/spreadsheet/csv/), Excel-indelingen, enz.

## MDB-bestandsindeling

Er zijn openbare specificaties beschikbaar voor het MDB-formaat en het blijft het eigen bestandsformaat van Microsoft. Microsoft biedt echter connectiviteitstoegang tot het MDB-bestand met behulp van de Open Database Connectivity (ODBC) -standaard en Visual Basic for Applications (VBA). De onofficiële MDB-gids geeft een korte informele beschrijving van het MDB-formaat op basis van reverse engineering en kan worden geraadpleegd voor meer informatie over de specificaties.

### Pagina's

Volgens de onofficiële MDB-gids bestaat een MDB-bestand uit pagina's met een vaste grootte (2048 bytes voor Jeb DB3 en 4096 bytes voor Jet DB 4). De eerste byte geeft het type pagina aan. Hieronder volgen de belangrijkste paginatypen:

`First Page:` Het bevat databaseheaderinformatie die ook de identificatie bevat van de Jet DB-versie waarmee het bestand compatibel is. Daarnaast bevat het ook informatie over bestandsbeveiliging en een kaart van het paginagebruik.

`Tabeldefinitiepagina:` Een tabeldefinitiepagina specificeert kolommen, gegevenstypen, index en andere informatie. Het gebruikt indien nodig extra pagina's en bevat een kaart met pagina's die de rijgegevens voor deze tabel bevat.

`Gegevenspagina's:` De gegevenspagina's zijn de feitelijke gegevenscontainers waarin gegevens per rij worden opgeslagen. Het gebruikt secundaire pagina's om lange gegevenswaarden op te slaan.

Een enkele Microsoft Access-database kan uit meerdere bestanden bestaan waarmee de beperkingen voor bestands- en tabelgrootte kunnen worden overschreden. Dit vergemakkelijkt het plaatsen van formulieren en code in een front-end MDB-bestand op het bureaublad van de gebruiker en gegevens in een andere backend MDB-bestanden op servers die op het netwerk zijn aangesloten.

## Referenties ##

* [Toegangsspecificaties](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
