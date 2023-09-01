{
  "date" : "2020-01-10",
  "keywords" :[ "otg-fil", "otg-filformat", "vad är en otg-fil", "fil", "otg-exempel", "otg-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument Drawing Template File Format",
  "description":"Läs mer om OTG-filformat och API:er som kan skapa och öppna OTG-filer.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Vad är en OTG fil?

En OTG-fil är en ritmall som skapas med OpenDocument-standarden som följer OASIS Office Applications [1.0-specifikationen](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Det representerar standardorganisationen för ritelement för en vektorbild som kan användas för att ytterligare förbättra innehållet i filen. OTF-filer är som alla andra OpenDocument-formatbaserade filer som är baserade på XML-format för att representera innehållet i dokumentet. OTF-filer kan ses genom att öppna dem i valfri text eller standard XML-redigerare.

## OTG filformatspecifikationer ##

OTG-filformatet är baserat på OpenDocument XML-formatet som har ett väletablerat schema. Strukturen för varje komponent i ett OpenDocument-format representeras av ett element som har associerade attribut och är gemensamt för alla dokumenttyper som textdokument, kalkylblad eller en ritfil. OTG, som är en ritmall, använder i stor utsträckning grafikinnehållsspecifikationerna som inkluderar:

* Förbättrade sidfunktioner för grafiska applikationer
* Rita former
* Ramar
* 3D-former
* Anpassad form
* Presentationsformer
* Presentationsanimationer
* SMIL-presentationsanimationer
* Presentationsevenemang
* Presentera textfält
* Innehåll i presentationsdokument

### Förbättrade sidfunktioner för grafiska applikationer ###
#### Handout Master ####

Handout Master-element är en mall för att automatiskt generera utdelningssidor för applikationer som stöder utskrift av sådana sidor.
Attributen som kan vara associerade med `<style:handout-master>` element är:

|Layout|Attribut|Beskrivning
---|---|---|
|Presentationssidalayout|presentation:presentation-page-layout-name|Länkar till `<style:presentation-page-layout>`  attribut
|Sidlayout|`style:page-layout-name` | Anger en sidlayout som innehåller storlekarna, ramarna och orienteringen för mallsidan för utdelningsmaterialet.
|Sidstil|`draw:style-name`|Tilldelar ytterligare formateringsattribut till en utdelningshuvudsida genom att tilldela en ritsidstil.|
|Rubrikdeklaration| `presentation:use-header-name`| Anger namnet på rubrikfältsdeklarationen som används för alla rubrikfält som visas på utdelningshuvudsidan.
|Sidfotsdeklaration| presentation:use-footer-name|Anger namnet på sidfotsfältsdeklarationen som används för alla sidfotsfält som visas på utdelningshuvudsidan.
|Datum- och tidsdeklaration|use-date-time-name|Anger namnet på datum- och tidfältdeklarationen som används för alla datum-tid-fält som visas på utdelningshuvudsidan.

### Rita former ###
OpenDocument-formatet stöder flera ritformer som kan användas av alla typer av dokument.

|Shape|Associerade attribut| element
---|---|---|
Rektangel - `<draw:rect>` |Position, Storlek, Stil, Lager, Z-index, ID, Bildtext-ID, Textankare, tabellbakgrund, ritslutposition, Runda hörn|Titel, Lång Beskrivning, Händelselyssnare, Limpunkter, Text
Rad `<draw:line> `|Stil, lager, Z-index, ID, bildtext-ID och transformation, textankare, tabellbakgrund, ritslutposition, startpunkt, slutpunkt|titel, lång beskrivning, händelseavlyssnare, limpunkter, text
Polylinje `<draw:polyline> `| Position, Storlek, View box, Style, Layer, Z-Index, ID, Caption ID och Transformation, Textankare, tabellbakgrund, rita slutposition, Points| Titel, lång beskrivning, händelselyssnare, limpunkter, text
Polygon `<draw:polygon> `|Position, Storlek, Visa ruta, Stil, Lager, Z-index, ID, Bildtext ID och Transformation, Textankare, tabellbakgrund, ritslutposition, Points|Titel, Lång beskrivning, Händelselyssnare, Limpunkter, Text
|Vanlig polygon `<draw:regular-polygon> `|Position, storlek, stil, lager, Z-index, ID, bildtext-ID och transformation, textankare, tabellbakgrund, ritslutposition, konkav, hörn, skärpa|titel, lång beskrivning, händelselyssnare, limpunkter, text
|Paht `<draw:path> `|Position, Storlek, View box, Style, Layer, Z-Index, ID, Caption ID och Transformation,Textankare, tabellbakgrund, rita slutposition, Bandata| Titel, lång beskrivning, händelselyssnare, limpunkter, text

### Ramar ###
En ram i ett ritdokument är en rektangulär behållare som innehåller textrutor, bilder eller objekt. Ramar stöder ytterligare funktioner som konturer, bildkartor och hyperlänkar. En ram kan innehålla ett objekt såväl som en bild, vilket gör det möjligt att ha flera återgivningar av ett objekt. Applikationerna återger respektive element baserat på det bästa stödet.

Ramar kan innehålla:
* Textrutor
* Objekt representerade antingen i OpenDocument-formatet eller i ett objektspecifikt binärt format
* Bilder
* Applets
* Plug-ins
* Flytande ramar

En ram finns i ett dokument som visas nedan.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Referenser ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

