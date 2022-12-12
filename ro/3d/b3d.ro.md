{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier B3D; folosit în jocurile blitz3d și API-urile care pot deschide și crea fișiere B3D.",
  "title" :"B3D - Fișier model de entitate Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Ce este un fișier B3D?

Un fișier cu extensia .b3d este un fișier model folosit de Blitz3D care poate conține modele de jocuri video pentru personaje, clădiri, teren și alte obiecte. Blitz3D este un limbaj de programare folosit pentru a crea **jocuri blitz3d**. Blitz3D este un limbaj de programare puternic, flexibil și ușor de utilizat, conceput pentru unicul scop de a scrie jocuri video. Dezvoltatorii pot crea jocuri 3D pline de acțiune, puzzle-uri 2D, aventuri, RPGS, orice, doar folosind Blitz3D.

Blitz3D se bazează pe limbajul de programare BASIC; care este, de asemenea, ușor de învățat și de utilizat. Toate aceste fapte fac din Blitz ideal atât pentru începători, cât și pentru programatorii mai experimentați. Deși caracteristicile sunt considerate oarecum învechite decât cele găsite în majoritatea motoarelor 3D moderne, Blitz3D continuă să fie folosit de mulți programatori de jocuri din întreaga lume.

## Scurt istoric al Blitz3D

Blitz3D a fost lansat practic pentru sistemul de operare Microsoft Windows în septembrie 2001, pentru a concura cu alte limbaje similare de dezvoltare a jocurilor. Blitz3D a fost o versiune actualizată față de motorul 2D anterior BlitzBasic, care și-a extins setul de comenzi cu adăugarea unui API pentru un motor 3D bazat pe DirectX 7. Utilizatorii Blitz3D ar trebui, de asemenea, să compare BlitzMax, care este un motor ulterior de BlitzBasic. BlitzMax este o versiune complexă, dar mai puternică a Blitz3D, care acceptă limbaje de programare orientate pe obiecte. Este un API grafic actualizat pentru a se potrivi mai bine cu caracterele Unicode, OpenGL și exportul către OSX și Linux în loc de numai Windows.

## Exemplu B3D
Un fișier b3d care conține 1 fragment TEXS, 1 fragment BRUS și 1 bucată NODE, va arăta astfel:

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
O plasă simplă, neanimată și fără textura va arăta astfel:

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


## Referințe
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

