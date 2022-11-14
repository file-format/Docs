{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over de FMPSL-bestandsindeling en API's die FMPSL-bestanden kunnen maken en openen.",
  "title" :"FMPSL-bestandsindeling - FileMaker Pro 12 Snapshot Link-bestand",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Wat is een FMPSL-bestand?

Een FMPSL-bestand is een snapshotbestand van een database die is gemaakt met FileMaker Pro 12. Het slaat de opgevraagde resultaten van de database op, samen met andere informatie zoals visuele lay-out en zichtbare informatie. Het FMPSL-bestand kan worden gebruikt om al deze gegevens in een ander exemplaar van de FileMaker Pro-database te herstellen. Deze bestandsindeling is geïntroduceerd met de lancering van FileMaker Pro v 12. Vóór deze versie werden de snapshot-koppelingen geïntroduceerd als FPSL-bestandsindeling in FileMaker Pro v 11. FMPSL-bestanden kunnen worden geopend met FileMaker Pro Advanced-software. Andere bestandsindelingen die door FileMaker Pro worden ondersteund, zijn [FP5](/nl/database/fp5/), [FP7](/nl/database/fp7/) en [FMP12](/nl/database/fmp12/).

## FMPSL-bestandsindeling

De details van de interne bestandsindeling van FMPSL-bestanden zijn niet openbaar beschikbaar voor referentie van de ontwikkelaar.

### Hoe records op te slaan als FMPSL-bestand?

Gegevens uit de FileMaker Pro-database kunnen worden opgeslagen als snapshot-linkbestand met behulp van de volgende stappen.

1. Zoek de records uit de database die moeten worden opgeslagen als een snapshot-linkbestand.
1. Gebruik de optie Opname verzenden als link naar momentopname in het menu en sla het bestand op door een bestandsnaam in te voeren.
1. Gebruik de Records die worden doorzocht om de volledige gevonden reeks records op te slaan.

Het gegenereerde snapshotbestand wordt met de opgegeven naam op schijf opgeslagen.

## Referenties

* [Converteer eerdere versies van FileMaker Pro-bestandsindelingen naar FMP12-bestandsindeling](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Records opslaan als een snapshot-linkbestand](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

