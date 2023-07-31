{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "sdf-fil","vad är sdf-fil","hur man öppnar en sdf-fil", "tillägg", "fil", "sdf-filformat", "Databasfiltyp", "Databasfilformat ", "Databasfiler" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om SDF-filformat och API:er som kan skapa och öppna SDF-filer.",
  "title" :"SDF - SQL Server Compact Database File",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Vad är en SDF fil?
En fil med filtillägget .sdf innehåller databasen Microsoft SQL Server Compact (SQL CE) som också är känd som en kompakt relationsdatabas; producerad av Microsoft för de applikationer som är gjorda för mobila enheter och stationära datorer. Den stöder både 32 och 64 bitars operativsystem och hela innehållet i databasen ingår i en enda SDF-fil och kan uppta mer än 4 GB diskutrymme. Av säkerhetsskäl kan en .sdf-fil krypteras med 128-bitars kryptering. SQL CE-runtime reglerar parallell åtkomst för flera användare till .sdf-filen. SDF-filen kan kopieras via **QuickOnce** eller helt enkelt kopieras till destinationen för systemdistribution.

## SDF-filformat
En SDF-fil innehåller en databas som brukar kallas kompakt relationsdatabas. En SDF-fil innehåller all databasrelaterad information och SQL Server Compact är en lättviktig och gratis databasmotor som används för att hantera .sdf-filerna. .sdf-filstorleken bör inte överstiga gränsen på 4 GB. SDF-filerna lagrar inte information om lagrade procedurer, utlösare eller vyer. Applikationer som använder en SQL CE-databas behöver inte ange sökvägen till en SDF-fil i ADO.NET-anslutningssträngen, istället kan den nämnas som |DataDirectory|\databasnamn.sdf, vilket definierar datakatalogen som definieras i sammansättningsmanifestet för applikationen
Namnkonventionen .sdf är valfri och vilken filändelse som helst kan användas för att spara filen. Att ställa in ett lösenord för databasfilen är ett valfritt steg. För att komprimera eller reparera databasen bör filen sparas med alternativet **komprimerad/reparerad databas**.

## Referenser

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Använder SQL Server Compact för ASP.NET-webbapplikationer](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


