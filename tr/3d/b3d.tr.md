{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"B3D dosya formatı hakkında bilgi edinin; blitz3d oyunlarında ve B3D dosyalarını açıp oluşturabilen API'lerde kullanılır.",
  "title" :"B3D - Blitz3D Varlık Modeli Dosyası",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## B3D dosyası nedir?

.b3d uzantılı bir dosya, Blitz3D tarafından kullanılan ve karakterler, binalar, arazi ve diğer nesneler için video oyunu modelleri içerebilen bir model dosyasıdır. Blitz3D, **blitz3d oyunları** oluşturmak için kullanılan bir programlama dilidir. Blitz3D, yalnızca video oyunları yazmak amacıyla tasarlanmış güçlü, esnek ve kullanımı kolay bir programlama dilidir. Geliştiriciler, yalnızca Blitz3D'yi kullanarak aksiyon dolu 3B oyunlar, 2B bulmacalar, maceralar, RPG'ler yaratabilirler.

Blitz3D, BASIC programlama dilini temel alır; öğrenmesi ve kullanması da kolaydır. Tüm bu gerçekler, Blitz'i hem yeni başlayanlar hem de daha deneyimli programcılar için ideal hale getiriyor. Özellikleri, çoğu modern 3B motorda bulunanlardan biraz eskimiş olarak görülse de, Blitz3D dünya çapında birçok oyun programcısı tarafından kullanılmaya devam ediyor.

## Blitz3D'nin kısa tarihi

Blitz3D, temel olarak Eylül 2001'de diğer benzer oyun geliştirme dilleriyle rekabet etmek için Microsoft Windows işletim sistemi için piyasaya sürüldü. Blitz3D, DirectX 7 tabanlı bir 3B motor için bir API'nin eklenmesiyle komut setini genişleten önceki 2B motor BlitzBasic'in yükseltilmiş bir versiyonuydu. Blitz3D kullanıcıları, BlitzBasic'in daha sonraki bir motoru olan BlitzMax'i de karşılaştırmalıdır. BlitzMax, nesne yönelimli programlama dillerini destekleyen Blitz3D'nin karmaşık ama daha güçlü bir sürümüdür. Unicode karakterlere, OpenGL'ye daha iyi uyum sağlamak ve yalnızca Windows yerine OSX ve Linux'a dışa aktarmak için güncellenmiş bir grafik API'sidir.

## B3D Örneği
1 TEXS yığın, 1 BRUS yığın ve 1 NODE yığın içeren bir b3d dosyası şöyle görünecektir:

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
Basit, animasyonsuz ve dokusuz bir ağ şöyle görünür:

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


## Referanslar
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

