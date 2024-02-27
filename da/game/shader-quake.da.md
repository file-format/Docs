{
   "date":"2023-10-11",
   "keywords":[
"skygge",
"shader-fil",
"shader quake 3 engine shader fil",
"hvordan man åbner en shader-fil",
"fil",
"shader filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"SHADER-filformat - Quake 3 Engine Shader-fil",
   "description":"Lær om SHADER Quake 3 Engine Shader-filformat og API'er, der kan oprette og åbne SHADER-filer.",
   "linktitle":"SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake-da",
         "parent":"game"
}
},
   "lastmod":"2023-10-11"
}

## Hvad er SHADER fil?

SHADER-filformatet bruges i **Quake 3-motoren** til at definere shaders for teksturer og materialer i spillet. Shaders bruges til at specificere, hvordan en overflade skal gengives, herunder dens udseende, reflektionsevne, gennemsigtighed og andre visuelle egenskaber.

## Quake 3 Engine SHADER-fil

Her er en grundlæggende oversigt over struktur og syntaks for Quake 3 engine shader-fil:

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

I Quake 3 engine shader-fil kan du definere flere shaders, hver med sit eget sæt af egenskaber og stadier. Disse shaders bruges til at definere udseendet af forskellige teksturer og materialer i spilverdenen. Motoren bruger disse oplysninger til at gengive overflader med specificerede visuelle effekter og adfærd.

Shader-filer i Quake 3-motoren er simple tekstfiler, der indeholder instruktioner til, hvordan teksturer og materialer skal fremstå i spillet. Disse filer kan åbnes og redigeres med almindelig teksteditor og findes typisk i mappen **/scripts** i spillets .PK3-pakke.

## Quake 3 motor

Quake 3-motoren er meget indflydelsesrig og alsidig spilmotor udviklet af id Software. Det blev først introduceret med udgivelsen af spillet Quake III Arena i 1999 og er siden blevet brugt i forskellige andre spil. Motoren er kendt for sin avancerede grafik, multiplayer-muligheder og modificerbarhed.

Her er nogle nøglefunktioner og aspekter af Quake 3-motoren:

1.  **Graphics Engine:** Quake 3-motoren var kendt for sin banebrydende grafikteknologi på et tidspunkt. Den introducerede avancerede funktioner såsom buede overflader, shaders og dynamisk belysning, som var banebrydende i slutningen af 1990'erne.
    
2.  **Multiplayer Focus:** Quake 3 Arena blev primært designet som multiplayer first-person shooter. Motorens netværkskode og support til online multiplayer-spil var enestående, hvilket gjorde den til et populært valg til konkurrencedygtigt onlinespil.
    
3.  **Modificerbarhed:** Quake 3-motoren er kendt for sin modificerbarhed. id Software frigivet motorkildekode under open source GNU General Public License (GPL). Dette tilskyndede til oprettelse af adskillige mods og brugerdefinerede kort, hvilket førte til et levende modding-fællesskab.
    
4.  **Scripted Gameplay:** Motoren brugte script-baseret system til at definere spillets regler og adfærd, hvilket gør det relativt nemt for moddere og kortlæggere at skabe brugerdefinerede spiltilstande og unikke oplevelser.
    
5.  **Understøttelse af brugerdefineret indhold:** Quake 3's motor understøttede brugerdefineret indhold, inklusive teksturer, modeller og lydfiler, hvilket muliggjorde en høj grad af tilpasning i brugerskabte kort og mods.
    
6.  **Niveaudesign:** Motoren brugte børstebaseret niveaudesignsystem, hvor kort blev konstrueret ved at skære mellemrum ud fra solide børster. Denne tilgang var veldokumenteret og brugervenlig for niveaudesignere.


Gennem årene er Quake 3-motoren blevet brugt som grundlag for mange andre spil og mods, inklusive Return to Castle Wolfenstein, Star Wars Jedi Knight II: Jedi Outcast og Urban Terror blandt andre. Det efterlod varig arv i spiludviklingens verden og hjalp med at forme first-person shooter-genren. Mens nyere og mere avancerede motorer siden er dukket op, bliver Quake 3-motoren fortsat respekteret for sit bidrag til spilindustrien.

## Hvordan åbner jeg filen SHADER?

Programmer, der åbner eller refererer til SHADER filer inkluderer

- **id Software Quake 3** (betalt) til (Windows, Mac, Linux)
- Microsoft Notesblok
- Notesblok++
- Enhver teksteditor

## Andre SHADER-filer

Her er andre filtyper, der bruger filtypen **.shader**.

**Spilfiler**
- [SHADER - Godot Engine Shader File](/game/shader-godot/)
- [SHADER - Quake 3 Engine Shader File](/game/shader-quake/)
- [SHADER - Unity Shader Asset](/game/shader-unity/)

## Referencer
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

