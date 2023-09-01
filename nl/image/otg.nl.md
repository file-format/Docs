{
  "date" : "2020-01-10",
  "keywords" :[ "otg-bestand", "otg-bestandsindeling", "wat is een otg-bestand", "bestand", "otg-voorbeeld", "otg-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument Tekensjabloon Bestandsformaat",
  "description":"Meer informatie over OTG-bestandsindeling en API's die OTG-bestanden kunnen maken en openen.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Wat is een OTG-bestand?

Een OTG-bestand is een tekensjabloon die is gemaakt met behulp van de OpenDocument-standaard die de OASIS Office Applications [1.0-specificatie](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf) volgt. Het vertegenwoordigt de standaardorganisatie van tekenelementen voor een vectorafbeelding die kan worden gebruikt om de inhoud van het bestand verder te verbeteren. OTF-bestanden zijn net als alle andere op OpenDocument-indeling gebaseerde bestanden die zijn gebaseerd op XML-indeling om de inhoud van het document weer te geven. OTF-bestanden kunnen worden bekeken door ze in een willekeurige tekst- of standaard XML-editor te openen.

## Specificaties OTG-bestandsindeling ##

OTG-bestandsindeling is gebaseerd op de OpenDocument XML-indeling met een goed ingeburgerd schema. De structuur van elk onderdeel van een OpenDocument-indeling wordt weergegeven door een element met bijbehorende attributen en is gemeenschappelijk voor alle documenttypen, zoals tekstdocument, spreadsheet of een tekenbestand. OTG, dat een tekensjabloon is, maakt uitgebreid gebruik van de specificaties voor grafische inhoud, waaronder:

* Verbeterde paginafuncties voor grafische toepassingen
* Vormen tekenen
* Kaders
* 3D-vormen
* Aangepaste vorm
* Presentatievormen
* Presentatie Animaties
* SMIL Presentatie Animaties
* Presentatie Evenementen
* Huidige tekstvelden
* Inhoud presentatiedocument

### Verbeterde paginafuncties voor grafische toepassingen ###
#### Hand-out Master ####

Hand-out Master-element is een sjabloon voor het automatisch genereren van de hand-outpagina's voor toepassingen die het afdrukken van dergelijke pagina's ondersteunen.
De attributen die kunnen worden geassocieerd met de `<style:handout-master>`-elementen zijn:

|Lay-out|Attribuut|Beschrijving
---|---|---|
|Presentatiepagina-indeling|presentatie:presentatie-pagina-indeling-naam|Links naar `<style:presentation-page-layout>` 'attribuut'
|Pagina-indeling|`style:page-layout-name` | Specificeert een paginalay-out die de formaten, rand en richting van de hand-outbasispagina bevat.
|Paginastijl|`draw:style-name`|Wijst aanvullende opmaakkenmerken toe aan een hand-outmasterpagina door een tekenpaginastijl toe te wijzen.|
|Kopverklaring| `presentation:use-header-name`| Specificeert de naam van de kopvelddeclaratie die wordt gebruikt voor alle kopvelden die worden weergegeven op de hand-outbasispagina.
|Voettekstverklaring| presentatie:use-footer-name|Specificeert de naam van de voettekstvelddeclaratie die wordt gebruikt voor alle voettekstvelden die worden weergegeven op de hand-outbasispagina.
|Datum- en tijddeclaratie|use-date-time-name|Specificeert de naam van de datum-tijdvelddeclaratie die wordt gebruikt voor alle datum-tijdvelden die worden weergegeven op de hand-outmodelpagina.

### Vormen tekenen ###
OpenDocument-indeling ondersteunt verschillende tekenvormen die door elk type document kunnen worden gebruikt.

|Vorm|Geassocieerde attributen| elementen
---|---|---|
Rechthoek - `<draw:rect>` |Positie, grootte, stijl, laag, Z-index, ID, bijschrift-ID, tekstanker, tabelachtergrond, eindpositie tekenen, ronde hoeken|titel, lange beschrijving, gebeurtenisluisteraars, lijmpunten, tekst
Lijn `<draw:line>` |Stijl, laag, Z-index, ID, bijschrift-ID en transformatie, tekstanker, tabelachtergrond, eindpositie tekenen, startpunt, eindpunt|Titel, lange beschrijving, gebeurtenisluisteraars, lijmpunten, tekst
Polylijn `<draw:polyline>` | Positie, grootte, weergavekader, stijl, laag, Z-index, ID, bijschrift-ID en transformatie, tekstanker, tabelachtergrond, eindpositie tekenen, punten| Titel, lange beschrijving, luisteraars van gebeurtenissen, lijmpunten, tekst
Veelhoek `<draw:polygon>` |Positie, grootte, weergavevak, stijl, laag, Z-index, ID, bijschrift-ID en transformatie, tekstanker, tabelachtergrond, eindpositie tekenen, punten|titel, lange beschrijving, gebeurtenisluisteraars, lijmpunten, tekst
|Regelmatige veelhoek `<draw:regular-polygon>` |Positie, grootte, stijl, laag, Z-index, ID, bijschrift-ID en transformatie, tekstanker, tabelachtergrond, eindpositie tekenen, hol, hoeken, scherpte|titel, lange beschrijving, gebeurtenisluisteraars, lijmpunten, tekst
|Paht `<draw:path>` |Positie, grootte, weergavevak, stijl, laag, Z-index, ID, bijschrift-ID en transformatie, tekstanker, tabelachtergrond, eindpositie tekenen, padgegevens| Titel, lange beschrijving, luisteraars van gebeurtenissen, lijmpunten, tekst

### Kaders ###
Een frame in een tekendocument is een rechthoekige container die tekstvakken, afbeeldingen of objecten bevat. Frames ondersteunen extra functies zoals contouren, afbeeldingen met afbeeldingen en hyperlinks. Een frame kan zowel een object als een afbeelding bevatten, waardoor meerdere weergaven van een object mogelijk zijn. De applicaties geven het respectieve element weer op basis van de beste ondersteuning.

Frames kunnen bevatten:
* Tekstvakken
* Objecten weergegeven in het OpenDocument-formaat of in een objectspecifiek binair formaat
* Afbeeldingen
* Appeltjes
* Plug-ins
* Zwevende frames

Een frame is opgenomen in een document zoals hieronder weergegeven.

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

## Referenties ##
* [OASIS Open Document Formaat voor Office-toepassingen](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument-indeling - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

