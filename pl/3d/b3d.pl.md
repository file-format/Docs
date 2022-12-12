{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików B3D; używany w grach blitz3d i interfejsach API, które mogą otwierać i tworzyć pliki B3D.",
  "title" :"B3D - Plik modelu jednostki Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Czym jest plik B3D?

Plik z rozszerzeniem .b3d to plik modelu używany przez Blitz3D, który może zawierać modele gier wideo dla postaci, budynków, terenu i innych obiektów. Blitz3D to język programowania używany do tworzenia **gier blitz3d**. Blitz3D to potężny, elastyczny i łatwy w użyciu język programowania przeznaczony wyłącznie do pisania gier wideo. Programiści mogą tworzyć pełne akcji gry 3D, układanki 2D, przygody, gry RPG, cokolwiek tylko za pomocą Blitz3D.

Blitz3D jest oparty na języku programowania BASIC; który jest również łatwy do nauczenia się i użytkowania. Te wszystkie fakty sprawiają, że Blitz jest idealny zarówno dla początkujących, jak i bardziej doświadczonych programistów. Chociaż jego funkcje są uważane za nieco przestarzałe niż w większości nowoczesnych silników 3D, Blitz3D jest nadal używany przez wielu programistów gier na całym świecie.

## Krótka historia Blitz3D

Blitz3D został zasadniczo wydany dla systemu operacyjnego Microsoft Windows we wrześniu 2001 roku, aby konkurować z innymi podobnymi językami do tworzenia gier. Blitz3D był ulepszoną wersją wcześniejszego silnika 2D BlitzBasic, który rozszerzył swój zestaw poleceń o interfejs API dla silnika 3D opartego na DirectX 7. Użytkownicy Blitz3D powinni również porównać BlitzMax, który jest późniejszym silnikiem BlitzBasic. BlitzMax to złożona, ale potężniejsza wersja Blitz3D, która obsługuje języki programowania zorientowane obiektowo. Jest to zaktualizowany graficzny interfejs API, aby lepiej pasował do znaków Unicode, OpenGL i eksportował do systemów OSX i Linux zamiast tylko do systemu Windows.

## Przykład B3D
Plik b3d zawierający 1 fragment TEXS, 1 fragment BRUS i 1 fragment NODE będzie wyglądał następująco:

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
Prosta, nieanimowana i nieteksturowana siatka będzie wyglądać tak:

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


## Bibliografia
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

