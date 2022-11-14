{
  "date" : "2019-10-11",
  "keywords" :[ "psb-bestand", "psb-bestandsindeling", "wat is een psb-bestand", "bestand", "psb-voorbeeld", "psb-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Photoshop Big Image-bestandsindeling",
  "description":"Meer informatie over PSB-bestandsindeling en API's die PSB-bestanden kunnen maken en openen.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PSB-bestand?
Adobe photoshop slaat bestanden op in twee formaten. Bestanden met een grootte van 30.000 bij 30.000 pixels worden opgeslagen met de PSD-extensie en bestanden groter dan PSD tot 300.000 bij 300.000 pixels worden opgeslagen met de PSB-extensie die bekend staat als "Photoshop Big". Meer specifiek kunnen PSB-bestanden zo groot zijn als 4 EB (meer dan 4,2 miljard GB) met afbeeldingen met een hoogte en breedte tot 300.000 pixels. PSD's daarentegen kunnen maximaal 2 GB zijn en beeldafmetingen van 30.000 pixels.

PSB staat ook bekend als groot formaat voor photoshop en ondersteunt alle photoshop-functies zoals lagen, effecten en filters. Photoshop kan PSB-bestanden converteren naar [PSD](/nl/image/psd/), [JPG](/nl/image/jpeg/) , [PNG](/nl/image/png/), [EPS](/nl/page-description-language/eps/), [GIF](/nl/image/gif/) en ook andere formaten. Het grote documentformaat van Photoshop is beschikbaar zodra de functie van het paneel voor bestandsverwerking van het dialoogvenster Voorkeuren van Photoshop is ingeschakeld.

## Informatie over bestandsindeling ##

Het Photoshop-bestandsformaat is verdeeld in vijf grote delen met veel lengtemarkeringen om tussen secties te bewegen.

|Bestandsindeling
---|
|Bestandskop
|Kleurmodusgegevens
| Afbeeldingsbronnen
|Laag- en maskerinformatie
|(((
Afbeeldingsgegevens
)))

### Bestandskop ###

De bestandskop heeft een vaste lengte van 26 bytes en bevat de basiseigenschappen van de afbeelding.

BYTE-handtekening [4] – Is gelijk aan '8BPS'.

WORD-versie [2] - Versienummer, PSD # 1, PSB # 2.

BYTE Gereserveerd [6] – Gereserveerd en altijd nul.

WORD-kanalen [2] – Aantal kleurkanalen in de afbeelding, inclusief alfakanalen. De waarde varieert van 1 tot 56.

LONG Rows [4] – Hoogte van de afbeelding in pixels, PSD 1-30.000, PSB 1-300.000.

LANGE kolommen [4] – Breedte van de afbeelding in pixels, PSD 1-30.000, PSB 1-300.000.

WORD Depth [2] – Aantal bits per kanaal. Ondersteunde waarden zijn 1,8,16 en 32.

WORD-modus [2] – Kleurmodus van het bestand.

#### Modus Beschrijving ####


|Modus|Beschrijving
---|---|
|0|Bitmap (zwart-wit)
|1|Grijsschaal
|2|Geïndexeerd
|3|RGB
|4|CMYK
|7|Meerkanaals
|8|Duotoon (halftoon)
|9|Lab

### Kleurmodusgegevens ###

Na de bestandskopsectie volgt de kleurmodusgegevenssectie. Het blok begint met een LANG Nummer dat de lengte van het blok in bytes aangeeft. De structuur van de kleurmodusgegevens is als volgt:

4 bytes – De lengte van de volgende kleurgegevens.

Variabele – Kleurgegevens

Als de waarde van het modusveld in het kopgedeelte niet Geïndexeerde kleur of duotoon is, is de lengte van het blok 0 en zijn er geen gegevens na het lengteveld.

Voor geïndexeerde kleurenafbeeldingen is de lengte 768 bytes, wat een 256 kleurenpalet zal bevatten. Voor duotoon zullen gegevens schermparameters en andere gerelateerde informatie bevatten.

### Beeldbronnen ###

Na het gedeelte met kleurmodusgegevens, is het derde blok het gedeelte met beeldbronnen. De eerste vier bytes zijn een LANG getal dat de lengte van het blok aangeeft, gevolgd door een reeks bronblokken. De structuur van het afbeeldingsbronblok is als volgt:

BYTE-type [4] – Handtekening '8BIM'

WOORD-ID [2] – Afbeeldingsbron-ID. Er is een lijst met resource-ID's die kan worden bekeken via de referentielink.

BYTE Naam [Variabele] – Naam: Pascal String met even lengte. ** **

LONG Size [4] – Werkelijke grootte van resourcegegevens die volgt.

BYTE-gegevens [Variabele} – Brongegevens. Het is gewatteerd om de gelijkmatige maat te maken.

Enkele van de bronformaten worden hieronder kort toegelicht:

**Resource-indeling raster en hulplijnen:** Informatie over rasters en hulplijnen wordt opgeslagen in het resourceblok. Deze resourceblokken bevatten een raster van 16 bytes en een gidskop, gevolgd door blokken van 5 bytes met gidsinformatie.

**Thumbnail Resource Format:** Thumbnail-informatie wordt opgeslagen in het afbeeldingsresourceblok voor preview-weergave, dat bestaat uit een 28-byte-header en JFIF-miniatuur in RGB.

**Resourceformaat kleursamplers:** Informatie over kleursamplers wordt opgeslagen in een afbeeldingsbronblok met een kop van 8 bytes, gevolgd door een blok met variabele lengte met informatie over kleursamplers.

### Informatie over lagen en maskers ###

Het vierde blok is het laag- en maskerinformatieblok en bevat informatie over de lagen en maskers. Laaginformatie wordt eerst opgeslagen en daarna maskerinformatie.

**Laaginformatie:** Laaginformatie begint met een LONG-waarde die de lengte van de laaginformatie aangeeft. Daarna is er een WORD-waardetelling die het aantal te volgen laagrecords laat zien.

[8] – lengte van de lagen

[2] – Aantal lagen

[Variabele] – Informatie over elke laag.

[Variabele] – Kanaalbeeldgegevens.** **

**Maskerinformatie:** De maskerstructuur heeft de volgende indeling:


|Gegevensstructuur|Veldnaam| Beschrijving
---|---|---|
|WOORD| Overlay-kleurruimte| (Niet gedocumenteerd)
|BYTE[8]| Kleurcomponenten| 4x2 byte kleurcomponenten
|WOORD| Ondoorzichtigheid| 0#transparant, 1#ondoorzichtig
|BYTE| Soort| 0#omgekeerd, 1#beschermd, 128#gebruik opgeslagen waarde
|BYTE| opvulling| op nul zetten

### Afbeeldingsgegevens ###

Het laatste gedeelte bevat de afbeeldingspixelgegevens. De beeldgegevens worden opgeslagen als een reeks reeksen in vlakken, dwz eerst alle rode gegevens, dan alle groene gegevens enz. WOORD aan het begin van elke regel geeft de grootte in bytes aan die betrekking heeft op elke scanregel.

[2] – Compressiemethode:

[Variabele] – Beeldgegevens in vlakke volgorde, dwz RRRR, GGGG, BBBB enz.

Compressie methoden:

0 – Raw Afbeeldingsgegevens

1 – RLE gecomprimeerd

2 – Zip zonder voorspelling

3 – Zip met voorspelling

## Referentie ##

* [PSB-bestandsindeling - door Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

