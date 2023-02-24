{
  "date" : "2019-10-11",
  "keywords" :[ "3DS", "bestand", "formaat", "bestandstype", "extensie", "wat is een 3DS-bestand?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over 3DS-bestandsindelingen en API's die 3DS-bestanden kunnen openen en maken.",
  "title" :"3DS-bestandsindeling",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een 3DS-bestand?

Een bestand met de extensie .3ds vertegenwoordigt de 3D Sudio (DOS) mesh-bestandsindeling die wordt gebruikt door Autodesk 3D Studio. Autodesk 3D Studio is sinds de jaren negentig actief op de markt voor 3D-bestandsindelingen en is nu geëvolueerd naar 3D Studio MAX voor het werken met 3D-modellering, animatie en weergave. Een 3DS-bestand bevat gegevens voor 3D-weergave van scènes en afbeeldingen en is een van de populaire bestandsindelingen voor het importeren en exporteren van 3D-gegevens. Het houdt rekening met informatie zoals cameralocaties, mesh-gegevens, verlichtingsinformatie, viewport-configuraties, vloeiende groepsgegevens, bitmapreferenties en attributen om hoekpunten en polygonen te creëren voor het renderen van een scène.

## 3DS-bestandsindeling - Meer informatie
In de basis is 3DS een binair bestandsformaat en volgt het een vooraf gedefinieerde structuur voor het opslaan en ophalen van gegevens. Het binaire bestandsformaat maakt het 3DS-bestandsformaat sneller kleiner in vergelijking met op tekst gebaseerde bestandsformaten. Gegevens in een 3DS-bestand worden opgeslagen in de vorm van chunks.

### 3DS Chunk

Elk blok in een 3DS-bestand is een gegevensblok dat een ID, de lengte van het blok voor de locatie van het volgende blok en de gegevens zelf bevat. Met de chunk-ID kunnen lezers van het 3DS-bestandsformaat de blokken overslaan die ze niet herkennen. Het helpt ook bij de uitbreidbaarheid van het formaat. Elk blok slaat informatie op met betrekking tot vormen, verlichting en kijkinformatie die samen de scène weergeven. Chunks zijn gerangschikt in een hiërarchische structuur in een 3DS-bestand en lijken qua weergave op de XML-documentobjectboom.

**Chunk-ID:** De eerste twee bytes van een chunk vertegenwoordigen een chunk-identifier waarmee de bestandslezer kan beslissen of hij deze tijdens het lezen in overweging neemt of deze overslaat.

**Lengte van de chunk:** De Chunk-ID wordt gevolgd door een geheel getal van 4 bytes (in little-endian) dat staat voor de lengte van de chunk. Deze lengte omvat ook de lengte van de gegevens, de lengte van de subblokken en de header van 6 bytes.

**Payload:** De lengte van de chunk wordt gevolgd door daadwerkelijke bytes aan gegevens voor de chunk, gevolgd door de sub-chunks in dezelfde hiërarchische structuur die kan worden uitgebreid tot verschillende niveaus diep.

### Structuur van een Chunk

De hiërarchische structuur van een eenvoudige chunk ziet er als volgt uit:

**Een stuk**

|begin|eind|maat|naam
--- | --- | --- | ---
|0|1|2|Chunk-ID
|2|5|4|Volgende Chunk

Chunks hebben een hiërarchie opgelegd die wordt geïdentificeerd door hun ID. Een 3ds-bestand heeft de primaire chunk-ID 4D4Dh. Dit is altijd het eerste stuk van het bestand. Met in de primaire chunk zijn de belangrijkste chunks.

**Hoofdstukjes**

|id|Beschrijving
--- | ---
|3D3D|Begin van object mesh data.
|B000|Begin van keyframer-gegevens.

De Next Chunk-aanwijzer na het ID-blok wijst naar de volgende Main-chunk.
Direct na een Main chunk is er weer een chunk. Dit kan elk ander type chunk zijn dat is toegestaan binnen het bereik van de belangrijkste chunks.
Voor de Mesh-beschrijving (3D3D) kunnen ze elk veelvoud zijn van.

**Subchunks van 3D3D - Mesh Block**


|id|Beschrijving
--- | ---
|1100|onbekend
|1200|Achtergrondkleur.
|1201|onbekend
|1300|onbekend
|1400|onbekend
|1420|onbekend
|1450|onbekend
|1500|onbekend
|2100|Omgevingskleurenblok
|2200|mist?
|2201|mist?
|2210|mist?
|2300|onbekend
|3000|onbekend
|4000|Objectblok
|7001|onbekend
|AFFF|onbekend

**Subchunks van 4000 - Objectbeschrijvingsblok**
Het eerste item van Subchunk 4000 is een ASCIIZ-string van de objectnaam.
Onthoud dat een object een gaas, een licht of een camera kan zijn.

|id|Beschrijving
--- | ---
|4010|onbekend
|4012|schaduw?
|4100|Driehoekig polygoonobject
|4600|Licht
|4700|Camera

## Referenties

* [Geometrie bestandsindelingen - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32-htm.html)
* [3DS - Door Wikipedia](https://en.wikipedia.org/wiki/.3ds)
