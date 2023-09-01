{
  "date" : "2021-02-10",
  "keywords" :[ "jpx-bestand", "jpx-bestandsformaat", "wat is een jpx-bestand", "bestand", "jpx-voorbeeld", "jpx-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Afbeeldingsbestandsformaat",
  "description":"Meer informatie over JPX-bestandsindelingen en API's die JPX-bestanden kunnen maken en openen.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Wat is een JPX-bestand? ##

Een bestand met de extensie .jpx is een extensie van de bestandsindeling JPEG 2000. Het gebruikt voornamelijk de JPEG 2000-compressie en biedt ook geavanceerde functies zoals meerdere lagen voor een afbeelding, verschillende kleurruimten, dekking en gefragmenteerde codestromen. JPX staat naast de JPEG 2000-compressie ook andere compressies toe, zoals JBIG, CCITT Group3, CCITT Group4, enz. Het JPX-bestandsformaat is goedgekeurd als [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html)-standaard, maar kon geen warm onthaal krijgen vanwege het uitgebreide gebruik van [JPEG ](/nl/image/jpeg/) bestandsformaat. Toepassingen die JPX-bestanden kunnen openen, zijn onder meer Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 en CorelDraw Graphics Suite 2020.

## Korte geschiedenis

In 2000 ontwierp de Joint Photographic Experts Group-commissie JP2 met als doel om hun eigen op discrete cosinustransformatie gebaseerde JPEG-standaard te verbeteren met deze nieuwe op wavelet gebaseerde methode. De JPEG-commissie wilde hun basismethoden vrij van licentiekosten aanbieden. In de JP2-licentie die concurrentie kreeg van 20 bedrijven, wonnen ze met een snor. JPEG 2000 is uitgeroepen tot ISO-standaard, hoewel de meeste webbrowsers sinds 2017 niet klaar zijn om JPEG 2000 een handje te helpen. In 2004 werd het ISO/IEC 15444-2-formaat publiekelijk geaccepteerd als uitbreiding op het JP2-bestandsformaat.

## JPX-bestandsindeling

Het JPX-bestandsformaat is geformuleerd om te voldoen aan de vereisten van applicaties die behoefte hadden aan datastructuren die verder gaan dan de functionaliteit gedefinieerd door het [JP2](/nl/image/jp2/)-bestandsformaat. Een JP2-bestand met niet-compatibele extensies kan leiden tot verwarring op de markt, waar sommige lezers sommige JP2-bestanden wel kunnen interpreteren, maar andere niet. JPX is het antwoord om dergelijke problemen in applicaties te vermijden.

### Bestandsidentificatie

JPX-bestanden worden opgeslagen als [JPF](/nl/image/jpf/) wanneer ze worden opgeslagen in een traditioneel computerbestandssysteem. Dat is de reden waarom de JPX-term het minst vaak wordt gebruikt in vergelijking met de JPF. Een JPX-bestand begint met de volgende bytes:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Bestandsorganisatie

Net als JP2 is een JPX-bestand een verzameling dozen met een binaire structuur waarbij de dozen in een aaneengesloten volgorde zijn gerangschikt. Het eerste vak geeft het begin van het bestand met zijn eerste byte en de laatste byte van het laatste vak vertegenwoordigt de laatste byte van het bestand.
De binaire structuur van een box in een JPX-bestand is identiek aan die gedefinieerd in het [JP2](/nl/image/jp2/)-bestandsformaat.

### Opslag van CodeStream in JPX

Met het JPX-bestandsformaat kan de afbeeldingscodestroom in fragmenten worden verdeeld. Dit maakt het mogelijk om een enkele tegel van de afbeelding te wijzigen en de gewijzigde tegel naar het einde van het bestand te schrijven zonder het hele bestand te herschrijven. Het originele [JP2](/nl/image/jp2/) bestandsformaat beperkt de opslag van de volledige codestroom in een aangrenzend deel van het bestand, wat problematisch kan zijn voor beeldbewerkingstoepassingen die een enkele tegel van de afbeelding willen wijzigen en de bovenstaande ondersteuning door JPX-bestandsindeling. De fragmentatie van de beeldcodestroom maakt het JPX-bestandsformaat superieur aan het JP2-bestandsformaat. Bovendien maakt het JPX-bestandsformaat het mogelijk om meerdere codestreams te combineren en gerenderde resultaten te produceren. Codestreams kunnen worden gecombineerd als compositing en animatie.

## Referenties ##

* [Overzicht van JPEG 2000](https://jpeg.org/jpeg2000/)

