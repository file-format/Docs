{
  "date": "2021-04-19",
  "keywords": [
"Cluiche Blitz 3D",
"b3d",
"comhad",
"síneadh",
"formáid",
"Cluichí blitz3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid B3D; a úsáidtear i gcluichí blitz3d agus APIs is féidir comhaid B3D a oscailt agus a chruthú.",
  "title": "B3D - Comhad Samhail Aonáin Blitz3D",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3-gad"
}
},
  "lastmod": "2021-04-19"
}

## Cad is comhad B3D ann?

Comhad samhail le síneadh .b3d is ea comhad a úsáideann Blitz3D a bhféadfadh samhlacha físchluiche do charachtair, foirgnimh, tír-raon agus réada eile a bheith ann. Is teanga ríomhchláraithe é an Blitz3D a úsáidtear chun **cluichí blitz3d** a chruthú. Teanga ríomhchlárúcháin chumhachtach, sholúbtha agus éasca le húsáid is ea Blitz3D atá deartha chun físchluichí amháin a scríobh. Is féidir leis na forbróirí a chruthú aicsean-pacáilte cluichí 3D, puzzlers 2D, eachtraí, RPGS, is cuma cad díreach ag baint úsáide as Blitz3D.

Tá an Blitz3D bunaithe ar an teanga ríomhchlárúcháin BASIC; atá éasca le foghlaim agus le húsáid freisin. Tá na fíricí seo go léir ag déanamh Blitz oiriúnach do thosaitheoirí agus do ríomhchláraitheoirí a bhfuil níos mó taithí acu araon. Cé go meastar go bhfuil na gnéithe seo beagán seanda ná mar a fhaightear i bhformhór na n-innill 3D nua-aimseartha, leanann go leor ríomhchláraitheoirí cluiche ar fud an domhain le Blitz3D a úsáid.

## Stair achomair blitz 3d saor in aisce,

Eisíodh an Blitz3D go bunúsach do chóras oibriúcháin Microsoft Windows i Meán Fómhair 2001, chun dul san iomaíocht le teangacha forbartha cluiche eile dá samhail. Leagan uasghrádaithe a bhí i Blitz3D thar an inneall 2D níos luaithe BlitzBasic, a leathnaigh a shraith orduithe le API le haghaidh inneall 3D bunaithe ar DirectX 7-bhunaithe. Ba cheart d’úsáideoirí Blitz3D comparáid a dhéanamh freisin le BlitzMax, inneall níos déanaí ag BlitzBasic. Is leagan casta ach níos cumhachtaí de Blitz3D é an BlitzMax, a thacaíonn le teangacha ríomhchláraithe atá dírithe ar oibiachtaí. Is API grafaic nuashonraithe é a oireann níos fearr do charachtair Unicode, OpenGL, agus onnmhairiú chuig OSX agus Linux seachas Windows amháin.

## Sampla B3D
Beidh cuma mar seo ar chomhad b3d ina bhfuil 1 smután TEXS, 1 smután BRUS agus 1 smután NODE:

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
Breathnóidh mogall simplí, neamhbheochanach agus neamh-uigeachta mar seo:

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


## Tagairtí
 * [B3D](https://moddb.fandom.com/wiki/B3D )
 * [Blitz BASIC](https://ga.wikipedia.org/wiki/Blitz_BASIC)

