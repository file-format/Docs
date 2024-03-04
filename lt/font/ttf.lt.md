{
  "date": "2020-08-20",
  "keywords": [
"ttf failą",
"ttf failo formatas",
"kas yra ttf failas",
"failą",
"ttf pavyzdys",
"ttf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TTF – „TrueType“ šrifto failo formatas",
  "description": "TrueType šriftai (TTF) yra pagrįsti skaitmeninių šriftų technologijos specifikacijomis, kurias iš pradžių sukūrė Apple, Inc. Tiek Apple, tiek Microsoft naudojo TTF Mac ir Windows operacinėse sistemose.",
  "linktitle": "TTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-ltf"
}
},
  "lastmod": "2020-09-21"
}

## Kas yra TTF failas?

Failas su plėtiniu .ttf reiškia šriftų failus, pagrįstus TrueType specifikacijų šriftų technologija. Iš pradžių ją sukūrė ir paleido Apple Computer, Inc, skirtą Mac OS, o vėliau Microsoft priėmė Windows OS. TrueType šriftai užtikrina aukščiausios kokybės vaizdą kompiuterių ekranuose ir spausdintuvuose, nepriklausydami nuo skiriamosios gebos. Visos šiuolaikinės programos, naudojančios šriftus, gali dirbti su TTF failais. TTF šriftų failai yra laisvai prieinami internete ir gali būti konvertuojami į kitus šriftų failų formatus, tokius kaip OTF ir WOFF.

## Trumpa istorija

Designed by Apply Computer, Inc in 1980s for MacOS, the TTF font format was aimed at resolving some technical limitations by Adobe's Type 1 format. Apple included support for TrueType fonts in Mac in 1991. TTF šriftų dizaino tikslas buvo saugojimo ir apdorojimo efektyvumas bei išplečiamumas. Remiantis šiuo išplėtimu, esamus šriftus galima konvertuoti į TrueType formatą.

Microsoft pirmą kartą TrueType šriftus panaudojo Windows 3.1 1992 m. balandžio mėn., kai Apple sutiko Microsoft licencijuoti TrueType. Tai pagerino rastrizacijos mechanizmą, pagerino jo efektyvumą ir našumą.

## Tikrojo tipo failo formato specifikacijos

TrueType šrifto failas yra dvejetainis failas, kurį sudaro sujungtų lentelių seka. Kiekviena lentelė yra žodžių seka ir turi pavadinimą, žinomą kaip Žyma. Kiekviena žyma yra uint32 duomenų tipo ir susideda iš keturių simbolių. Pirmoji failo lentelė yra šriftų katalogas, suteikiantis prieigą prie kitų šrifto failo lentelių. Šrifto duomenys pateikiami kitose lentelėse po šriftų katalogų lentelės. Kadangi kiekviena lentelė pasiekiama pagal jos žymą, lentelės faile gali būti rodomos bet kokia tvarka.

Reikalingos lentelės ir jų žymų pavadinimai pateikti šioje lentelėje.

|**Žyma**|**Lentelė**|
---|---|
|'cmap'| simbolio ir glifo atvaizdavimas|
|'glyf'| glifo duomenys|
|'galva'| šrifto antraštė|
|'hhea'| horizontali antraštė|
|'hmtx'| horizontalioji metrika|
|'loca'| rodyklė į vietą|
|'maxp'| maksimalus profilis|
|'vardas'| įvardijimas|
|'post'| PostScript|

### Duomenų tipai
TrueType šriftai naudoja standartinį sveikąjį skaičių ir papildomus duomenų tipus, kaip nurodyta šioje lentelėje.

|**Duomenų tipas** | **Aprašymas** |
---|---|
|shortFrac| 16 bitų trupmena su ženklu|
|Pataisytas| 16,16 bitų pasirašytas fiksuoto taško numeris|
|FWord| 16 bitų sveikasis skaičius, apibūdinantis kiekį FU vienetais, mažiausią išmatuojamą atstumą em erdvėje.|
|uFWord| 16 bitų beženklis sveikasis skaičius, apibūdinantis dydį FU vienetais, mažiausią išmatuojamą atstumą em erdvėje.|
|F2Dot14| 16 bitų pasirašytas fiksuotas skaičius, o mažieji 14 bitų reiškia trupmeną.|
|longDateTime|	The long internal format of a date in seconds since 12:00 midnight, January 1, 1904. It is represented as a signed 64-bit integer.|

### Šriftų katalogas

Pirmoji TrueType šrifto lentelė yra šriftų katalogas, suteikiantis prieigą prie informacijos, reikalingos norint pasiekti duomenis kitose lentelėse. Be to, jį sudaro:

 * Poslinkio sublentelė – saugo lentelių šrifto įrašus ir teikia poslinkio informaciją, kad būtų galima pasiekti kiekvieną lentelę kataloge
 * Lentelių katalogas – yra kiekvienos šrifto lentelės įrašai

#### Poslinkio sublentelė
Poslinkio sublentelė parodyta žemiau.

|**Tipas**|**Pavadinimas**|**Aprašymas**|
---|---|---|
|uint32| skalerio tipas| Žyma, nurodanti OFA mastelio keitiklį, kuris bus naudojamas šiam šriftui rastruoti; Norėdami gauti daugiau informacijos, žr. pastabą apie skalerio tipą toliau.|
|uint16| numTables| lentelių skaičius|
|uint16| paieškaRange| (didžiausia galia 2 <= numTables)*16|
|uint16| įrašasSelector| log2(didžiausia 2 galia <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Lentelių katalogas
Lentelės katalogas yra iškart po poslinkio antrinės lentelės. Jo struktūra yra tokia, kaip parodyta šioje lentelėje.

|**Tipas**|**Pavadinimas**|**Aprašymas**|
---|---|---|
|uint32| žyma| 4 baitų identifikatorius|
|uint32| kontrolinė suma| šios lentelės kontrolinė suma|
|uint32| kompensuoti| poslinkis nuo sfnt| pradžios
|uint32| ilgis| šios lentelės ilgis baitais (tikrasis ilgis nepaminkštintas)|

Kiekviena šrifto failo lentelė turi turėti savo lentelės katalogo įrašą. Įrašai lentelėje turi būti rūšiuojami didėjimo tvarka pagal žymą.


## Nuorodos
 * [TrueType Font Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
 * [TrueType apžvalga](https://learn.microsoft.com/en-us/typography/truetype/)

