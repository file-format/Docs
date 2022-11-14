{
  "date" : "2019-10-11",
  "keywords" :[ "asp","asp-bestand", "asp-bestandsformaat", "asp-bestandstype", "bestand", "type", "wat is een asp-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Active Server Pages-bestandsindeling",
  "description" :"Meer informatie over wat een ASP-bestand is en API's die ze kunnen maken en openen.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een ASP-bestand?

ASP staat voor Active Server Pages, een ontwikkelraamwerk voor het maken van webpagina's. Hiermee kan computercode worden uitgevoerd door een interne server om de webverzoeken te verwerken. Wanneer een verzoek wordt gegenereerd voor een ASP-bestand door een webbrowser, leest de server het bestand en voert elke code/script erin uit om het **[HTML](/nl/web/html/)** resultaat te genereren dat wordt geretourneerd naar de browser voor weergave.

In tegenstelling tot HTML-pagina's, die statische pagina's zijn die door de server worden bediend, genereren ASP-bestanden tijdens runtime dynamische inhoud waarbij mogelijk gegevens uit een database worden opgevraagd. ASP-pagina's gebruiken meestal de .asp-extensie in plaats van .html. Aangezien code/script in een ASP-bestand aan de serverzijde wordt uitgevoerd, kan de verzoekende browser de code die is gebruikt om de weergegeven pagina te bouwen niet zien. Alle moderne browsers kunnen pagina's weergeven die als resultaat zijn gegenereerd. Omdat ze zijn gebouwd op Microsoft-technologie, worden pagina's die met ASP zijn gemaakt, gehost op Microsoft Internet Information Services (IIS)-servers.

## Korte geschiedenis van ASP-bestandsindeling
ASP heeft slechts enkele revisies ondergaan, maar werd vervangen door ASP.NET, wat een modernere en efficiëntere manier is om pagina's aan de serverzijde te ontwikkelen en te beheren. Ondersteuning voor ASP is standaard inbegrepen, samen met Internet Information Services (IIS). ASP werd gepubliceerd in drie verschillende versies met verbeteringen in elke versie.

* ASP 1.0 werd uitgebracht in december 1996 als onderdeel van IIS 3.0
* ASP 2.0 werd in september 1997 uitgebracht als onderdeel van IIS 4.0
* ASP 3.0 werd in november 2000 uitgebracht als onderdeel van IIS 5.0

## ASP-functionele objecten

ASP-bestanden gebruiken server-side-objecten om gebruikersverzoeken te verwerken en uitvoerpagina's te genereren die aan gebruikers worden aangeboden. Elk object heeft een reeks verzamelingen, eigenschappen en methoden voor het verwerken van verzoeken en antwoorden. Deze objecten zijn onder meer:

### Object aanvragen

Wanneer een browser om een pagina van een server vraagt, wordt dit een verzoek genoemd. Het Request-object wordt gebruikt om informatie van een bezoeker te krijgen.

### Responsobject

Het ASP Response-object wordt gebruikt om uitvoer vanaf de server naar de gebruiker te sturen.

### Serverobject

Het ASP Server-object wordt gebruikt om toegang te krijgen tot eigenschappen en methoden op de server. Het staat verbindingen toe met databases (ADO), bestandssysteem en het gebruik van componenten die op de server zijn geïnstalleerd.

### Sessie-object

Een sessie-object is als een koppeling tussen de browser van de gebruiker die een pagina van de server opvraagt en de server zelf. Dit wordt bereikt door een cookie gemaakt door ASP en verzonden naar de computer van de gebruiker. Het Session-object slaat informatie op over of wijzigt instellingen voor een gebruikerssessie. Informatie wordt opgeslagen in een Session-object en wordt gedeeld over alle pagina's van een applicatie. Algemene informatie die is opgeslagen in sessievariabelen zijn naam, id en voorkeuren. De server maakt een nieuw Session-object voor elke nieuwe gebruiker en vernietigt het Session-object wanneer de sessie verloopt.

### Toepassingsobject

Het toepassingsobject bevat informatie die door veel pagina's in de toepassing zal worden gebruikt (zoals gegevens over de databaseverbinding). De informatie is vanaf elke pagina toegankelijk. De informatie kan ook op één plek worden gewijzigd en de wijzigingen worden automatisch op alle pagina's weergegeven. Het Application-object wordt gebruikt om variabelen vanaf elke pagina op te slaan en te openen, net als het Session-object.

### ASPE-foutobject

Het ASPError-object is geïmplementeerd in ASP 3.0 en is beschikbaar in IIS5 en hoger. Het ASPError-object wordt gebruikt om gedetailleerde informatie weer te geven over fouten die optreden in scripts op een ASP-pagina.

**Opmerking:** Het ASPError-object wordt gemaakt wanneer Server.GetLastError wordt aangeroepen, dus de foutinformatie is alleen toegankelijk met behulp van de Server.GetLastError-methode.

## Referenties

* [ASP - Door W3C](https://www.w3schools.com/asp/default.asp)
* [Eenvoudige ASP-pagina's maken](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

