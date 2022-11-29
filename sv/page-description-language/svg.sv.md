{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "fil", "filformat", "Sidbeskrivningsspråk", "Skalär" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om SVG-filformat och API:er som kan skapa och öppna SVG-filer.",
  "title" :"Vad är en SVG-fil?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Vad är SVG-fil? ##

En SVG-fil är en Scalar Vector Graphics-fil som använder XML-baserat textformat för att beskriva utseendet på en bild. Ordet Scalable syftar på det faktum att SVG kan skalas till olika storlekar utan att förlora någon kvalitet. Textbaserad beskrivning av sådana filer gör dem oberoende av upplösning. Det är ett av de mest använda formaten för att bygga en webbplats och skriva ut grafik för att uppnå skalbarhet. Formatet kan dock endast användas för tvådimensionell grafik. SVG-filer kan ses/öppnas i nästan alla moderna webbläsare inklusive Chrome, Internet Explorer, Firefox och Safari.

## Kortfattad bakgrund ##

SVG-specifikationer finns tillgängliga som öppen standard av World Wide Web Consortium (W3C) sedan 1999. Dessförinnan skickades liknande filformatspecifikationer i sex olika format till W3C fram till 1998. En uppdatering tillämpades på specifikationerna 2011 och den var version 1.1 . Under 2016 publicerades SVG 2 som en nyare version inklusive funktioner utöver de i SVG 1.1.

## Filformatspecifikationer ##

SVG Document Object Model (DOM) lägger grunden för alla specifikationer och gränssnitt som motsvarar de specifika avsnitten i specifikationerna. SVG-tittare måste implementera SVG DOM-gränssnitten enligt definitionen i W3C-specifikationerna. Dess DOM exponerar flera gränssnitt för olika datatyper och element.

### SVG-former ###

SVG har några fördefinierade formelement som kan användas av utvecklare:

* Rektangel<rect>
* Cirkel<circle>
* Ellips<ellipse>
* Linje<line>
* Polylinje<polyline>
* Polygon<polygon>
* Väg<path>

Baserat på dessa former och specifikationer är SVG:s funktionsområden följande.

**Bvägar** - Banor används för att representera enkla såväl som sammansatta konturer. Kodningar används för att definiera verksamhetens karaktär. Till exempel används M för Flytta till, L används för Linje till, Z används för att stänga en bana och så vidare.

**Grundläggande former** - Raka linjer och banor som består av en serie sammankopplade rätlinjesegment (polylinjer), såväl som slutna polygoner, cirklar och ellipser kan ritas. Rektanglar och rektanglar med runda hörn är också standardelement.

**Text** - Textrepresentation uttrycks som XML-teckendata där många visuella effekter kan appliceras på texten. Specifikationerna gör det möjligt att hantera dubbelriktad text, vertikal text och tecken längs en krökt bana.

**Målning** - Former kan fyllas och/eller kontureras med en färg, en gradient eller ett mönster, vilket gör det möjligt att göra det ogenomskinligt eller ha någon grad av transparens. Linjeändefunktioner som pilspetsar eller symboler som visas i hörnen på en polygon representeras av markörer.

**Färg** - SVG-specifikationer gör det möjligt att applicera färger på alla synliga SVG-element, antingen direkt eller via fyllning, streck och andra egenskaper. Olika färgkoder kan användas för att specificera som svart eller blått, hex-representation, decimal eller som procent av formen RGB.

**Gradienter och mönster** - Former i en SVG-fil kan fyllas eller kontureras med enfärgade färger, övertoningar eller upprepade mönster.

**Filtereffekter** - Det är faktiskt en serie grafikoperationer som tillämpas på given källvektorgrafik för att producera modifierade resultat.

**Interaktivitet** - Användare kan interagera med SVG-filer genom att ändra fokus, musklick, rulla eller zooma bilden. Interaktiviteten låter SVG-bilder interagera med användare på många olika sätt som tidigare nämnts.

**Länkar** - Det är möjligt för SVG-bilder att ha hyperlänkar till andra dokument. Detta uppnås via XML Linking Language eller XLink. Detta gör det möjligt att skapa specifika vytillstånd som används för att zooma in/ut i ett specifikt område eller för att begränsa vyn till ett specifikt element.

**Skript** - I likhet med HTML är alla aspekter av ett SVG-dokument tillgängliga för manipulering med skript. SVG DOM-objekten ger vägledning för att uppnå detta med SVG-element och -attribut. Skript är inneslutna i "script"-taggelement och kan köras som svar på pekare, tangentbord eller dokumenthändelser efter behov.

**Animation** - DOM-elementen<animate> ,<animateMotion> och<animateColor> låter dig inkludera animering för SVG-innehåll. Naturligtvis är detta inte möjligt utan att använda skript och inbyggda timers. Dessa animationer kan vara kontinuerliga och kan sättas i loop såväl som upprepningar samtidigt som de svarar på användarhändelser.

**Teckensnitt** - Text i SVG kan referera till externa teckensnittsfiler som systemteckensnitt. I avsaknad av sådana typsnitt kommer text i SVG inte att återges till utdata. Detta kan övervinnas genom att införliva de nödvändiga glyferna i en sådan fil som ett teckensnitt som sedan renderas med hjälp av<text> element.

## Exempel ##
Följande rader visar hur en cirkel representeras med SVG-skriptet.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Följande kodrader visar hur du använder<text> block för att rendera text till SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referenser ##

* [W3C SVG-specifikationer](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

