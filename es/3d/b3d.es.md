{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo B3D; se utiliza en juegos blitz3d y API que pueden abrir y crear archivos B3D",
  "title" :"B3D - Archivo de modelo de entidad Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## ¿Qué es un archivo B3D?

Un archivo con extensión .b3d es un archivo de modelo utilizado por Blitz3D que puede contener modelos de videojuegos para personajes, edificios, terrenos y otros objetos. Blitz3D es un lenguaje de programación utilizado para crear **juegos blitz3d**. Blitz3D es un lenguaje de programación potente, flexible y fácil de usar diseñado con el único propósito de escribir videojuegos. Los desarrolladores pueden crear juegos 3D llenos de acción, rompecabezas 2D, aventuras, juegos de rol, lo que sea con solo usar Blitz3D.

El Blitz3D se basa en el lenguaje de programación BASIC; que también es fácil de aprender y usar. Todos estos hechos hacen que Blitz sea ideal tanto para principiantes como para programadores más experimentados. Aunque sus características se consideran un tanto anticuadas que las que se encuentran en la mayoría de los motores 3D modernos, muchos programadores de juegos en todo el mundo continúan utilizando Blitz3D.

## Breve historia de Blitz3D

Blitz3D se lanzó básicamente para el sistema operativo Microsoft Windows en septiembre de 2001, para competir con otros lenguajes de desarrollo de juegos similares. Blitz3D era una versión mejorada del motor 2D anterior BlitzBasic, que amplió su conjunto de comandos con la adición de una API para un motor 3D basado en DirectX 7. Los usuarios de Blitz3D también deberían comparar BlitzMax, que es un motor posterior de BlitzBasic. BlitzMax es una versión compleja pero más poderosa de Blitz3D, que admite lenguajes de programación orientados a objetos. Es una API de gráficos actualizada para adaptarse mejor a los caracteres Unicode, OpenGL y exportar a OSX y Linux en lugar de solo a Windows.

## Ejemplo B3D
Un archivo b3d que contenga 1 fragmento TEXS, 1 fragmento BRUS y 1 fragmento NODE, se verá así:

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
Una malla simple, sin animación y sin textura se verá así:

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


## Referencias
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BÁSICO](https://en.wikipedia.org/wiki/Blitz_BASIC)

