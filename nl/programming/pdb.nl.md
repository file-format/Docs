{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDB-bestandsindeling - een programmadatabasebestand",
  "description":"Meer informatie over PDB-bestandsindeling en API's die PDB-bestanden kunnen maken en openen.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een PDB-bestand?

Een bestand met de extensie .pdb is een programmadatabasebestand dat foutopsporingsinformatie bevat voor een gecompileerd uitvoerbaar bestand (EXE/DLL). PDB-bestanden worden gegenereerd door Microsoft Compilers wanneer een toepassingsprogramma wordt gecompileerd in de foutopsporingsmodus. De aanwezigheid van een PDB-bestand kan helpen bij het reverse-engineeren van een uitvoerbaar bestand, omdat het belangrijke informatie bevat over alle symbolen van de modules. Het is om deze reden dat deze bestanden gescheiden worden gehouden van het uiteindelijke uitvoerbare bestand. Microsoft's [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) kan een PDB-bestand openen om informatie te verkrijgen zoals publics en exports, globale symbolen, lokale symbolen, type gegevens, bronbestanden en regelnummers.

## PDB-bestandsindeling

PDB is het eigen bestandsformaat van Microsoft en is nog nergens officieel gedocumenteerd. Er is echter een startdocumentatie [hier](https://github.com/Microsoft/microsoft-pdb) beschikbaar waarnaar kan worden verwezen.

### PDB-streams

PDB-bestanden bestaan uit meerdere streams waarbij elke stream fungeert als een virtueel individueel bestand en informatie bevat. Schrijvers van PDB-bestanden kunnen naar deze bestanden schrijven en het bestand wordt pas definitief nadat een expliciete vastlegging is gegeven. Een compiler kan naar een PDB-bestand blijven schrijven, maar alleen committen als alle gebruikerscode succesvol is gecompileerd. Een PDB-bestand bestaat uit de volgende streams:

|Streamnr. |Inhoud |Korte beschrijving|
---|---|---|
|1| Pdb (header) |Versie-informatie en informatie om deze PDB te verbinden met de EXE|
|2| Tpi (Type manager) |Alle typen die in het uitvoerbare bestand worden gebruikt.|
|3| Dbi (Debug-informatie) | Bevat sectiebijdragen en lijst met 'Mods'|
|4| NaamKaart| Bevat een gehashte stringtabel|
|4-(n+4)| n Mod's (Module informatie)| Elke Mod-stream bevat symbolen en regelnummers voor één compiland|
|n+4| Globaal symbool hash| Een index die het zoeken in globale symbolen op naam mogelijk maakt|
|n+5| Openbare symboolhash| Een index waarmee in openbare symbolen kan worden gezocht op adressen|
|n+6| Symbool records| Werkelijke symboolrecords van globale en openbare symbolen|
|n+7| Typ hash| Hash gebruikt door de TPI-stream.|

Elke stream in een PDB-bestand bestaat uit meerdere pagina's die niet noodzakelijk opeenvolgend zijn genummerd.

### PDB-header

Een PDB-bestand heeft een header die bestaat uit een handtekening voor het identificeren en valideren van het specifieke formaat. De lengte van de handtekening is afhankelijk van het PDB-formaat. De koptekst kan langer zijn dan een enkele pagina.

### VOB-metagegevens
De PDB-metadata is verantwoordelijk voor het herkennen van alle componentstromen, waarbij de lengte en volgorde van pagina's voor elke stream wordt gegeven. Orders worden achtereenvolgens aan streams gegeven; beginnend met 0. Er is ook een ongeordende rootstream, die enkele van de metadata bevat.

## Referenties
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft VOB](https://github.com/Microsoft/microsoft-pdb)

