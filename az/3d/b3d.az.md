{
  "date": "2021-04-19",
  "keywords": [
"Blitz3D",
"b3d",
"fayl",
"uzadılması",
"format",
"Blitz 3d oyunlar"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "B3D fayl formatı haqqında məlumat əldə edin; blitz3d oyunlarında və B3D fayllarını aça və yarada bilən API-lərdə istifadə olunur.",
  "title": "B3D - Blitz3D Müəssisə Model Faylı",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3-azd"
}
},
  "lastmod": "2021-04-19"
}

## B3D faylı nədir?

.b3d uzantısı olan fayl Blitz3D tərəfindən istifadə olunan model fayldır və burada personajlar, binalar, ərazi və digər obyektlər üçün video oyun modelləri ola bilər. Blitz3D **blitz3d oyunları** yaratmaq üçün istifadə edilən proqramlaşdırma dilidir. Blitz3D güclü, çevik və istifadəsi asan proqramlaşdırma dilidir, yalnız video oyunları yazmaq üçün nəzərdə tutulmuşdur. Tərtibatçılar sadəcə Blitz3D-dən istifadə etməklə hərəkətli 3D oyunlar, 2D tapmacalar, sərgüzəştlər, RPGS yarada bilərlər.

Blitz3D BASIC proqramlaşdırma dilinə əsaslanır; öyrənmək və istifadə etmək də asandır. Bütün bu faktlar Blitz-i həm yeni başlayanlar, həm də daha təcrübəli proqramçılar üçün ideal edir. Xüsusiyyətləri əksər müasir 3D mühərriklərdə olandan bir qədər köhnəlmiş hesab edilsə də, Blitz3D bütün dünyada bir çox oyun proqramçıları tərəfindən istifadə olunmağa davam edir.

## Blitz3D-nin qısa tarixi

Blitz3D digər oxşar oyun inkişaf etdirmə dilləri ilə rəqabət aparmaq üçün 2001-ci ilin sentyabrında Microsoft Windows əməliyyat sistemi üçün buraxıldı. Blitz3D əvvəlki 2D mühərriki BlitzBasic ilə müqayisədə təkmilləşdirilmiş versiya idi, o, DirectX 7 əsaslı 3D mühərriki üçün API əlavə etməklə komanda dəstini genişləndirdi. Blitz3D istifadəçiləri BlitzBasic-in sonrakı mühərriki olan BlitzMax-ı da müqayisə etməlidirlər. BlitzMax obyekt yönümlü proqramlaşdırma dillərini dəstəkləyən Blitz3D-nin mürəkkəb, lakin daha güclü versiyasıdır. Bu, Unicode simvollarına, OpenGL-ə daha yaxşı uyğunlaşmaq və yalnız Windows əvəzinə OSX və Linux-a ixrac etmək üçün yenilənmiş qrafik API-dir.

## B3D nümunəsi
1 TEXS yığını, 1 BRUS yığını və 1 NODE yığını olan b3d faylı belə görünəcək:

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
Sadə, canlandırıcı olmayan və teksturasız mesh belə görünəcək:

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


## İstinadlar
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

