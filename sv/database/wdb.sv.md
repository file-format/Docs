{
  "date" : "2021-08-24",
  "keywords" :[ "wdb-fil", "wdb-filformat", "vad är en wdb-fil", "fil", "wdb-exempel", "wdb-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om WDB-filformat och API:er som kan skapa och öppna WDB-filer.",
  "title" :"WDB - SQL Server Trace File",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Vad är WDB fil?
En fil med filtillägget .wdb är faktiskt en databasfil skapad av Microsoft Works som användes för att utföra funktioner som ett databashanteringssystem. WDB-filen liknar filen Access Database ([MDB](/sv/database/mdb/)), men mindre effektiv och större begränsningar. WDB-filerna kan inte öppnas med hjälp av Microsoft Access. Du kan dock öppna WDB-filen i Microsoft Works och sedan exportera den till MDB-fil, för att öppna en WDB-fil i MS Access.

## WDB filformat
Microsoft Works Database är det ursprungliga databasformatet för Microsoft Works kontorspaket. På grund av formatets proprietära karaktär och vissa begränsningar. WDB-filerna kan inte öppnas i någon annan programvara än Microsoft Works. I filformatet kan en återkommande rubrik på 10 byte hittas före var och en av ASCII-textsträngarna som representerar värdena för fälten som avslutades med ett NULL-värde. Rubriken börjar vanligtvis med en **\x0f** byte och NULL, följt av 4 databyte alternerade med NULL.

### Filstruktur

Strukturen för WDB-filen ges nedan:
- **1st header**: från början av filen, slutar med \x25\x00\xf2 och 244 NULL-byte
- **2nd header**: börjar med \xffT - dvs \xff\x54 och sträcker sig för 4096 byte, som innehåller kolumn-/fältnamn och andra saker, och verkar börja på byteposition 6144.
- **Fält**: värdet har en rubrik på 10 byte, med följande format: {typ byte} {typ byte, del 2} {databyte 1} \x00 {db 2} \x00 {db 3} {db 3 , del 2} {db 4} \x00. databyte 2 är fältnumret, databyte 3 är postnumret (lägger till databyte 3, del 2 när det går över 256 poster).


## Referenser ##

* [Användare:JesseW/wdb format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

