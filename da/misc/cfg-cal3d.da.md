{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg fil",
"cfg cal3d model konfigurationsfil",
"hvad er en cfg-fil",
"hvordan man åbner cfg fil",
"fil",
"cfg filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG-filformat - Cal3D-modelkonfigurationsfil",
  "description": "Lær om CFG Cal3D Model Configuration File format og API'er, der kan oprette og åbne CFG filer.",
  "linktitle": "CFG Cal3D",
  "menu": {
    "docs": {
      "identifier": "misc-cfg-cal3d-da",
      "parent": "misc"
}
},
  "lastmod": "2023-09-27"
}

## Hvad er CFG fil?

En Cal3D Model Configuration File er en tekstbaseret fil, der bruges af Cal3D-biblioteket, som er et open source-værktøjssæt til karakteranimation. Denne fil tjener som en plan for at samle en tredimensionel (3D) model. Den indeholder referencer til forskellige komponenter i modellen, såsom skeletstrukturen, materialer, animationer og mere. Grundlæggende fungerer det som et centralt dokument, der hjælper med at organisere og definere, hvordan alle dele af 3D-modellen passer sammen inden for Cal3D-rammen.

Cal3D er et skeletanimationsbibliotek, der ofte bruges i computergrafik og spiludvikling. For at arbejde med Cal3D-modeller skal du typisk oprette en konfigurationsfil, der beskriver modellens struktur, materialer, animationer og andre attributter. Nedenfor er et eksempel på, hvordan en Cal3D-modelkonfigurationsfil kan se ud.

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

Cal3D er et open source-figuranimationsbibliotek, der bruges i 3D computergrafik og spiludvikling. Det giver værktøjer og funktionaliteter til at skabe og animere 3D-karakterer eller -modeller. Cal3D bruges ofte til at bringe naturtro karakteranimationer til interaktive applikationer og spil.

Nøglefunktioner og komponenter i Cal3D omfatter:

1. **Mesh:** Mesh-komponenten definerer 3D-geometrien af en karakter eller et objekt, inklusive hjørner, normaler og teksturkoordinater. Det danner den visuelle repræsentation af modellen.

2. **Skelet:** Cal3D tillader oprettelsen af et skelethierarki for karaktermodeller. Dette skelet definerer knoglestrukturen, og hver knogle kan forbindes med en del af nettet. Skeletter er afgørende for at animere karakterer ved at manipulere knogler.

3. **Materialer:** Materialer definerer, hvordan overfladen af modellen skal se ud, når den gengives. Dette inkluderer oplysninger om teksturer, skyggere og andre gengivelsesegenskaber.

4. **Animationer:** Cal3D understøtter forskellige animationsteknikker, der kan anvendes på skelettet. Disse animationer definerer, hvordan knogler bevæger sig over tid for at skabe realistiske karakteranimationer, såsom at gå, løbe eller udføre andre handlinger.

5. **Konfigurationsfiler:** For at bruge Cal3D effektivt, er modeller ofte ledsaget af konfigurationsfiler i almindeligt tekstformat. Disse filer beskriver modellens struktur, herunder knoglehierarki, maskedata, materialer og animationsoplysninger. Konfigurationsfiler tjener som referencer for Cal3D til korrekt indlæsning og interaktion med modellen.

## Filformater brugt af Cal3D

Cal3D bruger flere filformater til forskellige formål, såsom lagring af modeldata, animationer og konfigurationsoplysninger. Her er nogle af de almindelige filformater, der bruges af Cal3D:

1. **Cal3D binære modelfiler (.cmf):** Disse filer gemmer den binære repræsentation af 3D-modeller, inklusive mesh-geometri, knoglehierarki og materialer. CMF-filer bruges til effektivt at indlæse og gengive Cal3D-modeller i applikationer.

1. **Cal3D XML-modelfiler (.cmx):** XML-baserede filer, der gemmer den tekstmæssige repræsentation af Cal3D-modeller. De indeholder information om modellens struktur, animationer, materialer og meget mere. [CMX](/image/cmx/) filer bruges ofte til lettere menneskelig læsbar redigering og fejlretning.

1. **Cal3D-animationsfiler (.caf):** Disse filer gemmer animationsdata, inklusive keyframes og knogletransformationer. CAF-filer er afgørende for at definere, hvordan karakterer eller objekter skal bevæge sig og animere i en Cal3D-model.

1. **Cal3D Morph Target Files (.crf):** Bruges til at definere morph-mål, som tillader ansigtsudtryk og andre ikke-skeletale deformationer af nettet.

1. **Cal3D-materialefiler (.cfm):** Disse filer gemmer materialeoplysninger for Cal3D-modeller. De specificerer, hvordan modellens overflade skal skygges, herunder teksturreferencer, shaders og gengivelsesegenskaber.

1. **Cal3D Skeleton Files (.csf):** Skeleton files store information about the bone hierarchy and structure of a Cal3D model. They define how bones are connected and parented within the skeleton.

1. **Cal3D-konfigurationsfiler (.cfg):** Disse almindelige tekstfiler fungerer som konfigurationsfiler til Cal3D-modeller. De indeholder referencer til forskellige komponenter i modellen, herunder knoglehierarki, maskedata, materialer og animationer. Konfigurationsfiler hjælper Cal3D med at indlæse og bruge modellen korrekt.

1. **Billedformater:** Selvom de ikke er specifikke for Cal3D, bruges billedfilformater som [JPEG](/image/jpeg/), [PNG](/image/png/), [BMP](/image/bmp/) eller [TGA](/image/tga/) almindeligvis til teksturer anvendt på Cal3D-modeller .

## Hvordan åbner jeg filen CFG?

Programmer, der åbner CFG filer inkluderer

- Cal3dViewer
- Microsoft Notesblok
- Apple TextEdit
- Enhver teksteditor

## Andre CFG-filer

Her er andre filtyper, der bruger filtypen **.cfg**.

**Indstillinger**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spil**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System og diverse**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Referencer
* [CAL3D](https://github.com/mp3butcher/Cal3D)
