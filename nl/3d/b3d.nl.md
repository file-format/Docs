{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over B3D-bestandsindeling; gebruikt in blitz3d-spellen en API's die B3D-bestanden kunnen openen en maken.",
  "title" :"B3D - Blitz3D-entiteitsmodelbestand",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Wat is een B3D-bestand?

Een bestand met de extensie .b3d is een modelbestand dat door Blitz3D wordt gebruikt en dat videogamemodellen kan bevatten voor personages, gebouwen, terrein en andere objecten. De Blitz3D is een programmeertaal die wordt gebruikt om **blitz3d-spellen** te maken. Blitz3D is een krachtige, flexibele en gebruiksvriendelijke programmeertaal die uitsluitend is ontworpen voor het schrijven van videogames. De ontwikkelaars kunnen 3D-games boordevol actie, 2D-puzzels, avonturen, RPGS, wat dan ook maken door gewoon Blitz3D te gebruiken.

De Blitz3D is gebaseerd op de programmeertaal BASIC; die ook gemakkelijk te leren en te gebruiken is. Al deze feiten maken Blitz ideaal voor zowel beginners als meer ervaren programmeurs. Hoewel het als enigszins verouderd wordt beschouwd dan in de meeste moderne 3D-engines, wordt Blitz3D nog steeds door veel gameprogrammeurs over de hele wereld gebruikt.

## Korte geschiedenis van Blitz3D

De Blitz3D werd in feite in september 2001 uitgebracht voor het Microsoft Windows-besturingssysteem om te concurreren met andere vergelijkbare talen voor het ontwikkelen van games. Blitz3D was een verbeterde versie ten opzichte van de eerdere 2D-engine BlitzBasic, die zijn commandoset uitbreidde met de toevoeging van een API voor een op DirectX 7 gebaseerde 3D-engine. De Blitz3D-gebruikers moeten ook BlitzMax vergelijken, een latere engine van BlitzBasic. De BlitzMax is een complexe maar krachtigere versie van Blitz3D, die objectgeoriënteerde programmeertalen ondersteunt. Het is een bijgewerkte grafische API die beter past bij Unicode-tekens, OpenGL en voor het exporteren naar OSX en Linux in plaats van alleen naar Windows.

## B3D-voorbeeld
Een b3d-bestand dat 1 TEXS-chunk, 1 BRUS-chunk en 1 NODE-chunk bevat, ziet er als volgt uit:

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
Een eenvoudig, niet-bewegend en niet-gestructureerd gaas ziet er als volgt uit:

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


## Referenties
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

