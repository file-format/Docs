{
  "date" : "2019-11-25",
  "keywords" :[ "jpeg-bestand", "jpeg-bestandsformaat", "wat is een jpeg-bestand", "bestand", "jpeg-voorbeeld", "jpeg-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Afbeeldingsbestandsformaat",
  "description":"Meer informatie over JPEG-bestandsindelingen en API's die JPEG-bestanden kunnen maken en openen.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Wat is een JPEG-bestand? ##

Een JPEG is een type afbeeldingsformaat dat wordt opgeslagen met de methode van compressie met verlies. Het uitvoerbeeld, als resultaat van compressie, is een afweging tussen opslaggrootte en beeldkwaliteit. Gebruikers kunnen het compressieniveau aanpassen om het gewenste kwaliteitsniveau te bereiken en tegelijkertijd de opslagruimte te verkleinen. De beeldkwaliteit wordt verwaarloosbaar beïnvloed als 10:1 compressie op de afbeelding wordt toegepast. Hoe hoger de compressiewaarde, hoe groter de verslechtering van de beeldkwaliteit.

## Specificaties bestandsindeling ##

Het JPEG-beeldbestandsformaat is gestandaardiseerd door de Joint Photographic Experts Group en vandaar de naam JPEG. Het formaat is de keuze geweest voor het opslaan en verzenden van fotografische afbeeldingen op het web. Bijna alle besturingssystemen hebben nu viewers die de visualisatie van JPEG-afbeeldingen ondersteunen, die vaak ook met de JPG-extensie worden opgeslagen. Zelfs de webbrowsers ondersteunen visualisatie van JPEG-afbeeldingen. Voordat we ingaan op de specificaties van het JPEG-bestandsformaat, moet het algemene proces van stappen die betrokken zijn bij het maken van JPEG worden vermeld.

### JPEG-compressiestappen ###

**Transformatie:** Kleurenafbeeldingen worden van RGB omgezet in een luminantie/chrominantie-afbeelding (Oog is gevoelig voor luminantie, niet voor chrominantie, zodat het chrominantiegedeelte veel gegevens kan verliezen en dus sterk kan worden gecomprimeerd.

**Downsampling:** De downsampling wordt gedaan voor gekleurde componenten en niet voor luminantiecomponenten. Downsampling wordt gedaan in een verhouding 2:1 horizontaal en 1:1 verticaal (2h 1 V). Het beeld wordt dus kleiner omdat de 'y'-component niet wordt aangeraakt, er is geen merkbaar verlies aan beeldkwaliteit.

**Ordenen in groepen:** De pixels van elke kleurcomponent zijn geordend in groepen van 8×2 pixels die "gegevenseenheden" worden genoemd. Als het aantal rijen of kolommen geen veelvoud is van 8, worden de onderste rij en de meest rechtse kolommen gedupliceerd.

**Discrete cosinustransformatie:** Discrete cosinustransformatie (DCT) wordt vervolgens toegepast op elke data-eenheid om een 8×8-kaart van getransformeerde componenten te maken. Bij DCT gaat wat informatie verloren vanwege de beperkte nauwkeurigheid van computerrekenkunde. Dit betekent dat er zelfs zonder de kaart enig verlies van beeldkwaliteit zal zijn, maar deze is normaal gesproken klein.

**Kwantisering:** Elk van de 64 getransformeerde componenten in de gegevenseenheid wordt gedeeld door een afzonderlijk getal, de 'kwantiseringscoëfficiënt (QC)' genoemd en vervolgens afgerond op een geheel getal. Dit is waar informatie onherstelbaar verloren gaat, Grote QC veroorzaakt meer verlies. Over het algemeen laten de meeste JPEG-tools het gebruik van QC-tabellen toe die worden aanbevolen door de JPEG-standaard.

**Codering:** De 64 gekwantiseerde getransformeerde coëfficiënten (die nu gehele getallen zijn) van elke data-eenheid worden gecodeerd met een combinatie van RLE- en Huffman-codering.

**Koptekst toevoegen:** De laatste stap voegt de koptekst en alle gebruikte JPEG-parameters toe en geeft het resultaat weer.

De JPEG-decoder gebruikt de stappen in omgekeerde volgorde om de originele afbeelding van de gecomprimeerde afbeelding te genereren.

### Bestandsstructuur ###

Een JPEG-afbeelding wordt weergegeven als een reeks segmenten waarbij elk segment begint met een markering. Elke markering begint met 0xFF byte gevolgd door een markeringsvlag om het type markering weer te geven. De payload gevolgd door marker verschilt per type marker. Veelvoorkomende JPEG-markeringstypen zijn zoals hieronder vermeld:

|Korte naam|Bytes|Payload|Naam|Opmerkingen
---|---|---|---|---|
|SOI|0xFF, 0xD8|geen|Begin van afbeelding|
|S0F0|0xFF, 0xC0|variabele grootte|Begin van frame|
|S0F2|0xFF, 0xC2|variabele grootte|Begin voor frame|
|DHT|0xFF, 0xC4|variabele grootte|Definieer Huffman-tabellen|
|DQT|0xFF, 0xDB|variabele grootte|Definieer kwantiseringstabel(len)|
|DRI|0xFF, 0xDD|4 bytes|Definieer herstartinterval|
|SOS|0xFF, 0xDA|variabele grootte|Begin van scan|
|RSTn|0xFF, 0xD//n//(/nl//n//#0..7)|geen|Herstart|
|APPn|0xFF, 0xE//n//|variabele grootte|Toepassingsspecifiek|
|COM|0xFF, 0xFE|variabele grootte|Commentaar|
|EOI|0xFF, 0xD9|geen|Einde van afbeelding|

Binnen de entropiegecodeerde gegevens wordt na elke 0xFF-byte een 0x00-byte ingevoegd door de encoder vóór de volgende byte, zodat er geen markering lijkt te zijn waar geen enkele is bedoeld, waardoor framingfouten worden voorkomen. Decoders moeten deze 0x00 byte overslaan. Deze techniek, genaamd [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (zie JPEG-specificatie sectie F.1.2.3), wordt alleen toegepast op de entropie-gecodeerde data, niet om de payload data te markeren . Merk echter op dat entropiegecodeerde gegevens een paar eigen markeringen hebben; met name de Reset-markeringen (0xD0 tot 0xD7), die worden gebruikt om onafhankelijke brokken entropie-gecodeerde gegevens te isoleren om parallelle decodering mogelijk te maken, en encoders zijn vrij om deze Reset-markeringen met regelmatige tussenpozen in te voegen (hoewel niet alle encoders dit doen).

