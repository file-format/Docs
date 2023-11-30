{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MASTER File - ASP.NET Master Page File Format",
  "description" :"Läs mer om MASTER-filformat och API:er för att skapa och öppna MASTER-filer.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Vad är en MASTER fil?

En MASTER-fil är en mallfil för huvudwebbsidor skapad med ASP.NET. Den används som utgångspunkt för att skapa flera sidor som har samma layout och inställningar som MASTER-filen. Mallen MASTER-filen innehåller inställningar för sidhuvud, navigeringsmenyer, sidfot, teckensnitt och stilinformation. Att använda en MASTER-fil hjälper till att skapa flera webbsidor snabbt.

Du kan öppna en MASTER-fil med Microsoft Visual Studio 2022 och högre.

## MASTER-filformat - Mer information

En MASTER-fil skapas och sparas i HTML-filformat och liknar alla andra webbsidesfiler. Den är uppdelad i redigerbara och icke-redigerbara sektioner. De redigerbara avsnitten är de som kan modifieras för att möta användarens krav. De icke-redigerbara avsnitten är nedtonade när MASTER-filen öppnas i Microsoft Visual Studio.

Master Pages består av två delar, dvs själva mastersidan och en eller flera innehållssidor.

### MASTER Page

Huvudsidan har tillägget .master och är gjord i ASP.NET. Den har en fördefinierad layout som består av statisk text, HTML-taggar och kontroller på serversidan. På vanliga .aspx-sidor används @ Page-direktivet. I fallet med .master-filer ersätts detta av @ Master-direktivet.

### Innehållssidor

En innehållssida representerar innehållet för mallsidans platshållarkontroller. Dessa är .aspx-sidor som faktiskt är koden bakom huvudsidan. Innehållssidor binds med @ Page-direktivet genom att inkludera ett MasterPageFile-attribut som pekar på huvudsidan som ska användas enligt nedan.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Referenser

* [ASP.NET Master Pages Översikt](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

