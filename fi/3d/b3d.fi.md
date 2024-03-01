{
  "date": "2021-04-19",
  "keywords": [
"Blitz3D",
"b3d",
"tiedosto",
"laajennus",
"muoto",
"blitz3d pelejä"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi B3D-tiedostomuodosta; käytetään blitz3d-peleissä ja API:issa, jotka voivat avata ja luoda B3D-tiedostoja.",
  "title": "B3D - Blitz3D-entiteettimallitiedosto",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3-fid"
}
},
  "lastmod": "2021-04-19"
}

## Mikä on B3D-tiedosto?

Tiedosto, jonka pääte on .b3d, on Blitz3D:n käyttämä mallitiedosto, joka voi sisältää videopelimalleja hahmoille, rakennuksille, maastolle ja muille kohteille. Blitz3D on ohjelmointikieli, jota käytetään **blitz3d-pelien** luomiseen. Blitz3D on tehokas, joustava ja helppokäyttöinen ohjelmointikieli, joka on suunniteltu yksinomaan videopelien kirjoittamiseen. Blitz3D:n avulla kehittäjät voivat luoda toiminnantäyteisiä 3D-pelejä, 2D-pulmapelejä, seikkailuja, RPGS-pelejä, mitä tahansa.

Blitz3D perustuu BASIC-ohjelmointikieleen; joka on myös helppo oppia ja käyttää. Kaikki nämä tosiasiat tekevät Blitzistä ihanteellisen aloittelijoille ja kokeneemmille ohjelmoijille. Vaikka Blitz3D:n ominaisuuksia pidetään hieman vanhentuneempina kuin useimmissa nykyaikaisissa 3D-moottoreissa, monet peliohjelmoijat käyttävät Blitz3D:tä edelleen maailmanlaajuisesti.

## Blitz3D:n lyhyt historia

Blitz3D julkaistiin pohjimmiltaan Microsoft Windows -käyttöjärjestelmälle syyskuussa 2001 kilpailemaan muiden vastaavien pelinkehityskielten kanssa. Blitz3D oli päivitetty versio aikaisemmasta 2D-moottorista BlitzBasic, joka laajensi komentosarjaansa lisäämällä API:n DirectX 7 -pohjaiselle 3D-moottorille. Blitz3D-käyttäjien tulisi myös verrata BlitzMaxia, joka on BlitzBasicin myöhempi moottori. BlitzMax on monimutkainen mutta tehokkaampi versio Blitz3D:stä, joka tukee olio-ohjelmointikieliä. Se on päivitetty grafiikkasovellusliittymä, joka sopii paremmin Unicode-merkkeihin, OpenGL:ään ja vientiin OSX:ään ja Linuxiin pelkän Windowsin sijaan.

## B3D esimerkki
B3d-tiedosto, joka sisältää 1 TEXS-kappaleen, 1 BRUS-kappaleen ja 1 NODE-kappaleen, näyttää tältä:

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
Yksinkertainen, ei-animoiva ja teksturoitumaton verkko näyttää tältä:

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


## Viitteet
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

