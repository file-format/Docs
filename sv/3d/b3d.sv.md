{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig om B3D-filformat; används i blitz3d-spel och API:er som kan öppna och skapa B3D-filer.",
  "title" :"B3D - Blitz3D Entity Model File",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Vad är en B3D fil?

En fil med tillägget .b3d är en modellfil som används av Blitz3D och som kan innehålla videospelsmodeller för karaktärer, byggnader, terräng och andra objekt. Blitz3D är ett programmeringsspråk som används för att skapa **blitz3d-spel**. Blitz3D är ett kraftfullt, flexibelt och lättanvänt programmeringsspråk designat för det enda syftet att skriva videospel. Utvecklarna kan skapa actionspäckade 3D-spel, 2D-pusselspel, äventyr, RPGS, vad som helst bara genom att använda Blitz3D.

Blitz3D är baserad på programmeringsspråket BASIC; som också är lätt att lära sig och använda. Alla dessa fakta gör Blitz idealisk för både nybörjare och mer erfarna programmerare. Även om funktionerna anses vara något föråldrade än de som finns i de flesta moderna 3D-motorer, fortsätter Blitz3D att användas av många spelprogrammerare över hela världen.

## Kort historia om Blitz3D

Blitz3D släpptes i princip för Microsoft Windows operativsystem i september 2001, för att konkurrera med andra liknande spelutvecklingsspråk. Blitz3D var en uppgraderad version jämfört med den tidigare 2D-motorn BlitzBasic, som utökade sin kommandouppsättning med tillägget av ett API för en DirectX 7-baserad 3D-motor. Blitz3D-användarna bör också jämföra BlitzMax, som är en senare motor från BlitzBasic. BlitzMax är en komplex men kraftfullare version av Blitz3D, som stöder objektorienterade programmeringsspråk. Det är ett uppdaterat grafik-API för att bättre passa Unicode-tecken, OpenGL och export till OSX och Linux istället för bara Windows.

## B3D-exempel
En b3d-fil som innehåller 1 TEXS-chunk, 1 BRUS-chunk och 1 NODE-chunk kommer att se ut så här:

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
Ett enkelt, icke-animerande och icke-texturerat mesh kommer att se ut så här:

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


## Referenser
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

