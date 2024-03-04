{
  "date": "2019-10-11",
  "keywords": [
"tga failą",
"tga failo formatas",
"kas yra tga failas",
"failą",
"tga pavyzdys",
"tga failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGA failo formatas – TARGA grafinio vaizdo failas",
  "description": "Sužinokite apie TGA failo formatą ir API, kurios gali kurti ir atidaryti TGA failus.",
  "linktitle": "TGA",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-tg-lta"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra TGA failas?

Failas su plėtiniu .tga yra rastrinės grafikos formatas, kurį sukūrė Truevision Inc. Jis buvo sukurtas TARGA (Truevision Advanced Raster Adapter) plokštėms ir suteikė Highcolor / truecolor ekrano palaikymą su IBM suderinamiems kompiuteriams. Jis palaiko 8, 16, 24 ir 32 bitų viename taške ir 8 bitų alfa kanalą. Jis taip pat palaiko be nuostolių RLE glaudinimą, kuris gali būti taikomas norint sumažinti vaizdo dydį. Skaitmeninėse nuotraukose ir tekstūrose naudojamas TGA vaizdo formatas.

## Trumpa istorija

TGA failo formatą suformavo 1984 m. AT&T EPICenter (vėliau ištrauktas ir suformuotas kaip nepriklausomas subjektas, žinomas kaip Truevision), kuris dirbo reklamuodamas naujas AT&T sukurtas technologijas, skirtas spalvų rėmelių buferiams. EPICenter jau kūrė pirmąsias dvi korteles – VDA (vaizdo ekrano adapterį) ir ICB (vaizdo fiksavimo plokštę), kurių darbas su dviejų tipų failais – .vda ir .icb – jau buvo vykdomas. Šie failų formatai buvo kodifikuoti ir buvo pristatytas ne toks platus specifinis failų formatas TGA. TGA buvo to, kas jau buvo naudojama, plėtinys ir suteikė tokią informaciją kaip plotis, aukštis, pikselių gylis, susijęs spalvų žemėlapis ir vaizdo kilmė.

TGA 2.0 versija, paskelbta 1989 m., apima keletą patobulintų funkcijų, tokių kaip:

 * Miniatiūros
 * Alfa kanalas
 * Gama vertė
 * Tekstiniai metaduomenys

Pagrindiniai TGA 2.0 versijos kūrėjai yra Shawn Steiner, Kevin Fiedly ir David Spoelstra iš Truevision.

## TGA TARGA failo formato specifikacijos

TGA failą sudaro 2 pagrindinės dalys:

 * Antraštė
 * Spalvų pikselių informacija

Visos TGA failo reikšmės pateikiamos mažomis kalbomis, kaip nurodyta formato specifikacijose.

### TGA antraštė

TGA failo antraštę sudaro šie 5 laukai.

|Lauko nr.|Ilgis |Lauko pavadinimas |Aprašymas|
---|---|---|---|
|1| 1 baitas |ID ilgis| Vaizdo ID lauko ilgis (0-255)|
|2| 1 baitas |Spalvoto žemėlapio tipas| Ar įtrauktas spalvų žemėlapis (0 – rodo, kad šiame paveikslėlyje nėra spalvų žemėlapio duomenų. 1 – rodo, kad su šiuo vaizdu yra spalvų žemėlapis.)|
|3| 1 baitas |Vaizdo tipas| Suspaudimas ir spalvų tipai (0 – neįtraukti vaizdo duomenų. 1 – nesuspaustas, spalvotas vaizdas, 2 – nesuspaustas, tikrosios spalvos vaizdas, 9 – užkoduotas pagal ilgį, spalvotas vaizdas, 11 – užkoduotas pagal ilgį, juodai baltas vaizdas )|
|4| 5 baitai |Spalvų žemėlapio specifikacija| Apibūdina spalvų žemėlapį|
|5| 10 baitų |Vaizdo specifikacija| Vaizdo matmenys ir formatas|

### Vaizdo ir spalvų žemėlapio duomenys

|Lauko Nr. |Ilgis |Laukas |Aprašymas|
---|---|---|---|
|6 |Iš vaizdo ID ilgio lauko| Vaizdo ID| Neprivalomas laukas su identifikavimo informacija|
|7 |Iš spalvų žemėlapio specifikacijos lauko| Spalvoti žemėlapio duomenys| Paieškos lentelė su spalvoto žemėlapio duomenimis|
|8 |Iš vaizdo specifikacijos lauko| Vaizdo duomenys| Saugoma pagal vaizdo aprašą|

### Kūrėjo sritis (pasirenkama)

TGA 2.0 versija palaiko papildomus patobulinimus / priedus, kuriuos daugelis kūrėjų norėjo saugoti daugiau informacijos. Informacija yra neprivaloma, todėl jei TGA dekoderis negali jos interpretuoti, ji bus ignoruojama.

### Išplėtimo sritis (pasirenkama)

|Lauko Nr.| Ilgis| Laukas |Aprašymas|
---|---|---|---|
|10| 2 baitai |Plėtinio dydis |Plėtinio srities dydis baitais, visada 495|
|11| 41 baitas| Autoriaus vardas | Autoriaus vardas. Jei nenaudojate, baitai turi būti nustatyti į NULL (\0) arba tarpai|
|12| 324 baitai| Autoriaus komentaras| Komentaras, suskirstytas į keturias eilutes, kurių kiekvieną sudaro 80 simbolių ir NULL|
|13| 12 baitų| Datos / laiko žyma |Vaizdo sukūrimo data ir laikas|
|14| 41 baitas| Darbo ID||
|15| 6 baitai| Darbo laikas| Valandos, minutės ir sekundės, praleistos kuriant failą (atsiskaitymui ir pan.)|
|16| 41 baitas| Programinės įrangos ID |Programa, kuri sukūrė failą.|
|17| 3 baitai| Programinės įrangos versija ||
|18| 4 baitai| Rakto spalva||
|19| 4 baitai| Pikselių formato santykis||
|20| 4 baitai| Gama vertė||
|21| 4 baitai| Spalvų korekcijos poslinkis |Baitų skaičius nuo failo pradžios iki spalvų korekcijos lentelės, jei yra|
|22| 4 baitai| Pašto ženklas | Baitų skaičius nuo failo pradžios iki pašto ženklo vaizdo, jei yra|
|23| 4 baitai| Nuskaitymo linijos poslinkis| Baitų skaičius nuo failo pradžios iki nuskaitymo eilučių lentelės, jei yra|
|24| 1 baitas| Atributų tipas| Nurodo alfa kanalą|

### Failo poraštė (pasirenkama)

Paskutiniai 26 failo baitai reiškia poraštę, kuri, jei yra, greičiausiai yra 2 versijos TGA failas.

|Lauko Nr.| Ilgis| Laukas| Aprašymas|
---|---|---|---|
|28| 4 baitai| Pratęsimo poslinkis| Poslinkis baitais nuo failo pradžios|
|29| 4 baitai| Kūrėjo srities poslinkis| Poslinkis baitais nuo failo pradžios|
|30| 16 baitų| Parašas| Sudėtyje yra TRUEVISION-XFILE|
|31| 1 baitas| | Sudėtyje yra .|
|32| 1 baitas| | Sudėtyje yra NULL|


## Nuorodos

 * [TGA 2.0 File Format Specifications](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
 * [TGA, Vikipedija](https://en.wikipedia.org/wiki/Truevision_TGA)

