{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-fil",
"cfg cal3d modell konfigurationsfil",
"vad är en cfg-fil",
"hur man öppnar cfg-fil",
"fil",
"cfg filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG-filformat - Cal3D-modellkonfigurationsfil",
  "description":"Läs mer om CFG Cal3D Model Configuration File format och API:er som kan skapa och öppna CFG-filer.",
"linktitle": "CFG Cal3D",
  "menu": {
    "docs": {
      "identifier": "misc-cfg-cal3d",
      "parent": "misc"
}
},
"lastmod": "2023-09-27"
}

## Vad är CFG fil?

En Cal3D Model Configuration File är en textbaserad fil som används av Cal3D-biblioteket, som är en öppen källkodsverktygslåda för karaktärsanimering. Den här filen fungerar som en ritning för att montera en tredimensionell (3D) modell. Den innehåller referenser till olika komponenter i modellen, såsom skelettets struktur, material, animationer och mer. I huvudsak fungerar det som ett centralt dokument som hjälper till att organisera och definiera hur alla delar av 3D-modellen passar ihop inom Cal3D-ramverket.

Cal3D är ett skelettanimationsbibliotek som ofta används i datorgrafik och spelutveckling. För att arbeta med Cal3D-modeller behöver du vanligtvis skapa en konfigurationsfil som beskriver modellens struktur, material, animationer och andra attribut. Nedan är ett exempel på hur en Cal3D-modellkonfigurationsfil kan se ut.

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

Cal3D är ett bibliotek med öppen källkod för karaktärsanimationer som används i 3D-datorgrafik och spelutveckling. Den tillhandahåller verktyg och funktioner för att skapa och animera 3D-karaktärer eller modeller. Cal3D används ofta för att ge verklighetstrogna karaktärsanimationer till interaktiva applikationer och spel.

Nyckelfunktioner och komponenter i Cal3D inkluderar:

1. **Mesh:** Mesh-komponenten definierar 3D-geometrin för en karaktär eller ett objekt, inklusive hörn, normaler och texturkoordinater. Det bildar den visuella representationen av modellen.

2. **Skeleton:** Cal3D tillåter skapandet av en skeletthierarki för karaktärsmodeller. Detta skelett definierar benstrukturen, och varje ben kan associeras med en del av nätet. Skelett är avgörande för att animera karaktärer genom att manipulera ben.

3. **Material:** Material definierar hur ytan på modellen ska se ut när den renderas. Detta inkluderar information om texturer, skuggningar och andra renderingsegenskaper.

4. **Animationer:** Cal3D stöder olika animationstekniker som kan appliceras på skelettet. Dessa animationer definierar hur ben rör sig över tiden för att skapa realistiska karaktärsanimationer, som att gå, springa eller utföra andra åtgärder.

5. **Konfigurationsfiler:** För att använda Cal3D effektivt, åtföljs modeller ofta av konfigurationsfiler i vanligt textformat. Dessa filer beskriver modellens struktur, inklusive benhierarki, nätdata, material och animationsinformation. Konfigurationsfiler fungerar som referenser för Cal3D för att korrekt ladda och interagera med modellen.

## Filformat som används av Cal3D

Cal3D använder flera filformat för olika ändamål, som att lagra modelldata, animationer och konfigurationsinformation. Här är några av de vanliga filformaten som används av Cal3D:

1. **Cal3D binära modellfiler (.cmf):** Dessa filer lagrar den binära representationen av 3D-modeller, inklusive nätgeometri, benhierarki och material. CMF-filer används för att effektivt ladda och rendera Cal3D-modeller i applikationer.

1. **Cal3D XML-modellfiler (.cmx):** XML-baserade filer som lagrar textrepresentationen av Cal3D-modeller. De innehåller information om modellens struktur, animationer, material med mera. [CMX](/sv/image/cmx/)-filer används ofta för lättare läsbar redigering och felsökning.

1. **Cal3D-animationsfiler (.caf):** Dessa filer lagrar animationsdata, inklusive nyckelbildrutor och bentransformationer. CAF-filer är viktiga för att definiera hur karaktärer eller objekt ska röra sig och animera i en Cal3D-modell.

1. **Cal3D Morph Target Files (.crf):** Används för att definiera morph-mål, som tillåter ansiktsuttryck och andra icke-skelettdeformationer av nätet.

1. **Cal3D-materialfiler (.cfm):** Dessa filer lagrar materialinformation för Cal3D-modeller. De anger hur modellens yta ska skuggas, inklusive texturreferenser, skuggningar och renderingsegenskaper.

1. **Cal3D Skeleton Files (.csf):** Skelettfiler lagrar information om benhierarkin och strukturen för en Cal3D-modell. De definierar hur ben är sammankopplade och föräldrade i skelettet.

1. **Cal3D-konfigurationsfiler (.cfg):** Dessa vanliga textfiler fungerar som konfigurationsfiler för Cal3D-modeller. De innehåller referenser till olika komponenter i modellen, inklusive benhierarki, nätdata, material och animationer. Konfigurationsfiler hjälper Cal3D att ladda och använda modellen korrekt.

1. **Bildformat:** Även om de inte är specifika för Cal3D, bildfilformat som [JPEG](/sv/image/jpeg/), [PNG](/sv/image/png/), [BMP](/sv/image/bmp/ ), eller [TGA](/sv/image/tga/) används ofta för texturer som appliceras på Cal3D-modeller.

## Hur öppnar man filen CFG?

Program som öppnar CFG-filer inkluderar

- Cal3dViewer
- Microsoft Notepad
- Apple TextEdit
- Vilken textredigerare som helst

## Andra CFG-filer

Här är andra filtyper som använder filtillägget **.cfg**.

**Inställningar**
- [CFG - Celestia-konfigurationsfil](/sv/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/sv/settings/cfg-citrix/)
- [CFG - MAME-konfigurationsfil](/sv/settings/cfg-mame/)
- [CFG - LightWave-konfigurationsfil](/sv/settings/cfg-lightwave/)

**Spel**
- [CFG - Wesnoth Markup Language File](/sv/game/cfg-wesnoth/)
- [CFG - MUGEN-konfigurationsfil](/sv/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/sv/game/cfg-sourceengine/)

**System & Övrigt**
- [CFG - CFG-fil](/sv/system/cfg/)
- [CFG - Cal3D Model Configuration File](/sv/misc/cfg-cal3d/)

## Referenser
* [CAL3D](https://github.com/mp3butcher/Cal3D)
