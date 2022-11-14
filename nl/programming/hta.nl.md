{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "bestand", "extensie", "bestandsindeling", "hta-implementatie", "Programmeergids", "hta-voorbeeld", "HTML-toepassing", "Hypertext Markup Language-toepassing", "HTA-bestanden", "Microsoft HTML-toepassing"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - HTML-toepassingsbestanden",
  "description":"Meer informatie over HTA-bestandsindeling en API's die HTA-bestanden kunnen maken en openen.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Wat is een HTA-bestand?

De HTMLA staat voor **Hypertext Markup Language Application** is een programma dat compatibel is met Microsoft Windows. De broncode van dit programma bevat meer dan één scripttaal, zoals [HTML](/nl/web/html/) en [JavaScript](/nl/web/js/). Voor de gebruikersinterface heeft een HTML-toepassing de voorkeur, terwijl om aan de eisen van programmalogica te voldoen elke andere scripttaal wordt gebruikt.

Een HTML Applicatie is onafhankelijk van het beveiligingsmodel van de internetbrowser en draait als een volledig vertrouwde applicatie. De extensie die wordt gebruikt voor bestanden met betrekking tot deze toepassingen is HTA. Deze toepassingen bevatten functies van HTML samen met de eigenschappen van andere scripttalen.


## Korte geschiedenis ##

De HTA werd voor het eerst geïntroduceerd in 1999 door Microsoft samen met de release van Internet Explorer 5. Het was compatibel met Internet Explorer en kon dus alleen worden uitgevoerd op het Windows-besturingssysteem. Deze technologie is in 2003 gepatenteerd. De HTA-bestanden worden uitgevoerd zoals alle andere .exe-bestanden. De HTA-bestanden zijn ook compatibel met de huidige bijgewerkte versie van Windows 11.


## Technische specificatie ##

HTA's hebben hetzelfde formaat als elke andere HTML-pagina, terwijl sommige attributen worden gebruikt voor het beheren van de stijlen van randen of pictogrammen van programma's. Bovendien worden argumenten gegeven voor de lancering van HTA. Deze toepassingen kunnen worden uitgevoerd met een programma met de naam mshta.exe. Het kan worden geopend door eenvoudig op het bestand te dubbelklikken. Deze programma's draaien automatisch mee met de Internet Explorer. Naast andere specificaties zijn deze niet onafhankelijk van de Trident engine browser, maar onafhankelijk van Internet Explorer. Dit betekent dat deze kunnen worden uitgevoerd zonder Internet Explorer te gebruiken.

De tags worden gebruikt om het uiterlijk van deze applicaties aan te passen. De conversie van Microsoft HTML-toepassing naar HTA-indeling is eenvoudiger, dwz u hoeft alleen de extensie te wijzigen. Omdat we weten dat deze applicaties volledig vertrouwd zijn, bevatten deze meer functies en voordelen in vergelijking met eenvoudige HTML-bestanden. Teksteditors kunnen worden gebruikt om HTA te maken. Deze editors kunnen worden verkregen door Microsoft of een andere vertrouwde bron.


## Voorbeeld HTA-bestandsindeling ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Referentie ##

* [HTA - door Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)



