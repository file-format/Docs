{
"date":"2023-10-11",
   "keywords":[
"schaduwer",
"shaderbestand",
"shader quake 3 engine shader-bestand",
"hoe een shader-bestand openen",
"bestand",
"shader bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"SHADER-bestandsindeling - Quake 3 Engine Shader-bestand",
   "description":"Leer meer over het SHADER Quake 3 Engine Shader-bestandsformaat en API's die SHADER-bestanden kunnen maken en openen.",
"linktitle":" SHADER Aardbeving",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake",
"parent":"spel"
}
},
"lastmod":"2023-10-11"
}

## Wat is een SHADER-bestand?

Het SHADER-bestandsformaat wordt gebruikt in de **Quake 3-engine** om shaders voor texturen en materialen in het spel te definiëren. Shaders worden gebruikt om te specificeren hoe een oppervlak moet worden weergegeven, inclusief het uiterlijk, de reflectiviteit, de transparantie en andere visuele eigenschappen.

## Quake 3 Engine SHADER-bestand

Hier is een basisoverzicht van de structuur en syntaxis van het Quake 3 engine shader-bestand:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

In het Quake 3 engine shader-bestand kun je meerdere shaders definiëren, elk met zijn eigen set eigenschappen en fasen. Deze shaders worden gebruikt om het uiterlijk van verschillende texturen en materialen in de gamewereld te definiëren. De engine gebruikt deze informatie om oppervlakken weer te geven met gespecificeerde visuele effecten en gedrag.

Shader-bestanden in de Quake 3-engine zijn eenvoudige tekstbestanden die instructies bevatten over hoe texturen en materialen in het spel moeten verschijnen. Deze bestanden kunnen worden geopend en bewerkt met een gewone teksteditor en zijn doorgaans te vinden in de map **"/scripts"** in het .PK3-pakket van de game.

## Quake 3-motor

De Quake 3-engine is een zeer invloedrijke en veelzijdige game-engine, ontwikkeld door id Software. Het werd voor het eerst geïntroduceerd met de release van de game "Quake III Arena" in 1999 en is sindsdien in verschillende andere games gebruikt. De engine staat bekend om zijn geavanceerde graphics, multiplayer-mogelijkheden en aanpasbaarheid.

Hier zijn enkele belangrijke kenmerken en aspecten van de Quake 3-engine:

1. **Grafische engine:** De Quake 3-engine stond destijds bekend om zijn geavanceerde grafische technologie. Het introduceerde geavanceerde functies zoals gebogen oppervlakken, shaders en dynamische verlichting, die eind jaren negentig baanbrekend waren.
    





2. **Multiplayerfocus:** Quake 3 Arena is in de eerste plaats ontworpen als first-person shooter voor meerdere spelers. De netwerkcode en ondersteuning van de engine voor online multiplayer-gaming waren uitzonderlijk, waardoor het een populaire keuze was voor competitief online spelen.
    





3. **Aanpasbaarheid:** De Quake 3-engine staat bekend om zijn aanpasbaarheid. id Software heeft de broncode van de engine vrijgegeven onder open-source GNU General Public License (GPL). Dit stimuleerde de creatie van talloze mods en aangepaste kaarten, wat leidde tot een levendige modding-gemeenschap.
    





4. **Gescripte gameplay:** De engine gebruikte een op scripts gebaseerd systeem om spelregels en gedrag te definiëren, waardoor het voor modders en mappers relatief eenvoudig werd om aangepaste spelmodi en unieke ervaringen te creëren.
    





5. **Ondersteuning voor aangepaste inhoud:** De engine van Quake 3 ondersteunde aangepaste inhoud, inclusief texturen, modellen en geluidsbestanden, wat een hoge mate van aanpassing mogelijk maakte in door gebruikers gemaakte kaarten en mods.
    





6. **Niveauontwerp:** De engine maakte gebruik van een op penseel gebaseerd niveauontwerpsysteem, waarbij kaarten werden geconstrueerd door spaties uit vaste penselen te snijden. Deze aanpak was goed gedocumenteerd en gebruiksvriendelijk voor levelontwerpers.


Door de jaren heen is de Quake 3-engine gebruikt als basis voor vele andere games en mods, waaronder onder meer 'Return to Castle Wolfenstein', 'Star Wars Jedi Knight II: Jedi Outcast' en 'Urban Terror'. Het heeft een blijvende erfenis nagelaten in de wereld van game-ontwikkeling en heeft bijgedragen aan het vormgeven van het first-person shooter-genre. Hoewel er sindsdien nieuwere en geavanceerdere motoren zijn verschenen, wordt de Quake 3-engine nog steeds gerespecteerd vanwege zijn bijdrage aan de game-industrie.

## Hoe open je een SHADER-bestand?

Programma's die SHADER-bestanden openen of ernaar verwijzen, omvatten

- **id Software Quake 3** (betaald) voor (Windows, Mac, Linux)
- Microsoft Kladblok
- Kladblok++
- Elke teksteditor

## Andere SHADER-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.shader** gebruiken.

**Spelbestanden**
- [SHADER - Godot Engine Shader-bestand] (/nl/game/shader-godot/)
- [SHADER - Quake 3 Engine Shader-bestand](/nl/game/shader-quake/)
- [SHADER - Unity Shader-item](/nl/game/shader-unity/)

## Referenties
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

