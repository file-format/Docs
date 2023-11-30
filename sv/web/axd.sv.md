{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD File - ASP.NET Web Handler File Format",
  "description" :"Läs mer om vad en AXD-fil och API:er är som kan skapa och öppna AXD-filer.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Vad är en AXD fil?

En AXD-fil är en webbinställningsfil som används för att hantera och hämta inbäddade resursförfrågningar i ASP.NET. Den består av instruktioner för att hämta inbäddade resurser som bilder, JavaScript-filer ([.JS](/sv/web/js/)) och [.CSS](/sv/web/css/)-filer. AXD-filer används för att injicera resurser på klientsidor. Detta tillåter klientsidor att komma åt dessa resurser på servern på ett standard sätt.

## AXD filformat

AXD-filer lagras som binära filer på serversidan. Det hänvisar till en Web Handler-fil i ASP.NET som är komponenter som genererar svar på specifika förfrågningar till en webbserver. AXD-filer utför anpassad bearbetning innan svaret genereras baserat på förfrågningar på klientsidan. Dessa sparas vanligtvis som **WebResource.axd**-filer.

### Vad är filen WebResource.axd?

De flesta ASP.NET-projekt sparar AXD-filer som WebResource.axd-filer som gör att sidor på klientsidan kan ladda ner resurser som är inbäddade i en sammansättning. Din applikation kan möta långsamma prestanda om du kör den i felsökningsläge eftersom WebResources.axd-hanteraren inte är cachad.

## Referenser

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

