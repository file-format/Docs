{
  "date" : "2019-10-11",
  "keywords" :[ "asp","asp-fil", "asp-filformat", "asp-filtyp", "fil", "typ", "vad är en asp-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Active Server Pages File Format",
  "description" :"Läs mer om vad som är en ASP-fil och API:er som kan skapa och öppna dem.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en ASP-fil?

ASP står för Active Server Pages som är ett utvecklingsramverk för att skapa webbsidor. Det gör att datorkod kan exekveras av en intern server för att betjäna webbförfrågningarna. När en begäran genereras för en ASP-fil av webbläsaren, läser servern filen och exekverar kod/skript inuti den för att generera resultatet **[HTML](/sv/web/html/)** som returneras till webbläsare för visning.

Till skillnad från HTML-sidor, som är statiska sidor som serveras, genererar ASP-filer dynamiskt innehåll vid körning som kan involvera förfrågningar till data från en databas. ASP-sidor använder vanligtvis tillägget .asp snarare än .html. Eftersom kod/skript inuti en ASP-fil körs på serversidan, kan den begärda webbläsaren inte se koden som används för att bygga den serverade sidan. Alla moderna webbläsare kan visa sidor som genereras som resultat. Sidor byggda med ASP är byggda på Microsoft-teknik och lagras på Microsoft Internet Information Services (IIS)-servrar.

## Kort historik om ASP-filformat
ASP har gått igenom några få revisioner och det ersattes av ASP.NET som är ett modernare och mer effektivt sätt att utveckla och hantera serversidor. Stöd för ASP ingår som standard tillsammans med Internet Information Services (IIS). ASP publicerades i tre olika versioner med förbättringar i var och en.

* ASP 1.0 släpptes i december 1996 som en del av IIS 3.0
* ASP 2.0 släpptes i september 1997 som en del av IIS 4.0
* ASP 3.0 släpptes i november 2000 som en del av IIS 5.0

## ASP funktionella objekt

ASP-filer använder objekt på serversidan för att behandla användarförfrågningar och generera utdatasidor som ska visas för användare. Varje objekt har en uppsättning samlingar, egenskaper och metoder för att behandla förfrågningar och svar. Dessa objekt inkluderar:

### Begär objekt

När en webbläsare frågar efter en sida från en server kallas det en begäran. Objektet Request används för att få information från en besökare.

### Svarsobjekt

ASP Response-objektet används för att skicka utdata till användaren från servern.

### Serverobjekt

ASP Server-objektet används för att komma åt egenskaper och metoder på servern. Det tillåter anslutningar till databaser (ADO), filsystem och användning av komponenter installerade på servern.

### Sessionsobjekt

Ett sessionsobjekt är som en länk mellan användarens webbläsare som begär en sida från servern och själva servern. Detta uppnås genom en cookie som skapas av ASP och skickas till användarens dator. Sessionsobjektet lagrar information om eller ändrar inställningar för en användarsession. Information som lagras i ett sessionsobjekt delas över alla sidor i en applikation. Vanlig information som lagras i sessionsvariabler är namn, id och preferenser. Servern skapar ett nytt Session-objekt för varje ny användare och förstör Session-objektet när sessionen löper ut.

### Application Object

Application-objektet innehåller information som kommer att användas av många sidor i programmet (som databasanslutningsinformation). Informationen kan nås från vilken sida som helst. Informationen kan också ändras på ett ställe, och ändringarna kommer automatiskt att återspeglas på alla sidor. Applikationsobjektet används för att lagra och komma åt variabler från vilken sida som helst, precis som Session-objektet.

### ASPError Object

ASPError-objektet implementerades i ASP 3.0 och är tillgängligt i IIS5 och senare. ASPError-objektet används för att visa detaljerad information om eventuella fel som uppstår i skript på en ASP-sida.

**Obs!** ASPError-objektet skapas när Server.GetLastError anropas, så felinformationen kan endast nås med metoden Server.GetLastError.

## Referenser

* [ASP – av W3C](https://www.w3schools.com/asp/default.asp)
* [Skapa enkla ASP-sidor](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

