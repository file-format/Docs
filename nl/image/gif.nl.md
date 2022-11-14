{
  "date" : "2019-10-11",
  "keywords" :[ "gif-bestand", "gif-bestandsindeling", "wat is een gif-bestand", "bestand", "gif-voorbeeld", "gif-bestandsextensie", "extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Afbeeldingsbestandsformaat",
  "description":"Meer informatie over GIF-bestandsindeling en API's die GIF-bestanden kunnen maken en openen.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een GIF-bestand? ##

Een GIF of Graphical Interchange Format is een type sterk gecomprimeerde afbeelding. GIF, eigendom van Unisys, gebruikt het LZW-compressie-algoritme dat de beeldkwaliteit niet verslechtert. Voor elke afbeelding staat GIF doorgaans tot 8 bits per pixel toe en zijn tot 256 kleuren toegestaan over de afbeelding. In tegenstelling tot een [JPEG](/nl/image/jpeg/)-afbeelding, die tot 16 miljoen kleuren kan weergeven en redelijk de grenzen van het menselijk oog raakt. Toen het internet opkwam, bleven GIF's de beste keuze omdat ze een lage bandbreedte nodig hadden en compatibel waren voor de afbeeldingen die effen kleurvlakken verbruiken. Een geanimeerde GIF combineert een groot aantal afbeeldingen of frames in een enkel bestand en geeft ze in een volgorde weer om een geanimeerde clip of een korte video te genereren. De kleurbeperkingen zijn maximaal 256 voor elk frame en zijn waarschijnlijk het minst geschikt voor het reproduceren van andere afbeeldingen en foto's met kleurverloop.

## GIF-bestandsindeling ##

Conceptueel hebben GIF-bestanden een grafisch gebied met een vaste grootte, gevuld met nul of meer afbeeldingen. Sommige GIF-bestanden verdelen het grafische gebied of de blokken met een vaste grootte in subafbeeldingen die kunnen functioneren als geanimeerde frames in het geval van geanimeerde GIF. Het GIF-formaat gebruikt de pixeldiepte van 1 tot 8 bits om de bitmapgegevens op te slaan. RGB-kleurmodel- en paletgegevens worden altijd gebruikt om de afbeeldingen op te slaan. Afhankelijk van de versie definieert een header met vaste lengte ("GIF87a" of "GIF89a") het begin van een typisch GIF-bestand.

Momenteel zijn er twee versies van GIF: 87a en 89a beschikbaar. De eerste is het originele GIF-formaat, terwijl de laatste het nieuwe GIF-formaat is. In dit bestandsformaat worden de kenmerken van de blokken en pixelafmetingen vermeld in een logische schermdescriptor met een vaste lengte. Het bestaan en de grootte van een globale kleurentabel kunnen worden gespecificeerd door de schermbeschrijving, die, indien aanwezig, verdere details bijhoudt. De trailer is de laatste byte van het bestand dat een enkele byte van een ASCII-puntkomma bevat. Een typische GIF87a-bestandsindeling is als volgt:

### Koptekst ###

De header bevat zes bytes en wordt gebruikt om het type bestand als GIF te specificeren. Hoewel de logische schermbeschrijving is gescheiden van de werkelijke koptekst, wordt deze soms als de tweede koptekst beschouwd. Dezelfde structuur die wordt gebruikt om de koptekst op te slaan, kan de logische schermdescriptor bevatten. Alle GIF-bestanden beginnen met de handtekening van 3 bytes en gebruiken de tekens "GIF" als identificatie. De versie is ook drie bytes groot en geeft de versie van het GIF-bestand aan.

### Logische schermbeschrijving ###

Een Image Descriptor met een vaste lengte specificeert de scherm- en kleurinformatie die nodig is om de GIF-afbeelding te maken. De velden Hoogte en Breedte bevatten de kleinste waarde van de schermresolutie, die verplicht is om de afbeeldingsgegevens weer te geven. Als het weergaveapparaat niet in staat is om de gespecificeerde resolutie weer te geven, is schaling nodig om het beeld op de juiste manier weer te geven. Scherm- en kleurenkaartinformatie wordt weergegeven door de vier subvelden van de onderstaande tabel (terwijl bit 0 het minst significante bit is):


|Bits|Subvelden
---|---|
|0-2|Grootte van de globale kleurentabel
|3|Kleurentabel Sorteer Vlag
|4-6|Kleurresolutie
|7|Global Color Table Flag

#### Globale kleurentabel ####

Een optionele globale kleurentabel wordt direct na de Logical Screen Descriptor geplaatst. Deze tabel is toegewezen om de pixelkleurgegevens in de afbeeldingsgegevens te indexeren. Bij afwezigheid van een globale kleurentabel, gebruikt elke afbeelding in het GIF-bestand zijn lokale kleur. Het is beter om een standaardkleurentabel aan te leveren als zowel de globale als de lokale kleurentabel ontbreekt. Een reeks triples van drie bytes vormen de elementen van de kleurentabel. Elke byte kenmerkt een RGB-kleurwaarde. De rode, groene en blauwe kleuren worden gebruikt als waarden van elk kleurentabelelement. De items in de Global Color Table hebben een maximum van 256 items en vertegenwoordigen altijd een macht van twee.

#### Afbeeldingsgegevens ####

De beeldgegevens slaan een byte van niet-gecodeerde symbolen op, gevolgd door een gekoppelde lijst van sub-samen met de LZW-gecodeerde gegevens.

#### Aanhangwagen ####

Trailer vertegenwoordigt een enkele byte aan gegevens die het laatste teken in het bestand is. De waarde van deze byte is permanent 3Bh en geeft het einde van de datastroom aan. Elk GIF-bestand moet de trailer in de laatste van elk bestand hebben.

## Referenties ##

* [GIF-bestandsindeling](https://en.wikipedia.org/wiki/GIF)

