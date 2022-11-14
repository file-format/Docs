{
  "date" : "2019-10-11",
  "keywords" :[ "tiff-bestand", "tiff-bestandsformaat", "wat is een tiff-bestand", "bestand", "tiff-voorbeeld", "tiff-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Afbeeldingsbestandsformaat",
  "description":"Meer informatie over TIFF-bestandsindelingen en API's die TIFF-bestanden kunnen maken en openen.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een TIFF-bestand?

TIFF of TIF, Tagged Image File Format, staat voor rasterafbeeldingen die bedoeld zijn voor gebruik op verschillende apparaten die voldoen aan deze standaard voor bestandsindelingen. Het is in staat om bilevel-, grijswaarden-, paletkleur- en full-color afbeeldingsgegevens in verschillende kleurruimten te beschrijven. Het ondersteunt zowel lossy als lossless compressieschema's om te kiezen tussen ruimte en tijd voor toepassingen die het formaat gebruiken. Het formaat is niet machine-afhankelijk en is vrij van beperkingen zoals processor, besturingssysteem of bestandssystemen.

## Korte geschiedenis van TIFF-bestandsindeling

Het TIFF-bestandsformaat werd oorspronkelijk gecreëerd door Aldus Corporation in de herfst van 1986, na een reeks ontmoetingen met verschillende scannerfabrikanten en softwareontwikkelaars. Het primaire doel van de TIFF-bestandsindeling was om een gemeenschappelijke bestandsindeling voor gescande afbeeldingen te bieden voor alle leveranciers van desktopscanners. Beginnend met ondersteuning voor alleen het binaire afbeeldingsformaat, evolueerde het formaat met het verstrijken van de tijd naar de ondersteuning van grijswaarden- en kleurenafbeeldingen. De initiële versie van de specificaties van de TIFF-bestandsindeling kan worden aangeduid als Reivision 3.0, aangezien er twee eerdere conceptversies waren. In 1988 werd een grote revisie 5.0 gepubliceerd die ondersteuning voor paletkleurenafbeeldingen en LZW-compressie toevoegde. Revisie 6.0 van TIFF-bestandsindelingen werd daarna in 1992 gepubliceerd. In 1994 nam Adobe Systems Aldus over en de specificaties zijn nu beschikbaar en worden onderhouden door Adobe Systems.

## Specificaties TIFF-bestandsindeling

Het TIFF-bestandsformaat is uitbreidbaar en heeft verschillende revisies ondergaan waardoor een onbeperkte hoeveelheid persoonlijke of speciale informatie kan worden opgenomen. Een TIFF-bestand begint met een header van 8 bytes waarin de bytes een getal zijn van 0 tot N. Het grootst mogelijke TIFF-bestand is 2**32 bytes lang. Het bestand begint met een 8-byte afbeeldingsbestandskop die rechtstreeks naar een afbeeldingsbestand verwijst (IFD). Een IFD bevat informatie over de afbeelding en verwijzingen naar de daadwerkelijke afbeeldingsgegevens.

### TIFF-bestandskop

De 8-byte TIFF-bestandskop bevat de volgende informatie:

**Bytes 0-1:** De bytevolgorde die in het bestand wordt gebruikt. Wettelijke waarden zijn:“II”(4949.H)“MM” (4D4D.H).

In het "II"-formaat is de bytevolgorde altijd van de minst significante byte tot de meest significante byte, voor zowel 16-bits als 32-bits gehele getallen. Dit wordt de little-endian bytevolgorde genoemd. In de "MM"-indeling is de bytevolgorde altijd van meest significant tot minst significant, voor zowel 16-bits als 32-bits gehele getallen. Dit wordt big-endian bytevolgorde genoemd.

**Bytes 2-3:** Een willekeurig maar zorgvuldig gekozen nummer (42) dat het bestand verder identificeert als een TIFF-bestand. De bytevolgorde hangt af van de waarde van Bytes 0-1.

**Bytes 4-7:** De offset (in bytes) van de eerste IFD. De map mag zich op elke locatie in het bestand na de koptekst bevinden, maar moet beginnen op een woordgrens. In het bijzonder kan een afbeeldingsbestandsdirectory de afbeeldingsgegevens volgen die het beschrijft. Lezers moeten de aanwijzers volgen waar ze ook heen leiden. De term byte-offset wordt in dit document altijd gebruikt om te verwijzen naar een locatie ten opzichte van het begin van het TIFF-bestand. De eerste byte van het bestand heeft een offset van 0.

### Afbeeldingsbestandsmap

Een IFD bevat informatie over de afbeelding en verwijzingen naar de daadwerkelijke afbeeldingsgegevens. Het bestaat uit een 2-byte telling van het aantal directory-items (dwz het aantal velden), gevolgd door een reeks van 12-byte-velditems , gevolgd door een 4-byte offset van de volgende IFD (of 0 als er geen is). Er moet minimaal 1 IFD in een TIFF-bestand zitten en elke IFD moet minimaal één item bevatten.

#### IFD-invoer

Elke IFD-invoer van 12 bytes heeft de volgende indeling.


|Bytes|Beschrijving
---|---|
|0-1|De tag die het veld identificeert
|2-3|Het veldtype
|4-7|Tellen van het aangegeven type
|8-11|De waardeverschuiving, de bestandsverschuiving (in bytes) van de waarde voor het veld. De waarde begint naar verwachting op een woordgrens; de corresponderende Value Offset zal dus een even getal zijn. Deze bestandsoffset kan overal in het bestand wijzen, zelfs na de afbeeldingsgegevens

Een TIFF-veld is een logische entiteit die bestaat uit een TIFF-tag en zijn waarde. Dit logische concept wordt geïmplementeerd als een IFD-invoer, plus de werkelijke waarde als deze niet past in het waarde/offset-gedeelte, de laatste 4 bytes van de IFD-invoer. De termen TIFF-veld en IFD-invoer zijn in de meeste contexten uitwisselbaar.

### Basislijn TIFF ###

Baseline TIFF is de kern van TIFF, de essentie die alle reguliere TIFF-ontwikkelaars in hun producten zouden moeten ondersteunen. Conformiteit met het TIFF-formaat is onderhevig aan naleving van de Baseline TIFF-vereisten. Deze eisen zijn goed gedocumenteerd in het specificatiedocument 6.0.

#### Meerdere afbeeldingen per bestand ####

Er kan meer dan één IFD in een TIFF-bestand staan. Elke IFD definieert een subbestand. Een mogelijk gebruik van subbestanden is het beschrijven van verwante afbeeldingen, zoals de pagina's van een faxverzending. Een Baseline TIFF-lezer is niet vereist om IFD's na de eerste te lezen.

#### Afbeeldingstypen ####

Basislijn TIFF-afbeelding heeft de volgende typen:

**Bilevel:** Een afbeelding op twee niveaus bevat twee kleuren: zwart en wit. Met TIFF kan een toepassing bilevel-gegevens wegschrijven in een wit-is-nul- of zwart-is-nul-indeling. Het veld waarin deze informatie wordt vastgelegd, heet **PhotometricInterpretation**.

* RGB-kleuren in kleur

Fotometrische interpretatie-informatie voor Bilevel-afbeeldingen is als volgt:

Tag = 262 (106.H)
Type = KORT
**Waarden**

|Waarde|Beschrijving|
---|---|
|0|Voor bilevel- en grijswaardenafbeeldingen: 0 wordt afgebeeld als wit. De maximale waarde wordt afgebeeld als zwart. Dit is de normale waarde voor Compressie #2|
|1|ZwartIsZero. Voor bilevel- en grijswaardenafbeeldingen: 0 wordt afgebeeld als zwart. De maximale waarde wordt afgebeeld als wit. Als deze waarde is opgegeven voor Compressie#2, zou de afbeelding omgekeerd moeten worden weergegeven en afgedrukt.|

**Grijsschaal:** Grijswaardenafbeeldingen zijn een veralgemening van afbeeldingen op twee niveaus. Bilevel-afbeeldingen kunnen alleen zwart-witafbeeldingsgegevens opslaan, maar in grijswaardenafbeeldingen kunnen ook grijstinten worden opgeslagen. Om dergelijke afbeeldingen te beschrijven, moet u de volgende velden toevoegen of wijzigen. De andere verplichte velden zijn dezelfde als die voor bilevel-afbeeldingen. Voor afbeeldingen in grijswaarden, compressie # 1 of 32773 (PackBits). In Baseline TIFF kunnen grijswaardenafbeeldingen worden opgeslagen als niet-gecomprimeerde gegevens of worden gecomprimeerd met het PackBits-algoritme.

**BitsPerSample** informatie voor grijswaardenafbeeldingen is als volgt:

Tag = 258 (102.H)
Type = KORT

Het aantal bits per component. Toegestane waarden voor Baseline TIFF-grijswaardenafbeeldingen zijn 4 en 8, waardoor 16 of 256 verschillende grijstinten mogelijk zijn.

**Paletkleur:** Paletkleurenafbeeldingen zijn vergelijkbaar met grijswaardenafbeeldingen. Ze hebben nog steeds één component per pixel, maar de componentwaarde wordt gebruikt als index in een volledige RGB-opzoektabel. Om dergelijke afbeeldingen te beschrijven, moet u de volgende velden toevoegen of wijzigen. De andere verplichte velden zijn dezelfde als die voor grijswaardenafbeeldingen.
Fotometrische interpretatie-informatie voor palet-kleurenafbeelding is als volgt:

Fotometrische Interpretatie = 3 (Paletkleur).
ColorMapTag = 320 (140.H)
Type = KORT
N = 3 * (2 bits per monster)

Dit veld definieert een rood-groen-blauwe kleurenkaart (vaak een opzoektabel genoemd) voor paletkleurenafbeeldingen. In een afbeelding met paletkleuren wordt een pixelwaarde gebruikt om te indexeren in een RGB-opzoektabel. Een paletkleurpixel met een waarde van 0 zou bijvoorbeeld worden weergegeven volgens het 0-de rode, groene, blauwe triplet. In een TIFF ColorMap komen eerst alle rode waarden, gevolgd door de groene waarden en daarna de blauwe waarden. In de ColorMap wordt zwart weergegeven door 0,0,0 en wit wordt weergegeven door 65535, 65535, 65535.

**RGB full-color:** In een RGB-afbeelding bestaat elke pixel uit drie componenten: rood, groen en blauw. Er is geen ColorMap. Om een RGB-afbeelding te beschrijven, moet u de volgende velden en waarden toevoegen of wijzigen. De andere verplichte velden zijn dezelfde als die voor afbeeldingen in paletkleuren.

BitsPerSample = 8,8,8. Elke component is 8 bits diep in een Baseline TIFF RGB-afbeelding.

PhotometricInterpretation = 2 (RGB) en er is geen ColorMap.

Tag = 277 (115.H)
Type = KORT
Het aantal componenten per pixel. Dit aantal is 3 voor RGB-afbeeldingen, tenzij er extra samples aanwezig zijn.

## Referenties ##

* [TIFF-bestandsindeling - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

