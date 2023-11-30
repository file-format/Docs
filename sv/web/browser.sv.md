{
  "date" : "2023-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BROWSER File - ASP.NET Browser Definition File Format",
  "description":"Läs mer om BROWSER-filformat och API:er som kan skapa och öppna BROWSER-filer.",
  "linktitle" : "BROWSER",
  "menu" : {
    "docs" : {
      "parent" : "web",
      "identifier": "web-browser"
}
},
  "lastmod" : "22023-06-06"
}

## Vad är en BROWSER-fil?

En fil med tillägget .browser används av ASP.NET-webbapplikationer för att bestämma webbläsares kapacitet och konfiguration. Den innehåller information om webbläsarens möjligheter, begränsningar och egenskaper. Dessa egenskaper hjälper ASP.NET-ramverket att känna igen den begärande webbläsaren och presentera webbsidan för användarna därefter.

## BROWSER Filformat

BROWSER-definitionsfiler används av ASP.NET-applikationen för att fastställa webbläsarens funktioner. Det är informationen i den här filen som används av servern för att generera uppmärkning och andra resurser som är kompatibla med den begärda webbläsaren.

BROWSER-filer sparas i vanligt textfilformat. Du kan öppna en BROWSER-fil i textredigerare som Notepad, Notepad++, Apple TextEdit och Visual Studio IDE.

### Filstruktur för filformatet BROWSER

BROWSER-definitionsfilerna använder en hierarkisk struktur. Varje .browser-fil innehåller en XML-uppmärkning som inkluderar funktionerna och funktionerna för en viss webbläsare eller en grupp webbläsare. Dessa detaljer inkluderar egenskaper som agentsträng, versionsnummer och stöd för teknologier som JavaScript, CSS eller andra HTML-element. Genom att använda dessa webbläsardefinitionsfiler anpassar ASP.NET-utvecklare användarupplevelser baserat på funktionerna hos olika webbläsare.

## Referenser

* [Arbeta med filer på en ASP.NET-webbsidor](https://learn.microsoft.com/en-us/aspnet/web-pages/overview/data/working-with-files)



