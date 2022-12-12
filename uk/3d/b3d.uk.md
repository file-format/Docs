{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу B3D; використовується в іграх blitz3d та API, які можуть відкривати та створювати файли B3D.",
  "title" :"B3D - файл моделі сутності Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Що таке файл B3D?

Файл із розширенням .b3d — це файл моделі, який використовується Blitz3D і може містити моделі відеоігор для персонажів, будівель, рельєфу та інших об’єктів. Blitz3D — це мова програмування, яка використовується для створення **ігор blitz3d**. Blitz3D — це потужна, гнучка та проста у використанні мова програмування, розроблена виключно для написання відеоігор. Розробники можуть створювати насичені екшенами 3D-ігри, 2D-головоломки, пригоди, рольові ігри тощо, просто використовуючи Blitz3D.

Blitz3D заснований на мові програмування BASIC; який також простий у вивченні та використанні. Усі ці факти роблять Blitz ідеальним як для початківців, так і для більш досвідчених програмістів. Хоча його функції вважаються дещо застарілими, ніж у більшості сучасних 3D-движків, Blitz3D продовжує використовуватися багатьма програмістами ігор у всьому світі.

## Коротка історія Blitz3D

Blitz3D був фактично випущений для операційної системи Microsoft Windows у вересні 2001 року, щоб конкурувати з іншими подібними мовами розробки ігор. Blitz3D був оновленою версією попереднього механізму 2D BlitzBasic, який розширив свій набір команд додаванням API для механізму 3D на основі DirectX 7. Користувачі Blitz3D також повинні порівняти BlitzMax, який є більш пізнім двигуном від BlitzBasic. BlitzMax — це складна, але потужніша версія Blitz3D, яка підтримує об’єктно-орієнтовані мови програмування. Це оновлений графічний API, щоб краще відповідати символам Unicode, OpenGL і експорту в OSX і Linux замість лише Windows.

## Приклад B3D
Файл b3d, який містить 1 фрагмент TEXS, 1 фрагмент BRUS і 1 фрагмент NODE, виглядатиме так:

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
Проста сітка без анімації та текстури виглядатиме так:

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


## Список літератури
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

