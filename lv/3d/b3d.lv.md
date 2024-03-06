{
  "date": "2021-04-19",
  "keywords": [
"Blitz3D",
"b3d",
"failu",
"pagarinājumu",
"formātā",
"blitz3d spēles"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par B3D faila formātu; izmanto blitz3d spēlēs un API, kas var atvērt un izveidot B3D failus.",
  "title": "B3D — Blitz3D entītijas modeļa fails",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3-lvd"
}
},
  "lastmod": "2021-04-19"
}

## Kas ir B3D fails?

Fails ar paplašinājumu .b3d ir modeļa fails, ko izmanto Blitz3D un kurā var būt ietverti varoņu, ēku, reljefa un citu objektu videospēļu modeļi. Blitz3D ir programmēšanas valoda, ko izmanto, lai izveidotu **blitz3d spēles**. Blitz3D ir jaudīga, elastīga un viegli lietojama programmēšanas valoda, kas paredzēta tikai videospēļu rakstīšanai. Izmantojot Blitz3D, izstrādātāji var izveidot 3D spēles, 2D atjautības, piedzīvojumus, RPGS un jebko citu.

Blitz3D pamatā ir BASIC programmēšanas valoda; ko arī ir viegli iemācīties un lietot. Visi šie fakti padara Blitz par ideālu gan iesācējiem, gan pieredzējušākiem programmētājiem. Lai gan Blitz3D funkcijas tiek uzskatītas par nedaudz novecojošām nekā lielākajā daļā mūsdienu 3D dzinēju, daudzi spēļu programmētāji joprojām izmanto Blitz3D visā pasaulē.

## Īsa Blitz3D vēsture

Blitz3D pamatā tika izlaists Microsoft Windows operētājsistēmai 2001. gada septembrī, lai konkurētu ar citām līdzīgām spēļu izstrādes valodām. Blitz3D bija jaunināta versija salīdzinājumā ar iepriekšējo 2D dzinēju BlitzBasic, kas paplašināja savu komandu kopu, pievienojot API uz DirectX 7 balstītam 3D dzinējam. Blitz3D lietotājiem vajadzētu arī salīdzināt BlitzMax, kas ir vēlāks BlitzBasic dzinējs. BlitzMax ir sarežģīta, bet jaudīgāka Blitz3D versija, kas atbalsta objektorientētas programmēšanas valodas. Tā ir atjaunināta grafikas API, kas labāk atbilst Unicode rakstzīmēm, OpenGL un eksportēšanai uz OSX un Linux, nevis tikai uz Windows.

## B3D piemērs
B3d fails, kurā ir 1 TEXS gabals, 1 BRUS gabals un 1 NODE gabals, izskatīsies šādi:

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
Vienkāršs, ne-animējošs un bez faktūras siets izskatīsies šādi:

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


## Atsauces
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

