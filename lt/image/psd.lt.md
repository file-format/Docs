{
  "date": "2019-10-11",
  "keywords": [
"psd failą",
"psd failo formatas",
"kas yra psd failas",
"failą",
"psd pavyzdys",
"psd failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSD – „Photoshop“ vaizdo failo formatas",
  "description": "Sužinokite apie PSD failo formatą ir API, kurios gali kurti ir atidaryti PSD failus.",
  "linktitle": "PSD",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-ltd"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PSD failas?

PSD, Photoshop dokumentas, yra Adobe Photoshop vietinis failo formatas, naudojamas grafikos projektavimui ir plėtrai. PSD failuose gali būti vaizdo sluoksnių, reguliavimo sluoksnių, sluoksnių kaukių, komentarų, failo informacijos, raktinių žodžių ir kitų Photoshop būdingų elementų. Photoshop failų numatytasis plėtinys yra .PSD, didžiausias jų aukštis ir plotis – 30 000 pikselių, o ilgis – du gigabaitai.

## PSD failo formato specifikacijos ##

Duomenys PSD faile saugomi didžiąja baitų tvarka. Tai reiškia, kad skaitant ar rašant Windows platformoje reikia keisti trumpuosius ir ilgus sveikuosius skaičius. Photoshop failo formatas yra padalintas į penkias pagrindines dalis. Jame yra daug ilgio žymeklių, kuriuos galima naudoti norint pereiti iš vienos dalies į kitą. Ilgio žymekliai paprastai užpildomi baitais, kad būtų suapvalinti iki artimiausio 2 arba 4 baitų intervalo. Penkios pagrindinės dalys yra:

* Failo antraštė

* Spalvų režimo duomenys

* Vaizdo ištekliai

* Informacija apie sluoksnį ir kaukę

* Vaizdo duomenys


Siekiant atitikties, duomenys turėtų būti įrašomi į visus šiuos skyriaus laukus, nes Photoshop gali bandyti perskaityti visą skyrių. Tai taip pat reiškia, kad rašant į failą į praleistus laukus įrašomi nuliai. Ilgio laukas ilgio skyriuose turėtų būti naudojamas norint nuspręsti, kada nutraukti skaitymą. Daugeliu atvejų ilgio lauke nurodomas sekančių baitų, o ne įrašų, skaičius. Skaitant failą reikia atsiminti šiuos dalykus.

* Vertės stulpelyje „Ilgis“ visose lentelėse pateikiamos baitais.

* Visos reikšmės, apibrėžtos kaip Unicode eilutė, susideda iš:

* 4 baitų ilgio laukas, nurodantis simbolių skaičių eilutėje (ne baitais).

* Unikodo reikšmių eilutė, du baitai vienam simboliui.


### Failo antraštė ###

Failo antraštėje yra pagrindinės vaizdo savybės.

|Ilgis|Aprašymas
---|---|
|4|Parašas: visada lygus '8BPS' . Nebandykite perskaityti failo, jei parašas neatitinka šios reikšmės.
|2|Version: always equal to 1. Nebandykite skaityti failo, jei versija neatitinka šios reikšmės. (~*~*PSB~*~* versija yra 2.)
|6|Rezervuota: turi būti nulis.
|2|Kanalų skaičius vaizde, įskaitant visus alfa kanalus. Palaikomas diapazonas yra nuo 1 iki 56.
|4|Vaizdo aukštis pikseliais. Palaikomas diapazonas yra nuo 1 iki 30 000.
|4|Vaizdo plotis pikseliais. Palaikomas diapazonas yra nuo 1 iki 30 000.
|2|Gylis: bitų skaičius kanale. Palaikomos reikšmės yra 1, 8, 16 ir 32.
|2|Failo spalvų režimas. Palaikomos reikšmės yra: Bitmap # 0; Pilkos spalvos # 1; Indeksuotas # 2; RGB # 3; CMYK # 4; Daugiakanalis # 7; Duotone # 8; 9 laboratorija.

### Spalvų režimo duomenų skyrius ###

Spalvų režimo duomenų skyriaus struktūra yra tokia:


|Ilgis|Aprašymas
---|---|
|4|Šių spalvų duomenų ilgis
|kintamasis|Spalvų duomenys

Spalvų režimo duomenys pasiekiami tik indeksuotoms spalvoms ir dvitoniams, kaip apibrėžta režimo lauke Failo antraštėje. Visiems kitiems režimams ši sekcija pavaizduota 4 baitų reikšmėmis su nuliu. Indeksuotų spalvotų vaizdų ilgis yra 768, o spalvų duomenyse yra vaizdo spalvų lentelė, išdėstyta be tarpinių. Duotone vaizdų spalvų duomenyse yra dvitonės specifikacijos (kurios formatas nėra dokumentuotas). Kitos programos, skaitančios Photoshop failus, gali dvitonio atvaizdą traktuoti kaip pilką vaizdą ir tiesiog išsaugoti dvitonės informacijos turinį skaitant ir rašant failą.

### Vaizdo išteklių skyrius ###

Trečioje failo dalyje yra vaizdo ištekliai. Jis prasideda ilgio lauku, po kurio seka išteklių blokų serija.


|Ilgis|Aprašymas
---|---|
|4|Vaizdo išteklių skyriaus ilgis. Ilgis gali būti lygus nuliui.
|Kintamasis|Vaizdo ištekliai (vaizdo išteklių blokai)

Vaizdo ištekliai naudojami ne pikselių duomenims, susijusiems su vaizdais, pvz., rašiklio įrankio takais, saugoti. Jie vadinami išteklių blokais, nes juose saugomi duomenys, kurie buvo saugomi Macintosh šaltinyje ankstyvosiose Photoshop versijose. Pagrindinė vaizdo išteklių blokų struktūra yra tokia, kaip parodyta toliau:


|Ilgis|Aprašymas
---|---|
|4|Parašas: 8BIM
|2|Unikalus ištekliaus identifikatorius. Vaizdo išteklių ID yra Photoshop naudojamų išteklių ID sąrašas.
|Kintamasis|Pavadinimas: Paskalio eilutė, užpildyta, kad dydis būtų lygus (nulinį pavadinimą sudaro du 0 baitai)
|4|Faktinis toliau pateikiamų išteklių duomenų dydis
|Kintamasis|Išteklių duomenys, aprašyti skyriuose apie atskirus išteklių tipus. Jis yra paminkštintas, kad dydis būtų vienodas.

Vaizdo ištekliai naudoja kelis standartinius ID numerius.

### Informacija apie sluoksnį ir kaukę ###

Ketvirtajame Photoshop failo skyriuje yra informacijos apie sluoksnius ir kaukes, pvz., sluoksnių skaičių, sluoksnių kanalus, maišymo diapazonus, reguliavimo sluoksnių klavišus, efektų sluoksnius ir kaukės parametrus. Jei nėra sluoksnių ar kaukių, ši sekcija vaizduojama nuliniu 4 baitų lauku. Skaitant šį skyrių ypatingas dėmesys turi būti skiriamas sekcijų ilgiui dėl nulinių verčių. Sluoksnio ir kaukės skyriaus išdėstymas yra toks:


|Ilgis|Aprašymas
---|---|
|4|Sluoksnio ir kaukės informacijos skyriaus ilgis. (PSB ilgis yra 8 baitai.)
|Kintamas|Sluoksnio informacija
|Kintamas|Informacija apie pasaulinę sluoksnio kaukę
|Kintamasis|Pažymėtų blokų, kuriuose yra įvairių tipų duomenų, serija.

#### Sluoksnio informacija ####

Šioje lentelėje parodytas aukšto lygio informacijos organizavimas.


|Ilgis|Aprašymas
---|---|
|4|Length of the layers info section, rounded up to a multiple of 2. (PSB ilgis yra 8 baitai.)
|2|Sluoksnių skaičius. Jei skaičius yra neigiamas, jo absoliuti reikšmė yra sluoksnių skaičius, o pirmame alfa kanale yra sujungto rezultato skaidrumo duomenys.
|Kintamas|Informacija apie kiekvieną sluoksnį. Žr. Sluoksnio įrašai aprašo kiekvieno sluoksnio informacijos struktūrą.
|Kintamas|Kanalo vaizdo duomenys. Yra vienas ar daugiau vaizdo duomenų įrašų kiekvienam sluoksniui. Sluoksniai yra tokia pat tvarka kaip ir sluoksnio informacijoje

### Vaizdo duomenys ###

Vaizdo pikselių duomenys yra failo skiltyje Vaizdo duomenys. Duomenų išdėstymas vaizdo duomenų skiltyje yra plokštumos tvarka, ty pirmiausia visi raudoni duomenys, tada visi žali duomenys ir tt Kiekviena plokštuma saugoma nuskaitymo eilutės tvarka, be baitų. Vaizdo duomenų sekcija yra išdėstyta formatu kaip parodyta tolesnėje lentelėje.

|Ilgis|Aprašymas
---|---|
|2|Compression method: *0 = Raw image data * 1 = RLE suspaustas vaizdo duomenys prasideda nuo visų nuskaitymo eilučių (eilučių * kanalų) baitų skaičiaus, o kiekvienas skaičius išsaugomas kaip dviejų baitų reikšmė. Toliau pateikiami RLE suspausti duomenys, kiekviena nuskaitymo linija suglaudinama atskirai. RLE glaudinimas yra tas pats glaudinimo algoritmas, kurį naudoja Macintosh ROM įprasta PackBits ir TIFF standartas. *2 = ZIP be numatymo *3 = ZIP su numatymu.
|Kintamasis|Vaizdo duomenys. Plokštuminė tvarka = RRR GGG BBB ir kt.

## Nuorodos Nr.

* [PSD failo formato specifikacijos – pateikė „Adobe“](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)

* [Adobe Photoshop failo formatas](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


