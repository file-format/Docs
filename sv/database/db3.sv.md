{
  "date" : "2019-12-12",
  "keywords" :[ "DB3", "DB3-filformat", "DB3-fil", "SQLite", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DB3-filformat och API:er som kan skapa och öppna DB3-filer.",
  "title" :"DB3-filformat",
  "linktitle" : "DB3",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Vad är en DB3-fil?
DB3-filen är en databasfil skapad av SQLite-programvaran som är ett lättviktigt, fristående databasprogram som skapar databaser med vanliga filer; innehåller databasens anatomi samt dataposter; används ofta för att hämta eller lagra strukturerad data med SQL. Dessa filer kan användas i smarta enheter eller där journalföring eller annan datahantering krävs men i en miljö med lite utrymme.


## DB3 filformat
DB3-filformatet är associerat med RDBMS (Relational Database Management System) SQLite, ett populärt val för inbäddad databas. Det finns ingen specifik filtillägg definierad i en SQLite_3 i dess specifikation, den kan använda tillägg inklusive [.dbf](/sv/database/dbf/) och [.sqlite](/sv/database/sqlite/).

### Databassekifikationen
Vanligtvis kan SQLite, version 3-relaterat db-filformat betraktas som DB3-filformatet som använts som det offentligt dokumenterade inbyggda formatet för SQLite-databasmotorn sedan juni 2004. DB3-filformatet är ett plattformsoberoende, överförbart mellan big-endian och little-endian-arkitekturer eller 32-bitars och 64-bitars system. Dessa funktioner gör DB3 till ett populärt val som programfilformat. Huvudfilen för SQLite_3-databasen (DB3) består av en eller flera sidor. Alla storlekar på alla sidor är lika i samma databas. Sidstorleken i byte är en tvåpotens mellan 512 och 65536 inklusive.



## Referenser ##

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite, version 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)

