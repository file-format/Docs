{
  "date": "2019-10-11",
  "keywords": [
"gbr failą",
"gbr failo formatas",
"kas yra gbr failas",
"failą",
"gbr pavyzdys",
"gbr failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GBR failo formatas - Gerber failo formatas PCB",
  "description": "Sužinokite apie GBR failo formatą ir API, kurios gali kurti ir atidaryti GBR failus.",
  "linktitle": "GBR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gb-ltr"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra GBR failas?

Failas su plėtiniu .gbr yra Gerber vaizdo failo formatas, skirtas keistis spausdintinės plokštės (PCB) dizaino duomenims perduoti. Jį sukūrė Ucamco. PCB projektavimo duomenys yra pagrindinis komponentas, kurio reikia gamybos pramonei. GRB faile yra PCB duomenų, tokių kaip vario sluoksniai, litavimo kaukė, legenda ir gręžimo bei maršruto duomenys. Jis gali būti naudojamas duomenims, pvz., PCB gamybos charakteristikoms, įskaitant storį ar apdailą, perduoti standartizuotu formatu. Visos PCB projektavimo sistemos išveda Gerber failus, kuriuos gali tvarkyti PCB gamybos sistemos. GBR failai dabar tapo de facto spausdintinės plokštės (PCB) dizaino duomenų perdavimo standartu. Ucamco pateikė [free online viewer](https://gerber-viewer.ucamco.com/), skirtą GBR failų formatams atidaryti ir peržiūrėti.

## GBR failo formatas

GBR yra UTF-8 žmogaus skaitomas formatas, kurį sudaro tik 27 komandos. Dėl šio trumpo komandų sąrašo ir kompaktiškumo GBR lengva derinti. Gerber esmė yra atviras vektorinis formatas 2D dvejetainiams vaizdams. Meta informacija perduodama kartu su vaizdais per atributus. Viename GRB faile nurodomas vienas vaizdas ir nereikia aiškinti jokių lydinčių failų ar išorinių parametrų. Vienam vaizdui reikia tik vieno failo. Jis naudoja 7 bitų ASCII simbolius visoms specifikacijoje apibrėžtoms komandoms ir pavadinimams, kuriuos galima spausdinti. Tai visiškai apima visą vaizdo generavimą.

### GBR failo pavyzdys

Toliau pateikiamas Gerber failo pavyzdys, sukuriantis 1,5 mm skersmens apskritimą, kurio centras yra nuo pradžios taško. Kiekvienoje eilutėje yra viena komanda.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Nuorodos

 * [Gerber formatas](https://www.ucamco.com/en/gerber)

