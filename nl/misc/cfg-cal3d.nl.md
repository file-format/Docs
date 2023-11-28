{
"datum": "27-09-2023",
  "keywords": [
"cfg",
"cfg-bestand",
"cfg cal3d-modelconfiguratiebestand",
"wat is een cfg-bestand",
"hoe cfg-bestand te openen",
"bestand",
"cfg-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CFG-bestandsindeling - Cal3D-modelconfiguratiebestand",
  "description":"Leer meer over het CFG Cal3D-modelconfiguratiebestandsformaat en API's waarmee CFG-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CFG Cal3D",
  "menu": {
    "docs": {
      "identifier": "misc-cfg-cal3d",
"parent" : "misc"
}
},
"laatste mod": "27-09-2023"
}

## Wat is een CFG-bestand?

Een Cal3D-modelconfiguratiebestand is een op tekst gebaseerd bestand dat wordt gebruikt door de Cal3D-bibliotheek, een open-source toolkit voor karakteranimatie. Dit bestand dient als blauwdruk voor het samenstellen van een driedimensionaal (3D) model. Het bevat verwijzingen naar verschillende componenten van het model, zoals de skeletstructuur, materialen, animaties en meer. In wezen fungeert het als een centraal document dat helpt bij het organiseren en definiëren van hoe alle onderdelen van het 3D-model in elkaar passen binnen het Cal3D-framework.

Cal3D is een skeletanimatiebibliotheek die vaak wordt gebruikt bij computergraphics en game-ontwikkeling. Om met Cal3D-modellen te werken, moet u doorgaans een configuratiebestand maken dat de structuur, materialen, animaties en andere kenmerken van het model beschrijft. Hieronder ziet u een voorbeeld van hoe een Cal3D-modelconfiguratiebestand eruit zou kunnen zien.

```
<MODEL>
  <HEADER MAGIC="C3D" VERSION="1050" />

  <!-- Skeleton -->
  <SKELETON>
    <BONE ID="0" NAME="Root">
      <TRANSLATION>0.0 0.0 0.0</TRANSLATION>
      <ROTATION>0.0 0.0 0.0</ROTATION>
      <SCALE>1.0 1.0 1.0</SCALE>
    </BONE>
    <!-- Add more bone definitions here -->
  </SKELETON>

  <!-- Mesh -->
  <MESH>
    <SUBMESH>
      <MATERIAL>MATERIAL_NAME</MATERIAL>
      <VERTEX>
        <!-- Vertex data for the first vertex -->
        <POSITION>0.0 0.0 0.0</POSITION>
        <NORMAL>0.0 0.0 1.0</NORMAL>
        <TEXCOORD>0.0 0.0</TEXCOORD>
        <!-- Add more vertices here -->
      </VERTEX>
      <FACE>
        <!-- Face data for the first face -->
        <VERTEXID>0 1 2</VERTEXID>
        <!-- Add more faces here -->
      </FACE>
      <!-- Add more submeshes here -->
    </SUBMESH>
  </MESH>

  <!-- Animation -->
  <ANIMATION>
    <SKELETON>
      <!-- Define animations and keyframes here -->
    </SKELETON>
  </ANIMATION>

</MODEL>
```

## Cal3D

Cal3D is een open-source karakteranimatiebibliotheek die wordt gebruikt bij 3D-computergraphics en game-ontwikkeling. Het biedt tools en functionaliteiten voor het maken en animeren van 3D-personages of -modellen. Cal3D wordt vaak gebruikt om levensechte karakteranimaties naar interactieve applicaties en games te brengen.

De belangrijkste kenmerken en componenten van Cal3D zijn onder meer:

1. **Mesh:** De mesh-component definieert de 3D-geometrie van een personage of object, inclusief hoekpunten, normalen en textuurcoördinaten. Het vormt de visuele weergave van het model.

2. **Skelet:** Cal3D maakt het mogelijk een skelethiërarchie voor personagemodellen te creëren. Dit skelet definieert de botstructuur en elk bot kan worden geassocieerd met een deel van het gaas. Skeletten zijn cruciaal voor het animeren van personages door botten te manipuleren.

3. **Materialen:** Materialen bepalen hoe het oppervlak van het model eruit moet zien wanneer het wordt gerenderd. Dit omvat informatie over texturen, shaders en andere weergave-eigenschappen.

4. **Animaties:** Cal3D ondersteunt verschillende animatietechnieken die op het skelet kunnen worden toegepast. Deze animaties bepalen hoe botten in de loop van de tijd bewegen om realistische karakteranimaties te creëren, zoals lopen, rennen of andere acties uitvoeren.

5. **Configuratiebestanden:** Om Cal3D effectief te kunnen gebruiken, worden modellen vaak vergezeld van configuratiebestanden in platte tekst. Deze bestanden beschrijven de structuur van het model, inclusief bothiërarchie, meshgegevens, materialen en animatie-informatie. Configuratiebestanden dienen als referentie voor Cal3D om het model correct te laden en ermee te communiceren.

## Bestandsformaten gebruikt door Cal3D

Cal3D gebruikt verschillende bestandsformaten voor verschillende doeleinden, zoals het opslaan van modelgegevens, animaties en configuratie-informatie. Hier zijn enkele van de veelgebruikte bestandsformaten die door Cal3D worden gebruikt:

1. **Cal3D binaire modelbestanden (.cmf):** Deze bestanden slaan de binaire weergave van 3D-modellen op, inclusief mesh-geometrie, bothiërarchie en materialen. CMF-bestanden worden gebruikt om Cal3D-modellen in applicaties efficiënt te laden en weer te geven.

1. **Cal3D XML-modelbestanden (.cmx):** XML-gebaseerde bestanden die de tekstuele weergave van Cal3D-modellen opslaan. Ze bevatten informatie over de structuur van het model, animaties, materialen en meer. [CMX](/nl/image/cmx/)-bestanden worden vaak gebruikt voor gemakkelijker leesbare bewerking en foutopsporing.

1. **Cal3D-animatiebestanden (.caf):** Deze bestanden slaan animatiegegevens op, inclusief keyframes en bottransformaties. CAF-bestanden zijn essentieel voor het definiëren hoe karakters of objecten binnen een Cal3D-model moeten bewegen en animeren.

1. **Cal3D Morph Target Files (.crf):** Wordt gebruikt om morph-doelen te definiëren, die gezichtsuitdrukkingen en andere niet-skeletvervormingen van de mesh mogelijk maken.

1. **Cal3D-materiaalbestanden (.cfm):** Deze bestanden slaan materiaalinformatie op voor Cal3D-modellen. Ze specificeren hoe het oppervlak van het model moet worden gearceerd, inclusief textuurreferenties, shaders en weergave-eigenschappen.

1. **Cal3D-skeletbestanden (.csf):** Skeletbestanden slaan informatie op over de bothiërarchie en structuur van een Cal3D-model. Ze definiëren hoe botten binnen het skelet zijn verbonden en onderhouden.

1. **Cal3D-configuratiebestanden (.cfg):** Deze tekstbestanden dienen als configuratiebestanden voor Cal3D-modellen. Ze bevatten verwijzingen naar verschillende componenten van het model, waaronder bothiërarchie, mesh-gegevens, materialen en animaties. Configuratiebestanden helpen Cal3D het model correct te laden en te gebruiken.

1. **Afbeeldingsformaten:** Hoewel niet specifiek voor Cal3D, zijn afbeeldingsbestandsformaten zoals [JPEG](/nl/image/jpeg/), [PNG](/nl/image/png/), [BMP](/nl/image/bmp/ ) of [TGA](/nl/image/tga/) worden vaak gebruikt voor texturen die worden toegepast op Cal3D-modellen.

## Hoe open je een CFG-bestand?

Programma's die CFG-bestanden openen omvatten

- Cal3dViewer
- Microsoft Kladblok
- Apple Teksteditor
- Elke teksteditor

## Andere CFG-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.cfg** gebruiken.

**Instellingen**
- [CFG - Celestia-configuratiebestand] (/nl/settings/cfg-celestia/)
- [CFG - Citrix-serververbindingsbestand](/nl/settings/cfg-citrix/)
- [CFG - MAME-configuratiebestand] (/nl/settings/cfg-mame/)
- [CFG - LightWave-configuratiebestand] (/nl/settings/cfg-lightwave/)

**Spel**
- [CFG - Wesnoth Markup Language-bestand] (/nl/game/cfg-wesnoth/)
- [CFG - MUGEN-configuratiebestand] (/nl/game/cfg-mugen/)
- [CFG - Bronengineconfiguratiebestand](/nl/game/cfg-sourceengine/)

**Systeem en Diversen**
- [CFG - CFG-bestand](/nl/system/cfg/)
- [CFG - Cal3D-modelconfiguratiebestand] (/nl/misc/cfg-cal3d/)

## Referenties
* [CAL3D](https://github.com/mp3butcher/Cal3D)
