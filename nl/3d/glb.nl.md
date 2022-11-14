{
  "date" : "2019-12-03",
  "keywords" :[ "GLB", "bestand", "formaat", "bestandstype", "extensie", "wat is een GLB-bestand?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Meer informatie over de GLB-bestandsindeling en API's die GLB-bestanden kunnen openen en maken.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Wat is een GLB-bestand?

GLB is de binaire bestandsindeling van 3D-modellen die zijn opgeslagen in het GL-transmissieformaat ([glTF](/nl/3d/gltf/)). Informatie over 3D-modellen zoals knooppunthiërarchie, camera's, materialen, animaties en meshes in binair formaat. Deze binaire indeling slaat het glTF-item (JSON, .bin en afbeeldingen) op in een binaire blob. Het vermijdt ook het probleem van een toename van de bestandsgrootte die optreedt in het geval van glTF. Het GLB-bestandsformaat resulteert in compacte bestandsgroottes, snel laden, volledige 3D-scèneweergave en uitbreidbaarheid voor verdere ontwikkeling. Het formaat gebruikt model/gltf-binary als MIME-type.

## GLB-bestandsindeling - Meer informatie

De door glTF gebruikte methoden voor het afleveren van inhoud resulteren in extra verwerking om de base-64-gecodeerde binaire gegevens te decoderen en vergroten ook de bestandsgrootte met 33%. Deze leveringsmethoden, die hebben bijgedragen aan de vorming van het GLB-bestandsformaat, omvatten:

* glTF JSON verwijst naar externe binaire gegevens (geometrie, keyframes, skins) en afbeeldingen.
* glTF JSON sluit base64-gecodeerde binaire gegevens en afbeeldingen inline in met behulp van gegevens-URI's.

GLB als containerformaat is geïntroduceerd als binair bestandsformaat voor weergave van glTF-activa in een binaire blob om de problemen veroorzaakt door glTF te voorkomen. GLB-bestandsindeling [specificaties](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification) moet worden verwezen voor elke lezer/schrijver-implementatie van hetzelfde voor toepassingsontwikkeling .

## GLB-bestandsstructuur

Het GLB-bestandsformaat is gebaseerd op little endian en de structuur laat zien dat het het volgende bevat:

* Een preambule van 12 bytes, getiteld de header.
* Een of meer chunks die JSON-inhoud en binaire gegevens bevatten.

#### GLB-koptekst

De header van de GLB-bestandsindeling bestaat uit drie 4-byte-items:

* uint32 magie - magie is gelijk aan 0x46546C67. Het is een ASCII-tekenreeks glTF en kan worden gebruikt om gegevens te identificeren als binaire glTF
* uint32-versie - geeft de versie van het binaire glTF-containerformaat aan
* uin32-lengte - de totale lengte van de binaire glTF, inclusief header en alle chunks in bytes

#### Brokken

Elke chunk in een GLB-bestand heeft de volgende structuur:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - lengte van chunkData in bytes
* `chunkType` - geeft het type chunk aan
* `chunkData` - binaire lading van chunk

waar de chunk-types zijn:

|# |Chunktype|ASCII|Beschrijving|Voorvallen
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Gestructureerde JSON-inhoud|1
|2.|0x004E4942|BIN|Binaire buffer|0 of 1

Het begin en einde van elk blok moet worden uitgelijnd met een grens van 4 bytes en voor dit doel moet opvulling worden gebruikt.

##### Gestructureerde JSON-inhoud

Dit zou het allereerste deel van binaire glTF-activa moeten zijn en stelt de implementatie in staat om geleidelijk bronnen uit volgende delen op te halen. Dit biedt ook de mogelijkheid om alleen een geselecteerde subset van bronnen van een binair glTF-item te lezen, zoals de grofste LOD van een mesh. Om aan de uitlijningsvereisten te voldoen, moet dit blok worden opgevuld met achterliggende spatietekens (0x20).

##### Binaire buffer #####

Dit blok bevat de binaire lading voor geometrie, animatiesleutelframes, skins en afbeeldingen. Het moet het tweede deel van het binaire glTF-activum zijn en moet worden opgevuld met nullen (0x00) om aan de uitlijningsvereisten te voldoen.

## Referenties ##

* [GLB-bestandsformaatspecificaties - Khronos](/nl/3D/GLTF/)

