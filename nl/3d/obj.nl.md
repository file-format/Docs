{
  "date" : "2019-10-11",
  "keywords" :[ "obj-bestand", "obj-bestandsindeling", "wat is een obj-bestand", "bestand", "obj-voorbeeld", "obj-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBJ-bestandsindeling",
  "description":"Meer informatie over OBJ-bestandsindelingen en API's die OBJ-bestanden kunnen openen en maken.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een OBJ-bestand?

**OBJ**-bestanden worden gebruikt door de toepassing Advanced Visualizer van Wavefront om de geometrische objecten te definiëren en op te slaan. Achterwaartse en voorwaartse overdracht van geometrische gegevens wordt mogelijk gemaakt via OBJ-bestanden. Zowel veelhoekige geometrie zoals punten, lijnen, textuurhoekpunten, vlakken als vrije-vormgeometrie (krommen en oppervlakken) worden ondersteund door het OBJ-formaat. Dit formaat ondersteunt geen animatie of informatie met betrekking tot licht en positie van scènes.

Een OBJ-bestand is meestal een eindproduct van het 3D-modelleringsproces dat wordt gegenereerd door een CAD (Computer Aided Design). De standaardvolgorde om hoekpunten op te slaan is tegen de klok in om expliciete declaratie van gezichtsnormalen te vermijden. Hoewel OBJ-bestanden schaalinformatie aangeven in een commentaarregel, zijn er nog geen eenheden gedeclareerd voor OBJ-coördinaten.

## Geschiedenis van het 3D OBJ-formaat

Wavefront Technologies heeft het OBJ-bestandsformaat gemaakt voor zijn Advanced Visualizer-toepassing om geometrische objecten en 3D-gegevens op te slaan. De versie 2.11 is vervangen door een nieuw gedocumenteerde versie 3. Het bestandsformaat is open en is geïmplementeerd door andere leveranciers voor hun 3D-grafische toepassing. Wavefront Technologies hield dit bestandsformaat open source en neutraal.

## OBJ-bestandsindeling

In 3D-objecten is het coderen van de oppervlaktegeometrie een uitdagende klus die het OBJ-bestandsformaat heel goed heeft gedaan. Dit formaat is vrij veelzijdig omdat het een aantal keuzes biedt om oppervlaktegeometrie te coderen. Hieronder volgen drie toegestane formaten met hun eigen voordelen en tekortkomingen:

### Tessellation met veelhoekige gezichten

Het OBJ-bestandsformaat stelt de gebruiker in staat om een 3D-modeloppervlak te mozaïeken met behulp van eenvoudige of complexe geometrische vormen. Voor het coderen van oppervlaktegeometrie van een model slaat een bestand de hoekpunten op en loodrecht op elke polygoon. Hoewel mozaïekpatroon de grofheid van het model vergroot, is het toch noodzakelijk om de juiste balans te vinden tussen de grootte van een bestand en de afdrukkwaliteit ervan.

### Curve in vrije vorm

Met de OBJ-bestandsindeling kunnen de door de gebruiker gedefinieerde vrije-vorm-oppervlakkrommen de oppervlaktegeometrie van een model specificeren. Omdat vrije-vormkrommen complexer zijn dan veelhoekige vlakken, omdat, met weinig wiskundige parameters, gebogen lijnen het best kunnen worden gedefinieerd door vrije-vormkrommen. Daarom, met minder gegevens in vergelijking met veelhoekige vlakverdelingen, werden vrije-vormcurven gebruikt om een hoogwaardige codering van elk 3D-model te genereren zonder de bestandsgrootte uit te breiden.

### Oppervlakken met vrije vorm

OBJ-bestandsindeling specificeert ook de betegeling van oppervlaktegeometrie met vrije-vorm oppervlaktepatches. Dit soort Freeform Surface Patches (NURBS) is zeer geschikt voor oppervlakken zonder starre radiale afmetingen zoals de carrosserie van een vrachtwagen, de vleugels van een helikopter of de romp van een boot. Het gebruik van vrije-vormoppervlakken is zeer voordelig omdat ze nauwkeuriger zijn om de bestandsgrootte bij hogere precisie kleiner te houden. Deze oppervlakken zijn een essentieel onderdeel van de lucht- en ruimtevaart- en auto-industrie waar de lage precisie meedogenloos is.

De volgende trefwoorden zijn gerangschikt op gegevenstype om oppervlaktegeometrie te definiëren.


|Elementen|Vrij-vorm kromme/oppervlaktelichaamverklaringen|Vrije-vorm kromme/oppervlakte-attributen
---|---|---|
|p|Punt|parm|Parameterwaarden|deg|Grade
|l|Lijn|trim|Buitenste trimlus|bmat|Basismatrix
|f|Gezicht|gat|Binnenste trimlus|stap|Stapmaat
|curv|Curve|scrv|Speciale curve|cstype|Curve of oppervlaktetype
|curv2|2D curve|sp|Speciaal punt|**Connectiviteit en groepering van oppervlakken**
|surf|Surface|end|End statement|con|connect
|**Weergave-/weergavekenmerken**|g|Groepsnaam
|bevel|Afschuining interpolatie|shadow_obj|Schaduw gieten|s|Verzachtende groep
|lod|Niveau van detail|trace_obj|Ray tracing|mg|Groep samenvoegen
|d_interp|Interpolatie oplossen|ctech|Krommebenadering techniek|o|Objectnaam
|c_interp|Kleurinterpolatie|stech|Techniek voor oppervlaktebenadering|
|usemtl|Materiaalnaam|mtllib|Materiaalbibliotheek|
|**Geometrische hoekpunten**|
|v|Geometrische hoekpunten|vn|Vertex normalen|
|vt|Textuur hoekpunten|vp|Parameter ruimte hoekpunten|

### Kleur en Textuur

Met het OBJ-bestand kan kleur- en textuurinformatie worden opgeslagen in een bijbehorende bestandsindeling, de Material Template Library (MTL). Geometrische modellen in meerdere kleuren worden gerenderd door deze twee bestanden samen te gebruiken. MTL-bestanden zijn ASCII-gebaseerd en vergemakkelijken de computerweergave door lichtreflecterende eigenschappen van een oppervlak te beschrijven met behulp van het model van Phong-reflectie. De standaard is overgenomen door een groot aantal softwareleveranciers die zijn voordeel halen uit de uitwisseling van materialen. Het MTL-formaat is enigszins verouderd omdat het geen ondersteuning biedt voor de nieuwste technologieën zoals spiegel- en parallax-kaarten.

## Referenties

* [Wavefront .obj-bestand](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

