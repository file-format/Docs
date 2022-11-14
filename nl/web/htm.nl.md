{
  "date" : "2019-10-11",
  "keywords" :[ "htm","htm-bestand", "htm-bestandsformaat", "htm-bestandstype", "bestand", "type", "wat is een htm-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTM-bestandsindeling",
  "description" :"Uw gids voor bestandsindelingen om te leren wat een HTM-bestand is en API's die ze kunnen maken en openen.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een HTM-bestand?

Bestanden met de extensie **.htm** vertegenwoordigen Hypertext Markup Language voor het maken van webpagina's voor weergave in webbrowsers zoals Google Chrome, Internet Explorer, Firefox en een aantal andere. Het definieert de markeringen voor het maken van statische pagina's die op World Wide Web (WWW) moeten worden gepubliceerd voor toegang door anderen. Deze markeringen vertellen de browsers hoe de inhoud van een webpagina moet worden weergegeven. Dergelijke pagina's kunnen platte tekst, afbeeldingen, hyperlinks naar andere pagina's, video's en andere media-informatie bevatten. Wanneer een webpagina is gepubliceerd, kunt u de opmaakcode erachter bekijken door de paginabron te bekijken. Moderne browsers maken het mogelijk om elke sectie van een webpagina te inspecteren waar elke onderverdeling of opmaakelement in de HTM-bron is uitgewerkt.

## Korte geschiedenis van HTM

Sinds het begin en de eerste uitrol, worden de HTML-specificaties sinds 1996 onderhouden door World Wide Web Consortium (W3C). In 2000 werd het ook een internationale standaard (ISO/IEC 15445:2000). In 1999 werd HTML 4.01 gepubliceerd. In 2004 begon de Web Hypertext Application Technology Working Group (WHATWG) te werken aan de HTML5-versie, die in 2008 samen met het W3C werd geleverd. Het werd voltooid en gestandaardiseerd op 28 oktober 2014.

## HTML-bestandsindeling

Een HTML 4-document bestaat uit drie delen:

1. een regel met informatie over de HTML-versie
1. een declaratieve koptekst
1. een body die de feitelijke inhoud van het document bevat. De body kan worden geïmplementeerd door het BODY-element of het FRAMESET-element om de body in frames te bevatten

Elke sectie kan worden voorafgegaan of gevolgd door spaties, nieuwe regels, tabbladen en opmerkingen. Hieronder ziet u een voorbeeld van een eenvoudig HTML-document:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Versie informatie

De eerste regel code,<!DOCTYPE html> , wordt een doctype-declaratie genoemd en vertelt de browser in welke versie van HTML de pagina is geschreven. Afhankelijk van de versie van HTML zijn er een aantal verschillende doctype-declaraties die de documenttypedefinitie (DTD) noemen die voor het document wordt gebruikt. Elke DTD verschilt van andere in de elementen die het ondersteunt en verschilt als volgt:

* HTML 4.01 Strict - bevat alle elementen en attributen die niet [verouderd](https://www.w3.org/TR/html401/conform.html#deprecated) of niet voorkomen in frameset-documenten
* HTML 4.01 Transitional - bevat alles in de strikte DTD plus verouderde elementen en attributen (waarvan de meeste betrekking hebben op visuele presentatie
* HTML 4.01 Frameset - bevat ook alles in de tijdelijke DTD plus-frames

Voor **HTML5** is de versie-informatie eenvoudig zoals hieronder vermeld.

```
<!DOCTYPE html>
```

### Koptekstinformatie

De koptekst van een HTML-document kan een aantal HTML-elementen bevatten die niet door de browser worden weergegeven. Dergelijke elementen zijn ofwel metadata die informatie over de pagina beschrijven of bevatten secties die worden gebruikt om informatie op te halen van externe bronnen zoals CSS-stylesheets of JavaScript-bestanden. De kop van een pagina wordt weergegeven door \<head> tag en eindigt met \</head> label.

<html>Voor het instellen van de paginatitel, de \<title> element is het enige dat vereist is binnen de \<head>-tags. Hetzelfde wordt door zoekmachines gebruikt om de titel van een pagina te identificeren. </html>

### Lichaamsinformatie

Dit is het hoofdgedeelte van het bestand dat alle inhoud van het bestand bevat die door browsers wordt weergegeven. Html body kan markeringen bevatten die kunnen verwijzen naar verschillende bouwstenen in de vorm van tags. Het kan verschillende soorten informatie bevatten, zoals tekst, afbeeldingen, kleuren, afbeeldingen, enz. Daarnaast kunnen audio- en video-elementen ook worden ingebed in html-body voor weergave door browsers. In aanwezigheid van moderne stylesheets-applicatie voor visuele representatie, zijn de presentatie-attributen van BODY zoals achtergrondkleur, linkkleur, tekstkleur, enz. verouderd. Dezelfde effecten kunnen dus worden bereikt met behulp van stylesheets zoals hieronder weergegeven:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Inline-stylesheets zijn eenvoudig in te sluiten en voor snelle toepassingen van de visuele effecten maken externe stylesheets het gemakkelijker om eenmalig te implementeren en op veel plaatsen te openen.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML-elementen

Zoals eerder vermeld, wordt inhoud in HTML Body weergegeven door tags, ook wel bekend als Html-elementen. Elke tag kan aanvullende informatie hebben in de vorm van attributen die worden geschreven als
```
<tag attribute1#"value1" attribute2#"value2">
```
hoewel het niet nodig is om bij elke tag attributen te hebben. Als attributen niet worden vermeld, worden in elk geval standaardwaarden gebruikt. Hieronder volgen enkele voorbeelden van elementen:

#### Koptekst

```
<head>
  <title>The Title</title>
</head>
```

#### Koppen

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Alinea's

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Referenties

* [De globale structuur van het HTML-document](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

