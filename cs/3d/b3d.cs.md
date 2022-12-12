{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Zjistěte více o formátu souborů B3D; používaný v blitz3d hrách a rozhraních API, která mohou otevírat a vytvářet soubory B3D.",
  "title" :"B3D - Blitz3D Entity Model File",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Co je soubor B3D?

Soubor s příponou .b3d je soubor modelu používaný Blitz3D, který může obsahovat modely videoher pro postavy, budovy, terén a další objekty. Blitz3D je programovací jazyk používaný k vytváření **blitz3d her**. Blitz3D je výkonný, flexibilní a snadno použitelný programovací jazyk určený výhradně pro psaní videoher. Vývojáři mohou pomocí Blitz3D vytvářet akční 3D hry, 2D hlavolamy, dobrodružství, RPGS, cokoliv.

Blitz3D je založen na programovacím jazyce BASIC; který se také snadno učí a používá. Díky těmto všem skutečnostem je Blitz ideální pro začátečníky i zkušenější programátory. Ačkoli jsou jeho funkce považovány za poněkud zastaralé než ve většině moderních 3D enginů, Blitz3D je nadále používán mnoha herními programátory po celém světě.

## Stručná historie Blitz3D

Blitz3D byl v podstatě vydán pro operační systém Microsoft Windows v září 2001, aby konkuroval jiným podobným jazykům pro vývoj her. Blitz3D byla vylepšená verze dřívějšího 2D enginu BlitzBasic, která rozšířila svou sadu příkazů přidáním API pro 3D engine založený na DirectX 7. Uživatelé Blitz3D by také měli porovnat BlitzMax, což je pozdější engine od BlitzBasic. BlitzMax je komplexní, ale výkonnější verze Blitz3D, která podporuje objektově orientované programovací jazyky. Jedná se o aktualizované grafické rozhraní API, které lépe vyhovuje znakům Unicode, OpenGL a exportu do OSX a Linuxu namísto pouze Windows.

## Příklad B3D
Soubor b3d, který obsahuje 1 blok TEXS, 1 blok BRUS a 1 blok NODE, bude vypadat takto:

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
Jednoduchá síť bez animace a bez textury bude vypadat takto:

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


## Reference
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

