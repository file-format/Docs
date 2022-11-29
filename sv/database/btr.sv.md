{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om BTR-filformat och API:er som kan skapa och öppna BTR-filer.",
  "title" :"BTR - Btrieve Database File",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Vad är BTR fil?

En fil med filtillägget .btr är en databasfil skapad av [Btrieve](https://www.actian.com/) transaktionsdatabasapplikation. Till skillnad från relationsdatabashanteringssystem (RBMS) är Btrieve baserat på Indexed Sequential Access Method (ISAM), vilket är ett sätt att lagra data för snabb hämtning. BTR-filen lagrar en samling poster och används för att generera rapporter enligt kraven. BTR-filer kan öppnas med Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility och Legend Software BTRIEVE Viewer.

## BTR-filstruktur - Mer information

Den interna datastrukturen och justeringen av varje byte i strukturen för en BTR-fil är inte allmänt tillgänglig. Men Btrieve
tillhandahåller [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) som kan användas för att läsa informationen från BTR-filer. Den är kompatibel med följande programmeringsspråk och utvecklingsmiljöer.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Att hämta data från en BTR-fil är beroende av den associerade DDF-filen med den. Utan DDF kommer det inte att vara lätt att hämta informationen från en sådan fil.

## Referenser

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Introduktion till Btreive API:er](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

