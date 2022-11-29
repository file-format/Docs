{
  "date" : "2021-09-06",
  "keywords" :[ "adp", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Åtkomstprojekt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om ADP-filformat och API:er som kan skapa och öppna ADP-filer.",
  "title" :"ADP - Access Database File",
  "linktitle" : "ADP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Vad är en ADP fil?

En fil med .adp-tillägget är en Microsoft Access-projektfil som använder OLE DB-komponentarkitektur för att tillhandahålla en direkt och effektiv anslutning till en Microsoft SQL Server-databas. Sådana filer innehåller inte de faktiska tabellerna, databasdiagrammen eller andra databaselement. ADP-filer kan skapas med Access 2007 och 2010. Filer skapade med de tidigare versionerna av Access kan också öppnas Access 2007 och 2010. ADP-filer kan öppnas med Microsoft Access 365.

## ADP-filformat - Mer information

Ett Access-projekt skapat som ADP låter dig göra designändringar i SQL-serverobjekt som tabeller och vyer. Det gör det också möjligt att skapa, redigera och använda SQL-funktioner som databasdiagram, lagrade procedurer och användardefinierade funktioner. Detta ger fördelar jämfört med att länka till en SQL-serverdatabas där du inte kan göra ändringar i designen och bara kan länka till SQL-servertabeller och vyer.

### Datatyper och diagramstöd

**Data-/tiddatatyper**

Följande nya datatyper för datum/tid stöds i Access 2010.

* TID
* DATUM
* DATUM TID2
* DATETIMEOFFSET

**Datatyper med variabel längd**

Följande datatyper med variabel längd kan användas i Access 2010-projekt:

* VARBIN(MAX)
* VARCHAR(MAX)
* NVARCHAR(MAX)

## Referenser

* [Skapa ett Access-projekt](https://support.microsoft.com/en-us/office/create-an-access-project-89c48da0-55a4-45d4-9ee5-95f67383d4cb)

