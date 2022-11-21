{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file B3D; digunakan dalam game blitz3d dan API yang dapat membuka dan membuat file B3D.",
  "title" :"B3D - File Model Entitas Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Apa itu file B3D?

File dengan ekstensi .b3d adalah file model yang digunakan oleh Blitz3D yang mungkin berisi model video game untuk karakter, bangunan, medan, dan objek lainnya. Blitz3D adalah bahasa pemrograman yang digunakan untuk membuat **game blitz3d**. Blitz3D adalah bahasa pemrograman yang kuat, fleksibel, dan mudah digunakan yang dirancang hanya untuk tujuan menulis video game. Pengembang dapat membuat game 3D penuh aksi, teka-teki 2D, petualangan, RPG, apa pun hanya dengan menggunakan Blitz3D.

Blitz3D didasarkan pada bahasa pemrograman BASIC; yang juga mudah dipelajari dan digunakan. Semua fakta ini menjadikan Blitz ideal untuk pemula dan pemrogram yang lebih berpengalaman. Meskipun fiturnya dianggap agak kuno daripada yang ditemukan di sebagian besar mesin 3D modern, Blitz3D terus digunakan oleh banyak pemrogram game di seluruh dunia.

## Sejarah singkat Blitz3D

Blitz3D pada dasarnya dirilis untuk sistem operasi Microsoft Windows pada September 2001, untuk bersaing dengan bahasa pengembangan game serupa lainnya. Blitz3D adalah versi yang ditingkatkan dari mesin 2D BlitzBasic sebelumnya, yang memperluas kumpulan perintahnya dengan penambahan API untuk mesin 3D berbasis DirectX 7. Pengguna Blitz3D juga harus membandingkan BlitzMax, yang merupakan mesin terbaru dari BlitzBasic. BlitzMax adalah versi Blitz3D yang kompleks namun lebih bertenaga, yang mendukung bahasa pemrograman berorientasi objek. Ini adalah API grafik yang diperbarui agar lebih sesuai dengan karakter Unicode, OpenGL, dan mengekspor ke OSX dan Linux, bukan hanya Windows.

## Contoh B3D
File b3d yang berisi 1 potongan TEXS, 1 potongan BRUS dan 1 potongan NODE, akan terlihat seperti ini:

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
Jaring sederhana, non-animasi, dan non-tekstur akan terlihat seperti ini:

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


## Referensi
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

