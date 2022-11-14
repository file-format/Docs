{
  "date" : "2021-08-24",
  "keywords" :[ "wdb-bestand", "wdb-bestandsindeling", "wat is een wdb-bestand", "bestand", "wdb-voorbeeld", "wdb-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over WDB-bestandsindeling en API's die WDB-bestanden kunnen maken en openen.",
  "title" :"WDB - SQL Server-traceringsbestand",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Wat is een WDB-bestand?
Een bestand met de extensie .wdb is eigenlijk een databasebestand gemaakt door Microsoft Works dat werd gebruikt om functies uit te voeren zoals een databasebeheersysteem. Het WDB-bestand is vergelijkbaar met het Access Database-bestand ([MDB](/nl/database/mdb/)), maar minder efficiënt en met grotere beperkingen. De WDB-bestanden kunnen niet worden geopend met Microsoft Access. U kunt het WDB-bestand echter openen in Microsoft Works en het vervolgens exporteren naar het MDB-bestand om een WDB-bestand in MS Access te openen.

## WDB-bestandsindeling
Microsoft Works-database is de native database-indeling van de Microsoft Works-kantoorsuite. Vanwege de gepatenteerde aard van het formaat en enkele beperkingen. De WDB-bestanden kunnen niet worden geopend in andere software dan Microsoft Works. In het bestandsformaat kan een terugkerende header van 10 bytes worden gevonden voor elk van de ASCII-tekstreeksen die de waarden vertegenwoordigen van de velden die werden afgesloten met een NULL-waarde. De header begint over het algemeen met een **\x0f** byte en NULL, gevolgd door 4 databytes afgewisseld met NULL's.

### Bestandsstructuur

De structuur van het WDB-bestand wordt hieronder gegeven:
- **1e kop**: vanaf het begin van het bestand, eindigend met \x25\x00\xf2 en 244 NULL-bytes
- **2e kop**: beginnend met \xffT - dwz \xff\x54 en uitgebreid tot 4096 bytes, die kolom-/veldnamen en andere dingen bevat, en lijkt te beginnen op bytepositie 6144.
- **Veld**: waarde heeft een header van 10 byte, met het volgende formaat: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , deel 2} {db 4} \x00. databyte 2 is het veldnummer, databyte 3 is het recordnummer (databyte 3 toevoegen, deel 2 wanneer het meer dan 256 records gaat).


## Referenties ##

* [Gebruiker:JesseW/wdb-formaat](https://en.wikipedia.org/wiki/Gebruiker:JesseW/wdb_format)

