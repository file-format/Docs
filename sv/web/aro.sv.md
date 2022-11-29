{
  "date" : "2021-12-09",
  "keywords" :[ "aro", ".aro-fil", "aro-filformat", "en filtyp", "fil", "typ", "vad är en .aro-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARO-filformat - SteelArrow Web Application File",
  "description" :"Läs mer om vad en ARO-fil och API:er är som kan skapa och öppna ARO-filer.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Vad är ARO fil?

En ARO-fil är en webbsidesfil på serversidan som genereras med SteelArrow Web Application. Den innehåller [HTML](/sv/web/html/) och SteelArrow-taggar och skript. Dessa exekveras på servern för att generera en komplett svarssida innan de skickas till användarens webbläsare. ARO-filer innehåller nästan 95 % av HTML-innehållet medan resten består av SteelArrow-kod. För att ARO-filer ska fungera för dig bör SteelArrow Web Applications-servern vara installerad och köra på webbserverns dator.

## ARO filformat

ARO-filer är skrivna i HTML-markeringsspråkfil med inbäddad JavaScript-kod och Java-appletar. [SteelArrow-taggar](http://www.steelarrow.com/docs/basics1.aro) är de grundläggande byggstenarna för utveckling av webbsidor. Även om dessa inte ändrar visningen av sidan, används de för att fylla sidan med data. Dessutom kan de också användas för att styra utdata med villkorliga uttalanden.

### Exempel på ARO-tagg

De<SAOUTPUT> ARO-taggen låter utvecklare mata ut datavärden var som helst i ett skript. Till exempel kan den användas för att få utdata från PARAM-tabellen med<SAOUTPUT VALUE=PARAM[]> som kan visas i HTML<BODY> märka.

## Referenser

* [SteelArrow-taggar](http://www.steelarrow.com/docs/basics.aro)

