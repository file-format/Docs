{
  "date" : "2019-10-11",
  "keywords" :[ "chm","chm file", "chm file format", "chm file type", "file", "type", "wat is een chm file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - Gecompileerde HTML Help-bestandsindeling",
  "description" :"Meer informatie over wat een CHM-bestand is en API's die ze kunnen maken en openen.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een CHM-bestand?

De CHM-bestandsindeling vertegenwoordigt Microsoft **[HTML](/nl/web/html/)** helpbestand dat bestaat uit een verzameling HTML-pagina's. Het biedt een index voor snelle toegang tot de onderwerpen en navigatie naar verschillende delen van het helpdocument. Het CHM-bestand kan worden doorzocht op inhoud via de meegeleverde zoekoptie. CHM is een eigen online helpbestandsindeling van Microsoft die vaak wordt gebruikt voor softwaredocumentatie. Bovendien wordt het gebruikt in verschillende andere toepassingen, zoals trainingsgidsen, interactieve boeken en elektronische nieuwsbrieven. De meeste moderne ontwikkelomgevingen van Microsoft ondersteunen het genereren van CHM-documentatie op basis van informatie die beschikbaar is in de toepassing.

Het unieke vermogen van het CHM-bestandsformaat om een gecombineerde inhoudsopgave en index te implementeren, maakt het anders dan andere standaard HTML-pagina's. Het gegenereerde CHM-bestand is relatief klein en kan daarom gemakkelijk met softwarepakketten worden gedistribueerd. Het hulpmiddel voor het maken van hulp, HTML Help Workshop, biedt een gebruiksvriendelijk systeem voor het maken en beheren van hulpprojecten en de bijbehorende bestanden. CHM-bestanden kunnen tekst, afbeeldingen en hyperlinks bevatten; zichtbaar in een webbrowser; gebruikt door Windows en andere programma's als een online help-oplossing.

## CHM-bestandsindeling

De uiteindelijke vorm van het gegenereerde CHM-bestand hangt af van hoe het helpsysteem is ontworpen en of het bestemd is voor een toepassing of een website. Een CHM-bestand ondersteunt gegevenscompressie met LZX-compressie om de gecomprimeerde HTML-bestanden te genereren. Het heeft de ingebouwde zoekmachine voor het snel doorzoeken van inhoud en de mogelijkheid om meerdere .CHM-bestanden samen te voegen. Een CHM-bestand bestaat uit een set HTML-bestanden, een gekoppelde inhoudsopgave en een indexbestand.

### HTML-bestanden

Of u nu Help-onderwerpen maakt voor distributie met een programma of op het web, de documenten die u schrijft, worden gemaakt met behulp van een speciale opmaaktaal die bekend staat als Hypertext Markup Language (HTML). HTML-onderwerpbestanden hebben de bestandsnaamextensie .htm of .html.

Hoewel elk Help-onderwerp of elke webpagina die u schrijft een document lijkt te zijn met tekst, afbeeldingen of bewegende afbeeldingen erop, zijn .htm-bestanden eigenlijk tekstdocumenten met speciale HTML-opmaakcodes. Deze codes, tags genoemd, vertellen een browser hoe elke pagina moet worden weergegeven. Alleen de tekst die in een onderwerp of webpagina verschijnt, staat ook daadwerkelijk in het .htm-bestand. Alle afbeeldingen, geluiden, geanimeerde afbeeldingen of andere elementen die verschijnen, zijn afzonderlijke bestanden waarnaar uw HTML-bestand verwijst. De browser kopieert of downloadt de afbeeldingen, geluiden of andere elementen wanneer hij de tags ziet die hem dit vertellen.

### Inhoudsopgave (TOC)
Het Help-inhoudsopgave-bestand (.hhc) is een HTML-bestand dat de onderwerptitels voor uw inhoudsopgave bevat. Wanneer een gebruiker de inhoudsopgave opent in een gecompileerd helpbestand (of op een webpagina) en op een onderwerptitel klikt, wordt het HTML-bestand dat bij die titel hoort, geopend.

### Indexbestand
Het indexbestand (.hhk) is een HTML-bestand dat de indexitems (trefwoorden) voor uw index bevat. Wanneer een gebruiker de index opent in een gecompileerd helpbestand, of op een webpagina, en op een trefwoord klikt, wordt het HTML-bestand dat bij het trefwoord hoort, geopend.

## HTML Help-componenten

HTML Help bestaat uit verschillende componenten. Deze omvatten het volgende:

* `HTML Help Workshop`: een hulpmiddel voor het maken van hulp met een gebruiksvriendelijke grafische interface voor het maken van projectbestanden, HTML-onderwerpbestanden, inhoudsbestanden, indexbestanden en al het andere dat u nodig hebt om een online helpsysteem of website samen te stellen .
* `HTML Help ActiveX-besturingselement`: een klein, modulair programma dat wordt gebruikt om Help-navigatie en secundaire vensterfunctionaliteit in een HTML-bestand in te voegen.
* `The HTML Help Viewer`: een volledig functioneel en aanpasbaar venster met drie panelen waarin online helponderwerpen kunnen verschijnen.
* `Microsoft HTML Help Image Editor`: een online grafisch hulpmiddel voor het maken van schermafbeeldingen; en voor het converteren, bewerken en bekijken van afbeeldingsbestanden.
* `The HTML Help Java Applet`: een klein, op Java gebaseerd programma dat kan worden gebruikt in plaats van een ActiveX-besturingselement om Help-navigatie in een HTML-bestand in te voegen.
* `Het uitvoerbare programma HTML Help`: het programma dat Help weergeeft en uitvoert wanneer u op een gecompileerd Help-bestand klikt.
* `De HTML Help compiler`: het programma dat project, inhoud, index, onderwerp en andere bestanden compileert tot een gecompileerd helpbestand.
* `The HTML Help Authoring Guide`: een online gids die is ontworpen om auteurs te helpen bij het gebruik van HTML Help bij het ontwerpen van een helpsysteem. De gids bevat ook een volledige HTML Help-referentie voor ontwikkelaars en een HTML-tagreferentie voor auteurs.

## Referenties

* [Microsoft HTML Help](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

