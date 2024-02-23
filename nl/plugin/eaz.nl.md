{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ-bestand - Wat is een EAZ-bestand en hoe u dit openen?",
  "description":"Meer informatie over de EAZ-bestandsindeling en API's waarmee EAZ-bestanden kunnen worden gemaakt en geopend.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-nlz"
}
},
  "lastmod" : "2023-12-23"
}

## Wat is een EAZ-bestand?

Het EAZ-bestand is een invoegbestand dat wordt gebruikt door ArcGIS Explorer, een gratis applicatie ontwikkeld door ESRI voor het verkennen, visualiseren en delen van kaarten. Het bevat een gecomprimeerd bestandsarchief met een [XML file](/web/xml/), gecompileerde code en ondersteunende bestanden die nodig zijn voor de invoegtoepassing. Deze bestanden worden gebruikt om de basisfunctionaliteit van de software uit te breiden door nieuwe knoppen, dockbare vensters en andere extensies op te nemen.

## EAZ-bestandsindeling - Meer informatie

EAZ-bestanden worden gemaakt door gebruik te maken van de ArcGIS Explorer SDK, een ontwikkelingskit die is ontworpen voor het creëren van aangepaste functionaliteiten binnen ArcGIS Explorer. Deze bestanden maken gebruik van [ZIP](/compression/zip/)-compressie om hun inhoud efficiënt te verpakken. De kern van het archief wordt gevormd door het **Addins.xml**-bestand, dat zich in de hoofdmap bevindt en fungeert als een essentieel onderdeel dat de verschillende aanpassingen die in het EAZ-bestand zijn ingebed, schetst en detailleert.

Het Addins.xml-bestand fungeert in wezen als een routekaart en biedt inzicht in de specifieke verbeteringen, aanpassingen en uitbreidingen die het EAZ-bestand introduceert in ArcGIS Explorer. Via deze uitgebreide structuur kunnen ontwikkelaars nieuwe functies, knoppen en koppelbare vensters inkapselen en naadloos integreren, waardoor de algehele functionaliteit en gebruikerservaring van de ArcGIS Explorer-applicatie wordt verbeterd.

## Referenties

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
