{
  "date": "2021-08-09",
  "keywords": [
"cso failą",
"cso failo formatas",
"kas yra cso failas",
"failą",
"cso pavyzdys",
"cso failo plėtinys",
"pratęsimas",
"formatu",
"iso",
"DAX suspaudimas"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie CSO failų formatą ir API, kurios gali kurti ir atidaryti CSO failus.",
  "title": "CSO – suspaustas ISO disko vaizdas",
  "linktitle": "CSO",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cs-lto"
}
},
  "lastmod": "2021-08-09"
}

## Kas yra CSO failas?

Failas su plėtiniu .cso yra suglaudintas ISO vaizdo failas. CSO yra alternatyva DAX glaudinimo metodui; taip pat žinomas kaip CISO; buvo pirmasis būdas suspausti [ISO](/compression/iso/) failus ir dažniausiai yra pageidaujamas PlayStation Portable daiktų archyvavimo būdas. Šiame formate naudojamas glaudinimas, kuris gali apimti iki devynių glaudinimo sluoksnių. Vaizdams kurti naudojama tokia programinė įranga kaip Prometheus ir YACC.

## CSO failo formatas

CSO failo formatas buvo pirmasis ISO suspaudimo metodas, skirtas sutaupyti daugiau vietos atmintyje. Kartkartėmis buvo daromi patobulinimai, siekiant geresnio suspaudimo. CSO naudoja Deflate glaudinimą, turėdamas devynis išankstinių nustatymų lygius, paprastai kiekvienas lygis gali apdoroti 2 KiB blokus atskirai. Nors aukščiausias glaudinimo lygis gali sulėtinti ir pailginti programinės įrangos įkėlimo laiką, kuris labai priklauso nuo disko srautinio perdavimo, taip pat žemesni lygiai gali atlikti didelį suspaudimą.

### CSO failo struktūra

CSO failo formatą sudaro 24 baitų antraštė, duomenų blokai ir rodyklės lentelė. Manoma, kad laukuose, didesniuose nei baitas, Little-endian. PlayStation Portable architektūros baigtis pateikta žemiau.

#### Antraštė

| Poslinkis (baitai) | Vardas | Dydis (baitais) | Paskirtis |
----------|----------|--------------|---------|
| 0x0 | Magija | 4 | Visada CISO arba 0x4F534943, kai skaitomas kaip 32 bitų sveikasis skaičius. Šis laukas naudojamas CSO failui identifikuoti. Atkreipkite dėmesį, kad šis laukas gali skirtis kitiems CSO dariniams, pavyzdžiui, ZSO naudojo stebuklingą kodą ZISO. |
| 0x4 | Antraštės dydis | 4 | Pradinio CSO v1 failo formato atveju šis laukas nepaisomas, todėl nereikia, kad jis būtų tikslus. Tačiau v2 ir ZSO formatai reikalauja, kad šis laukas visada būtų 0x18 (24 baitai). |
| 0x8 | Nesuspaustas dydis | 8 | Originalo nesuspausto ISO dydis baitais. |
| 0x10 | Bloko dydis | 4 | Kiekvieno duomenų bloko dydis baitais prieš suspaudimą. Paprastai 2048 baitai, tiek pat, kiek kiekvieno ISO 9660 sektoriaus dydis. |
| 0x14 | Version | 1 | The version of the file format in use. For the "v1" format, the value can be either 0 or 1. v2 formatui tai turi būti 2. Be to, ZSO formatui tai turi būti 1. |
| 0x15 | Rodyklės lygiavimas | 1 | Kiekvieno indekso įrašo lygiavimas, nurodytas bitais. |
| 0x16 | Rezervuota | 2 | Šis laukas nenaudojamas. V1 formatu šis laukas nepaisomas ir jame gali būti savavališkų reikšmių. v2 formatu šis laukas turi būti lygus nuliui. |

#### Rodyklės lentelė

Indekso lentelėje yra keli 4 baitų įrašai, nurodantys kiekvieno duomenų bloko vietą, ir papildomas paskutinis įrašas, nukreipiantis į failo pabaigą.
Kiekvieno įrašo turinys yra toks:
| Bit | Ilgis | Kaukė | Vardas | Paskirtis |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Padėtis | Šis laukas, perkeltas į kairę pagal antraštėje pateiktą rodyklės išlygiavimą, suteikia vietą, kurioje prasideda duomenų blokas. |
| 31 | 1 | 0x80000000 | Suspaudimo tipas | ZSO formatas turi panašią semantiką, tik 0 reiškia LZ4, o ne Deflate. v2 formatu. Blokas netiesiogiai laikomas nesuspaustu, jei bloko dydis yra lygus arba didesnis už bloko dydį, nurodytą failo antraštėje. |

#### Duomenų blokai

Duomenų blokus sudaro nesuspausti arba suspausti duomenys. Bloko dydis apskaičiuojamas gavus jo vietą ir atimant jį iš kito bloko padėties. Jei indekso lygiavimas yra didesnis nei nulis, tikėtina, kad bloko dydis yra didesnis nei jame saugomi duomenys.


## Nuorodos 

* N/A


