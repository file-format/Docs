{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD-bestand - ASP.NET Web Handler-bestandsformaat",
  "description" :"Leer meer over wat een AXD-bestand is en API's die AXD-bestanden kunnen maken en openen.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Wat is een AXD-bestand?

Een AXD-bestand is een webinstellingenbestand dat wordt gebruikt voor het afhandelen en ophalen van ingebedde bronaanvragen in ASP.NET. Het bevat instructies voor het ophalen van ingebedde bronnen zoals afbeeldingen, JavaScript-bestanden ([.JS](/nl/web/js/)) en [.CSS](/nl/web/css/)-bestanden. AXD-bestanden worden gebruikt voor het injecteren van bronnen in pagina's aan de clientzijde. Hierdoor hebben clientpagina's op een standaard manier toegang tot deze bronnen op de server.

## AXD-bestandsindeling

AXD-bestanden worden aan de serverzijde opgeslagen als binaire bestanden. Het verwijst naar een Web Handler-bestand in ASP.NET, dit zijn componenten die antwoorden genereren op specifieke verzoeken aan een webserver. AXD-bestanden voeren aangepaste verwerking uit voordat het antwoord wordt gegenereerd op basis van paginaverzoeken aan de clientzijde. Deze worden doorgaans opgeslagen als **WebResource.axd**-bestanden.

### Wat is het WebResource.axd-bestand?

De meeste ASP.NET-projecten slaan AXD-bestanden op als WebResource.axd-bestanden waarmee pagina's aan de clientzijde bronnen kunnen downloaden die zijn ingebed in een assembly. Uw toepassing kan trage prestaties ondervinden als u deze in de foutopsporingsmodus uitvoert, omdat de WebResources.axd-handler niet in de cache is opgeslagen.

## Referenties

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

