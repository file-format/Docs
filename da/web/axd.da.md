{
  "date": "2023-05-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AXD-fil - ASP.NET Web Handler-filformat",
  "description": "Lær om, hvad en AXD-fil og API'er er, der kan oprette og åbne AXD-filer.",
  "linktitle": "AXD",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ax-dad"
}
},
  "lastmod": "2023-05-23"
}

## Hvad er en AXD fil?

En AXD-fil er en webindstillingsfil, der bruges til at håndtere og hente indlejrede ressourceanmodninger i ASP.NET. Den består af instruktioner til at hente indlejrede ressourcer såsom billeder, JavaScript ([.JS](/web/js/)) filer og [.CSS](/web/css/) filer. AXD-filer bruges til at injicere ressourcer på klientsidesider. Dette giver klientsider adgang til disse ressourcer på serveren på en standard måde.

## AXD filformat

AXD-filer gemmes som binære filer på serversiden. Det refererer til en Web Handler-fil i ASP.NET, som er komponenter, der genererer svar på specifikke anmodninger til en webserver. AXD-filer udfører tilpasset behandling, før de genererer svaret baseret på anmodninger om klientsiden. Disse gemmes typisk som **WebResource.axd** filer.

### Hvad er filen WebResource.axd?

De fleste ASP.NET-projekter gemmer AXD-filer som WebResource.axd-filer, der tillader klientsidesider at downloade ressourcer, der er indlejret i en samling. Din applikation kan opleve langsom ydeevne, hvis du kører den i fejlretningstilstand, da WebResources.axd-handleren ikke er cachelagret.

## Referencer

 * [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

