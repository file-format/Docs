{
  "date": "2021-04-19",
  "keywords": [
"Blitz3D",
"b3d",
"fil",
"udvidelse",
"format",
"blitz3d spil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om B3D-filformat; bruges i blitz3d-spil og API'er, der kan åbne og skabe B3D-filer.",
  "title": "B3D - Blitz3D Entity Model File",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3-dad"
}
},
  "lastmod": "2021-04-19"
}

## Hvad er en B3D fil?

En fil med filtypenavnet .b3d er en modelfil, der bruges af Blitz3D, og som kan indeholde videospilmodeller for figurer, bygninger, terræn og andre objekter. Blitz3D er et programmeringssprog, der bruges til at skabe **blitz3d-spil**. Blitz3D er et kraftfuldt, fleksibelt og brugervenligt programmeringssprog designet til det ene formål at skrive videospil. Udviklerne kan skabe actionfyldte 3D-spil, 2D-puslespil, eventyr, RPGS, hvad som helst bare ved at bruge Blitz3D.

Blitz3D er baseret på BASIC programmeringssproget; som også er let at lære og bruge. Alle disse fakta gør Blitz ideel for både begyndere og mere erfarne programmører. Selvom funktionerne betragtes som noget forældede, end de findes i de fleste moderne 3D-motorer, bliver Blitz3D fortsat brugt af mange spilprogrammører verden over.

## Kort historie om Blitz3D

Blitz3D blev grundlæggende udgivet til Microsoft Windows-operativsystemet i september 2001 for at konkurrere med andre lignende spiludviklingssprog. Blitz3D var en opgraderet version i forhold til den tidligere 2D-motor BlitzBasic, som udvidede sit kommandosæt med tilføjelsen af en API til en DirectX 7-baseret 3D-motor. Blitz3D-brugerne bør også sammenligne BlitzMax, som er en senere motor fra BlitzBasic. BlitzMax er en kompleks, men mere kraftfuld version af Blitz3D, som understøtter objektorienterede programmeringssprog. Det er en opdateret grafik API, der passer bedre til Unicode-tegn, OpenGL og eksport til OSX og Linux i stedet for kun Windows.

## B3D eksempel
En b3d-fil, der indeholder 1 TEXS-chunk, 1 BRUS-chunk og 1 NODE-chunk, vil se sådan ud:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
Et simpelt, ikke-animerende og ikke-tekstureret mesh vil se sådan ud:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## Referencer
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

