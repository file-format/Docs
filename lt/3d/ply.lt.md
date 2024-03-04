{
  "date": "2019-12-12",
  "keywords": [
"PLY",
"failą",
"pratęsimas",
"formatu",
"3D failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie PLY failo formatą ir API, kurios gali kurti ir atidaryti PLY failus.",
  "title": "PLY – daugiakampis 3D failo formatas",
  "linktitle": "PLY",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-pl-lty"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PLY failas?

PLY, daugiakampio failo formatas, reiškia 3D failo formatą, kuriame saugomi grafiniai objektai, apibūdinami kaip daugiakampių rinkinys. Šio failo formato tikslas buvo sukurti paprastą ir paprastą failo tipą, kuris būtų pakankamai bendras, kad būtų naudingas įvairiems modeliams. PLY failo formatas yra ASCII ir dvejetainis formatas kompaktiškam saugojimui ir greitam išsaugojimui bei įkėlimui. Failo formatą naudoja įvairios programos, kurios palaiko 3D failų skaitymą.

PLY formato objektai aprašomi viršūnių, veidų ir kitų elementų rinkiniu, taip pat ypatybėmis, tokiomis kaip spalva ir įprasta kryptis, kurias galima pridėti prie šių elementų. Kitos ypatybės, kurios taip pat gali būti saugomos su objektu, yra šios:

* Paviršiaus normalios

* tekstūros koordinatės

* skaidrumas

* diapazono duomenų patikimumas

* daugiakampio priekio ir galo savybės


PLY formatu vaizduojamas objektas gali būti įvairių šaltinių, tokių kaip ranka suskaitmeninti objektai, daugiakampiai objektai iš modeliavimo programų, diapazono duomenys, trikampiai iš žygiuojančių kubų, reljefo duomenys ir spinduliavimo modeliai, rezultatas.

## Trumpa istorija

PLY formatą 1990-aisiais sukūrė Gregas Turkas ir kiti Stanfordo grafikos laboratorijoje, todėl jis taip pat žinomas kaip Stanfordo trikampio formatas. Nuo tada failo formatas turi 1.0 versiją ir nebuvo atlikta jokių papildomų pakeitimų.

## PLY failo formatas

Paprastas PLY objektas susideda iš elementų rinkinio, skirto objekto vaizdavimui. Jį sudaro (x,y,z) viršūnių trigubų sąrašas ir veidų, kurie iš tikrųjų yra viršūnių sąrašo indeksai, sąrašas. Viršūnės ir veidai yra du elementų pavyzdžiai, o didžiąją dalį PLY failo sudaro šie du elementai. Taip pat galima sukurti naujas savybes ir pridėti prie objekto elementų, tačiau jas reikia pridėti taip, kad senos programos nesugestų susidūrus su šiomis naujomis savybėmis. Tokių savybių galima atsisakyti ir skaitant programas. Be to, naudojant šį elementą galima sukurti naujus elementus ir apibrėžti savybes.

### Failo struktūra

PLY failo formato failo struktūra yra tokia:

|Laukas
---|
|Failo antraštė
|Vertex sąrašas
|Veidų sąrašas
|Kitų elementų sąrašas

#### Struktūros pavyzdys

Toliau pateiktą pavyzdį naudosime tolesnėje diskusijoje įvairioms PLY failo formato dalims.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Failo antraštė

PLY failo formato antraštė susideda iš ASCII teksto tiek ASCII, tiek dvejetainiam formatui. Antraštės skilties pradžia ir pabaiga identifikuojama pagal sluoksnio ir pabaigos antraštės raktinius žodžius. Antraštės pradžioje yra stebuklingas žodis ply, kuris naudojamas skaitytojams atpažinti PLY failo formatą. Kitoje eilutėje rodomas šio failo versijos numeris. PLY failo formato komentarai prasideda komentaro raktiniu žodžiu kiekvienos komentaro eilutės pradžioje.

#### Elemento raktinis žodis

Tada elemento raktinis žodis nurodo, kas yra failo viduje. Po jos pateikiamos to konkretaus elemento tipo savybės, kur kiekviena ypatybė turi savo savybių tipą ir tvarką, kaip parodyta toliau:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Šiame konkrečiame pavyzdyje konkretus viršūnės elementas turi 3 plaukiojančio tipo savybes su nurodyta tvarka.

#### Duomenų tipų tipai

Nuosavybė gali turėti dviejų tipų duomenų tipus.

Skaliarinis: skaliarinių duomenų tipai yra tokie, kaip parodyta toliau:

|#Vardas|#Tipas|#Baitų skaičius
|charakteris|simbolis|1
|uchar|nesignalas|1
|trumpas|trumpas sveikasis skaičius|2
|ushort|nepasirašytas trumpasis sveikasis skaičius|2
|int|Sveikasis skaičius|4
|uint|nepasirašytas sveikasis skaičius|4
|plūdė|vienkartinė plūdė|4
|dviguba|dvigubos tikslumo plūdė|8

Sąrašas: yra speciali ypatybių apibrėžimų forma, kuri naudoja sąrašo duomenų tipą. To pavyzdys yra iš aukščiau esančio kubo failo:

ypatybių sąrašas uchar int vertex_index.

Tai reiškia, kad ypatybėje vertex_index pirmiausia yra nepasirašytas simbolis, nurodantis, kiek ypatybėje yra indeksų, o po to pateikiamas sąrašas, kuriame yra tiek sveikųjų skaičių. Kiekvienas sveikas skaičius šiame kintamo ilgio sąraše yra viršūnės indeksas.

## Nuorodos Nr.

* [PLY failo formatas](http://paulbourke.net/dataformats/ply/)

* [PLY – Vikipedija](https://en.wikipedia.org/wiki/PLY_(file_format))


