{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tudjon meg többet a B3D fájlformátumról; Blitz3d játékokban és API-kban használatos, amelyek képesek megnyitni és létrehozni B3D fájlokat.",
  "title" :"B3D – Blitz3D entitásmodellfájl",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Mi az a B3D fájl?

A .b3d kiterjesztésű fájl a Blitz3D által használt modellfájl, amely videojáték-modelleket tartalmazhat karakterekhez, épületekhez, domborzathoz és egyéb objektumokhoz. A Blitz3D egy programozási nyelv, amelyet **blitz3d játékok** létrehozására használnak. A Blitz3D egy erőteljes, rugalmas és könnyen használható programozási nyelv, amelyet kizárólag videojátékok írására terveztek. A fejlesztők akciódús 3D-s játékokat, 2D-s fejtörőket, kalandokat, RPGS-t, bármit készíthetnek a Blitz3D használatával.

A Blitz3D a BASIC programozási nyelven alapul; amely szintén könnyen megtanulható és használható. Mindezek miatt a Blitz ideális kezdőknek és tapasztaltabb programozóknak egyaránt. Bár a Blitz3D funkcióit némileg elavultnak tekintik, mint a legtöbb modern 3D motorban, a Blitz3D-t továbbra is sok játékprogramozó használja világszerte.

## A Blitz3D rövid története

A Blitz3D-t alapvetően 2001 szeptemberében adták ki Microsoft Windows operációs rendszerre, hogy felvegyék a versenyt más hasonló játékfejlesztő nyelvekkel. A Blitz3D a korábbi 2D motor, a BlitzBasic továbbfejlesztett verziója volt, amely kibővítette a parancskészletét egy API hozzáadásával a DirectX 7 alapú 3D motorhoz. A Blitz3D felhasználóknak össze kell hasonlítaniuk a BlitzMax-ot is, amely a BlitzBasic későbbi motorja. A BlitzMax a Blitz3D összetett, de erősebb változata, amely támogatja az objektumorientált programozási nyelveket. Ez egy frissített grafikus API, amely jobban megfelel a Unicode karaktereknek, az OpenGL-nek, valamint az OSX-re és Linuxra való exportálásra a Windows helyett.

## B3D példa
Az 1 TEXS darabot, 1 BRUS darabot és 1 NODE darabot tartalmazó b3d fájl így fog kinézni:

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
Egy egyszerű, nem animáló és nem texturált háló így fog kinézni:

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


## Hivatkozások
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

