{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "bestand", "bestandsindeling", "Taal paginabeschrijving", "Scalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over SVG-bestandsindelingen en API's die SVG-bestanden kunnen maken en openen.",
  "title" :"Wat is een SVG-bestand?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Wat is een SVG-bestand? ##

Een SVG-bestand is een Scalar Vector Graphics-bestand dat op XML gebaseerde tekstindeling gebruikt om het uiterlijk van een afbeelding te beschrijven. Het woord Scalable verwijst naar het feit dat de SVG kan worden geschaald naar verschillende formaten zonder kwaliteitsverlies. Op tekst gebaseerde beschrijving van dergelijke bestanden maakt ze onafhankelijk van resolutie. Het is een van de meest gebruikte formaten voor het bouwen van een website en het afdrukken van afbeeldingen om schaalbaarheid te bereiken. Het formaat kan echter alleen worden gebruikt voor tweedimensionale afbeeldingen. SVG-bestanden kunnen worden bekeken/geopend in bijna alle moderne browsers, waaronder Chrome, Internet Explorer, Firefox en Safari.

## Korte geschiedenis ##

SVG-specificaties zijn sinds 1999 beschikbaar als open standaard door World Wide Web Consortium (W3C). Daarvoor werden tot 1998 vergelijkbare bestandsformaatspecificaties in zes verschillende formaten ingediend bij W3C. In 2011 werd een update van de specificaties toegepast en deze kreeg versie 1.1. . In 2016 werd SVG 2 gepubliceerd als nieuwere versie, inclusief functies naast die in SVG 1.1.

## Specificaties bestandsindeling ##

Het SVG Document Object Model (DOM) legt de basis voor alle specificaties en interfaces die overeenkomen met de specifieke secties van de specificaties. SVG-viewers moeten de SVG DOM-interfaces implementeren zoals gedefinieerd in de W3C-specificaties. De DOM onthult verschillende interfaces voor verschillende gegevenstypen en elementen.

### SVG-vormen ###

SVG heeft een aantal vooraf gedefinieerde vormelementen die door ontwikkelaars kunnen worden gebruikt:

* Rechthoek<rect>
* Cirkel<circle>
* Ovaal<ellipse>
* Lijn<line>
* Polylijn<polyline>
* Veelhoek<polygon>
* Pad<path>

Op basis van deze vormen en specificaties zijn de functionele gebieden van SVG als volgt.

**Paden** - Paden worden gebruikt om zowel eenvoudige als samengestelde vormcontouren weer te geven. Coderingen worden gebruikt om de aard van de operatie te definiëren. M wordt bijvoorbeeld gebruikt voor Verplaatsen naar, L wordt gebruikt voor Lijn naar, Z wordt gebruikt om een pad te sluiten, enzovoort.

**Basisvormen** - Rechte paden en paden bestaande uit een reeks verbonden rechte lijnsegmenten (polylijnen), evenals gesloten polygonen, cirkels en ellipsen kunnen worden getekend. Rechthoeken en rechthoeken met ronde hoeken zijn ook standaardelementen.

**Tekst** - Tekstrepresentatie wordt uitgedrukt als XML-tekengegevens waarbij veel visuele effecten op de tekst kunnen worden toegepast. De specificaties maken het mogelijk om bidirectionele tekst, verticale tekst en tekens langs een gebogen pad te verwerken.

**Schilderen** - Vormen kunnen worden gevuld en/of omlijnd met een kleur, een verloop of een patroon, waardoor ze dekkend kunnen worden of enige mate van transparantie hebben. Functies aan het einde van de lijn, zoals pijlpunten of symbolen die op de hoekpunten van een veelhoek verschijnen, worden weergegeven door markeringen.

**Kleur** - Met SVG-specificaties kunnen kleuren worden toegepast op alle zichtbare SVG-elementen, hetzij rechtstreeks, hetzij via vulling, lijn en andere eigenschappen. Er kunnen verschillende kleurcoderingen worden gebruikt voor het specificeren, zoals zwart of blauw, hex-weergave, decimaal of als percentages van de vorm RGB.

**Verlopen en patronen** - Vormen in een SVG-bestand kunnen worden gevuld of omlijnd met effen kleuren, verlopen of herhalende patronen.

**Filtereffecten** - Het is eigenlijk een reeks grafische bewerkingen die worden toegepast op een bepaalde bronvectorafbeelding om een gewijzigd resultaat te produceren.

**Interactiviteit** - Gebruikers kunnen communiceren met SVG-bestanden door de focus te wijzigen, te klikken met de muis, te scrollen of in te zoomen op de afbeelding. Dankzij de interactiviteit kunnen SVG-afbeeldingen op veel verschillende manieren met gebruikers communiceren, zoals hierboven vermeld.

**Koppelen** - Het is mogelijk dat SVG-afbeeldingen hyperlinks hebben naar andere documenten. Dit wordt bereikt via de XML Linking Language of XLink. Dit maakt het mogelijk om specifieke weergavestatussen te creëren die worden gebruikt om in/uit te zoomen op een specifiek gebied of om de weergave te beperken tot een specifiek element.

**Scripting** - Net als bij HTML zijn alle aspecten van een SVG-document toegankelijk voor manipulatie met behulp van scripts. De SVG DOM-objecten bieden de begeleiding om dit te bereiken met behulp van SVG-elementen en -attributen. Scripts zijn ingesloten in `script` tag-elementen en kunnen naar behoefte worden uitgevoerd als reactie op aanwijzer-, toetsenbord- of documentgebeurtenissen.

**Animatie** - De DOM-elementen<animate> ,<animateMotion> en<animateColor> kunt u animaties opnemen voor SVG-inhoud. Dit is natuurlijk niet haalbaar zonder gebruik te maken van scripts en ingebouwde timers. Deze animaties kunnen continu zijn en kunnen zowel in een lus als herhalingen worden geplaatst, terwijl ze tegelijkertijd reageren op gebruikersgebeurtenissen.

**Lettertypen** - Tekst in SVG kan verwijzen naar externe lettertypebestanden, zoals systeemlettertypen. Als dergelijke lettertypen ontbreken, wordt tekst in SVG niet naar de uitvoer weergegeven. Dit kan worden ondervangen door de vereiste glyphs in een dergelijk bestand op te nemen als een lettertype dat vervolgens wordt weergegeven met de<text> element.

## Voorbeelden ##
De volgende regels laten zien hoe een cirkel wordt weergegeven met behulp van het SVG-script.

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

De volgende regels code laten zien hoe u de . gebruikt<text> blok voor het renderen van tekst naar SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referenties ##

* [W3C SVG-specificaties](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

