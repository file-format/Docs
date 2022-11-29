{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","asmx-fil", "asmx-filformat", "asmx-filtyp", "fil", "typ", "vad är en asmx-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET Web Service File",
  "description" :"Läs mer om vad som är en ASMX-fil och API:er som kan skapa och öppna ASMX-filer.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Vad är en ASMX fil?

En fil med .asmx-tillägg är en ASP.NET Web Service-fil som tillhandahåller kommunikation mellan två objekt över internet med hjälp av Simple Object Access Protocol (SOAP). Den distribueras som en tjänst på den Windows-baserade webbservern för att behandla inkommande förfrågan och returnera svaret. Till skillnad från [ASPX](/sv/web/aspx/)-filer som innehåller koden för visuell visning av ASP.NET-webbsidor, körs ASMX-filer på servern i bakgrunden och utför olika uppgifter som att ansluta till databasen, hämta data och returnera den i ett format som begäran gjordes i. Dessa används specifikt för XML-webbtjänster.

## ASMX filformat

ASMX-filer är i vanligt textformat och kan öppnas eller redigeras i applikationer som Microsoft Visual Studio eller textredigerare. Det är ett proprietärt filformat från Microsoft och har en väldefinierad syntax för att skapa webbtjänster. Ett svar från en ASMX-fil i form av SOAP XML har följande element.

* `Envelop` - Ett rotelement som identifierar XML-dokumentet som ett SOAP-meddelande.
* `Header` - Ett valfritt element som innehåller programspecifik information som autentiseringsdata. Om Header-elementet finns måste det vara det första underordnade elementet i Envelope-elementet.
* `Body` - Innehåller SOAP-meddelandet avsett för mottagaren.
* `Fel` - Ett valfritt element som används för att indikera felmeddelanden. Om Fault-elementet finns måste det vara ett underordnat element till Body-elementet.

ASMX-filer kan skrivas på .NET-språk som [C#](/sv/programming/cs/), [Visual Basic](/sv/programming/vb/) eller JScript.

## Hur skiljer sig ASMX från ASPX och ASCX?

ASMX-filer skiljer sig från ASPX- och ASCX-filer.

* ASPX, Active Server Pages, filer är programmeringsfiler som genereras med hjälp av Microsoft ASP.NET-ramverket som körs på webbservrar. Dessa återges i klientens webbläsare när användaren begär att få tillgång till en sådan sida.
* ASCX, Active Server User Control, definierar användarkontroller som används för att definiera återanvändbara kontroller på ASP.NET-webbsidor eller hela webbplatsen.

## Referenser

* [konsumerar ASMX-tjänst](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX User Control](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

