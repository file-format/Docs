{
  "date": "2021-04-19",
  "keywords": [
"Blitz3D",
"b3d",
"failą",
"pratęsimas",
"formatu",
"blitz3d žaidimai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie B3D failo formatą; naudojamas blitz3d žaidimuose ir API, kurios gali atidaryti ir kurti B3D failus.",
  "title": "B3D – Blitz3D objekto modelio failas",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3-ltd"
}
},
  "lastmod": "2021-04-19"
}

## Kas yra B3D failas?

Failas su plėtiniu .b3d yra Blitz3D naudojamas modelio failas, kuriame gali būti vaizdo žaidimų modelių, skirtų personažams, pastatams, reljefui ir kitiems objektams. Blitz3D yra programavimo kalba, naudojama kuriant **blitz3d žaidimus**. Blitz3D yra galinga, lanksti ir lengvai naudojama programavimo kalba, skirta vieninteliam tikslui rašyti vaizdo žaidimus. Kūrėjai gali sukurti veiksmo kupinus 3D žaidimus, 2D galvosūkius, nuotykius, RPGS ir bet ką, naudodami Blitz3D.

Blitz3D yra pagrįstas BASIC programavimo kalba; kurią taip pat lengva išmokti ir naudoti. Dėl visų šių faktų Blitz idealiai tinka pradedantiesiems ir labiau patyrusiems programuotojams. Nors Blitz3D funkcijos laikomos šiek tiek pasenusiomis nei daugumoje šiuolaikinių 3D variklių, daugelis žaidimų programuotojų visame pasaulyje naudoja Blitz3D.

## Trumpa Blitz3D istorija

Blitz3D iš esmės buvo išleistas Microsoft Windows operacinei sistemai 2001 m. rugsėjo mėn., siekiant konkuruoti su kitomis panašiomis žaidimų kūrimo kalbomis. Blitz3D buvo atnaujinta versija, palyginti su ankstesniu 2D varikliu BlitzBasic, kuris išplėtė savo komandų rinkinį pridedant DirectX 7 pagrindu veikiančio 3D variklio API. Blitz3D vartotojai taip pat turėtų palyginti BlitzMax, kuris yra vėlesnis BlitzBasic variklis. BlitzMax yra sudėtinga, bet galingesnė Blitz3D versija, kuri palaiko į objektą orientuotas programavimo kalbas. Tai atnaujinta grafinė API, kad geriau tiktų Unicode simboliams, OpenGL ir eksportui į OSX bei Linux, o ne tik į Windows.

## B3D pavyzdys
B3d failas, kuriame yra 1 TEXS dalis, 1 BRUS dalis ir 1 NODE dalis, atrodys taip:

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
Paprastas, neanimuojantis ir be tekstūros tinklelis atrodys taip:

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


## Nuorodos
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

