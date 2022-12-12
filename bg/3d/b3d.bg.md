{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за файловия формат B3D; използва се в blitz3d игри и API, които могат да отварят и създават B3D файлове.",
  "title" :"B3D – Blitz3D файл с модел на обект",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Какво е B3D файл?

Файл с разширение .b3d е файл с модел, използван от Blitz3D, който може да съдържа модели на видеоигри за герои, сгради, терен и други обекти. Blitz3D е език за програмиране, използван за създаване на **blitz3d игри**. Blitz3D е мощен, гъвкав и лесен за използване език за програмиране, създаден с единствената цел да пише видео игри. Разработчиците могат да създават изпълнени с екшън 3D игри, 2D пъзели, приключения, ролеви игри, каквото и да е само с помощта на Blitz3D.

Blitz3D е базиран на езика за програмиране BASIC; което също е лесно за научаване и използване. Всички тези факти правят Blitz идеален както за начинаещи, така и за по-опитни програмисти. Въпреки че неговите функции се считат за малко остарели в сравнение с повечето съвременни 3D машини, Blitz3D продължава да се използва от много програмисти на игри по целия свят.

## Кратка история на Blitz3D

Blitz3D беше основно пуснат за операционната система Microsoft Windows през септември 2001 г., за да се конкурира с други подобни езици за разработка на игри. Blitz3D беше подобрена версия спрямо по-ранния 2D двигател BlitzBasic, който разшири своя набор от команди с добавяне на API за базиран на DirectX 7 3D двигател. Потребителите на Blitz3D трябва също да сравнят BlitzMax, който е по-късен двигател от BlitzBasic. BlitzMax е сложна, но по-мощна версия на Blitz3D, която поддържа обектно-ориентирани езици за програмиране. Това е актуализиран графичен API, за да отговаря по-добре на Unicode символи, OpenGL и експортиране към OSX и Linux вместо само към Windows.

## Пример за B3D
B3d файл, който съдържа 1 TEXS парче, 1 BRUS парче и 1 NODE парче, ще изглежда така:

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
Една проста, неанимираща и нетекстурирана мрежа ще изглежда така:

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


## Препратки
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

