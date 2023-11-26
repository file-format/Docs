{
"date":"2023-07-20",
   "keywords":[
"BIN",
"BIN-bestand",
"bestand",
"BIN bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"BIN-bestandsindeling - MacBinary-gecodeerd bestand",
   "description":"Leer meer over het BIN-formaat en API's waarmee BIN-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
"parent":" compressie"
}
},
"lastmod":"2023-07-20"
}

## Wat is een BIN-bestand?

Een BIN-bestand kan, in de context van Macintosh-computers, verwijzen naar een bestand dat is opgeslagen in het MacBinary-formaat. MacBinary is een bestandsindeling die speciaal is ontworpen voor het overbrengen van Macintosh-bestanden via internet, e-mail, FTP of draagbare media. Het doel van MacBinary is om de volledige bestandsstructuur en kenmerken van Macintosh-bestanden, inclusief zowel de datavork als de bronvork, binnen één enkel bestand te behouden.

Het MacBinary-formaat bereikt dit door de bronvork en de gegevensvork van het Macintosh Hierarchical File System (HFS) in te kapselen in een gecomprimeerd bestand. Het bevat ook een finder-header die belangrijke metagegevens over het bestand bevat. Door al deze componenten in één bestand te combineren, zorgt MacBinary ervoor dat het bestand zijn integriteit behoudt en gemakkelijk kan worden overgedragen en gedeeld tussen verschillende platforms.

Met de vooruitgang in de bestandssystemen en bestandsoverdrachtprotocollen van Apple is het gebruik van BIN-bestanden en het MacBinary-formaat minder gebruikelijk geworden. De introductie van bestandsformaten zoals ZIP en de overgang naar modernere bestandssystemen, zoals HFS+ en APFS, hebben de behoefte aan MacBinary-gecodeerde bestanden verminderd. Deze nieuwere bestandssystemen bieden efficiëntere manieren om bestandskenmerken, bronvorken en datavorken te verwerken, waardoor het MacBinary-formaat minder noodzakelijk wordt in het huidige computerlandschap.

## BIN-bestandsformaat - Meer informatie

In de begindagen van Macintosh-computers werden bestanden vanwege gegevensbeperkingen in twee afzonderlijke "vorken" opgeslagen. De ‘resource fork’ bevatte gestructureerde gegevens, terwijl de ‘data fork’ ongestructureerde gegevens bevatte. Terwijl het klassieke Mac OS deze forks als één enkel bestand behandelde, resulteerde het overbrengen van bestanden naar niet-Mac-systemen in gegevensverlies omdat ze de forks niet als één geheel herkenden. Om dit aan te pakken, is het MacBinary-formaat gemaakt door individuen als de Dennis Brothers, Harry Chesley en Yves Lempereur. MacBinary comprimeerde en combineerde de forks tot één enkel bestand, ook wel een BIN-bestand genoemd, voor overdracht naar niet-Mac-systemen. Bij terugkeer naar het Mac OS zouden de vorken weer gescheiden worden. Met de overgang van de fork-gebaseerde HFS in de jaren 2000 nam het gebruik van het MacBinary-formaat aanzienlijk af. Tegenwoordig kom je zelden een MacBinary-gecodeerd BIN-bestand tegen, tenzij je een oud bestand tegenkomt op een niet-Mac-systeem of er een downloadt van internet.

Het MacBinary-formaat heeft in de loop van de tijd verschillende versies ondergaan om tegemoet te komen aan veranderingen in Macintosh-systemen en bestandsverwerking. Hier zijn enkele van de verschillende versies van het MacBinary-formaat:

- **MacBinary I:** De eerste versie van MacBinary, geïntroduceerd eind jaren tachtig. Het combineerde de resource fork en data fork in één enkel binair bestand, waardoor platformonafhankelijke overdracht van Macintosh-bestanden mogelijk werd.

- **MacBinary II:** Deze versie, uitgebracht begin jaren negentig, verbeterde het originele MacBinary-formaat door aanvullende informatie, zoals bestandstype en makercodes, toe te voegen aan de header van het binaire bestand. Deze codes hielpen de integriteit en identificatie van Macintosh-bestanden tijdens de overdracht te behouden.

- **MacBinary III:** Het MacBinary III-formaat, geïntroduceerd halverwege de jaren negentig, heeft de vorige versies verder verbeterd door aanvullende metagegevens op te nemen, zoals de bestandsnaam en de aanmaak- en wijzigingsdatums van bestanden, in de header van het binaire bestand. Dit maakte een uitgebreider behoud van Macintosh-bestandskenmerken tijdens de overdracht mogelijk.

- **MacBinary IV:** MacBinary IV is begin jaren 2000 ontwikkeld om compatibiliteitsproblemen met het opkomende Mac OS X-besturingssysteem op te lossen. Het bevatte wijzigingen om zich aan te passen aan de nieuwe bestandssysteemstructuur en kenmerken die in Mac OS X waren geïntroduceerd.

## Hoe open je een BIN-bestand?

De MacBinary Encoded BIN-bestanden kunnen worden geopend met behulp van verschillende compressiehulpprogramma's. Voor macOS-gebruikers is de **Apple Archive Utility** een geschikte optie. Windows-gebruikers kunnen software zoals **Smith Micro StuffIt Deluxe** gebruiken om de inhoud van een MacBinary Encoded BIN-bestand te extraheren. Een andere optie voor macOS-gebruikers is **The Unarchiver**, een veelzijdige tool die meerdere bestandsformaten kan verwerken, waaronder MacBinary.

Het is belangrijk op te merken dat de bestandsextensie .bin door verschillende bestandsformaten wordt gebruikt, niet alleen door MacBinary. Als u daarom een BIN-bestand tegenkomt dat niet kan worden geopend met de bovengenoemde hulpprogramma's, kan het in een ander formaat worden opgeslagen. In dergelijke gevallen moet u mogelijk het specifieke bestandsformaat identificeren en de juiste software of hulpprogramma's gebruiken die voor dat formaat zijn ontworpen om toegang te krijgen tot de bestandsinhoud.

## Andere BIN-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.bin** gebruiken.

- [BIN - Binair schijfimagebestand](/nl/disc-and-media/bin/)
- [BIN - Unix uitvoerbaar bestand](/nl/executable/bin/)
- [BIN - BlackBerry IT-beleidsbestand](/nl/settings/bin/)
- [BIN - Sega Genesis Game-ROM](/nl/game/bin/)
- [BIN - PSX PlayStation BIOS-afbeelding](/nl/game/bin-pcsx/)

## Referenties

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

