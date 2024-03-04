{
  "date": "2019-12-10",
  "keywords": [
"CSV",
"failą",
"pratęsimas",
"Dokumento formatas",
"Kableliais atskirtos reikšmės",
"Skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie CSV failo formatą ir API, kurios gali kurti ir atidaryti CSV failus.",
  "title": "CSV failo formatas",
  "linktitle": "CSV",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-cs-ltv"
}
},
  "lastmod": "2019-12-10"
}

## Kas yra CSV failas?

Failai su plėtiniu .csv (kableliais atskirtos reikšmės) yra paprasto teksto failai, kuriuose yra duomenų įrašų su kableliais atskirtomis reikšmėmis. Kiekviena CSV failo eilutė yra naujas įrašas iš faile esančių įrašų rinkinio. Tokie failai generuojami, kai ketinama perkelti duomenis iš vienos saugojimo sistemos į kitą. Kadangi visos programos gali atpažinti kableliais atskirtus įrašus, tokių duomenų failų importavimas į duomenų bazę atliekamas labai patogiai. Beveik visos skaičiuoklių programos, tokios kaip Microsoft Excel arba OpenOffice Calc, gali importuoti CSV failą be didelių pastangų. Duomenys, importuoti iš tokių failų, yra išdėstyti skaičiuoklės langeliuose, kad būtų galima pateikti vartotojui.

## Trumpa istorija ##

Toliau pateikiami keli faktai apie CSV failo formato kilmę ir istoriją.

* 1972 m. – IBM Fortran (išplėstinis H lygis) kompiliatorius palaikė juos OS/360


* 1978 m. – FORTRAN 77 palaiko į sąrašą nukreiptą įvestį/išvestį, kuri skyrėjams naudojo kablelius ir tarpus


* 2005 m. – CSV buvo standartizuotas naudojant [RFC4180](https://tools.ietf.org/html/rfc4180) kaip MIME turinio tipą.


* 2013 m. – RFC4180 trūkumai buvo pašalinti pagal W3C rekomendaciją


* 2015 m. – W3C parengė pirmuosius rekomendacijų dėl CSV metaduomenų standartų projektus, kurie prasidėjo kaip rekomendacija 2015 m. gruodžio mėn.


## Konvertuoti CSV failus ##

CSV failus galima konvertuoti į kelis skirtingus failų formatus naudojant programas, kurios gali atidaryti šiuos failus. Pavyzdžiui, Microsoft Excel gali importuoti duomenis iš CSV failo formato ir išsaugoti XLS, [XLSX](/spreadsheet/xlsx/), [PDF](/pdf/), [TXT](/word-processing/txt/), XML ir [HTML](/web/html/) failų formatais. Panašiai, kitos darbalaukio ir internetinės paslaugos suteikia galimybę eksportuoti CSV failus į HTML, ODS ir [RTF](/word-processing/rtf/).

## CSV failo formatas ##

Žinoma, kad CSV failo formatas nurodytas [RFC4180](https://tools.ietf.org/html/rfc4180). Jis apibrėžia, kad bet kuris failas yra suderinamas su CSV, jei:

* Kiekvienas įrašas yra atskiroje eilutėje, atskirtoje eilutės lūžiu (CRLF). Pavyzdžiui:

  * aaa,bbb,ccc CRLF
  * zzz, yyy, xxx CRLF
* Paskutinis failo įrašas gali turėti arba neturėti pabaigos eilutės lūžio. Pavyzdžiui:

  * aaa,bbb,ccc CRLF
  * zzz, yyy, xxx
* Gali būti pasirenkama antraštės eilutė, kuri bus rodoma kaip pirmoji failo eilutė su tokiu pačiu formatu kaip ir įprastos įrašo eilutės. Šioje antraštėje bus pavadinimai, atitinkantys failo laukus ir turi būti tiek pat laukų, kiek ir įrašai likusioje failo dalyje (antraštės eilutės buvimas ar nebuvimas turėtų būti nurodytas pasirenkamu parametru „antraštė“ MIME tipas). Pavyzdžiui:

  * lauko_pavadinimas,lauko_pavadinimas,lauko_pavadinimas CRLF
  * aaa,bbb,ccc CRLF
  * zzz, yyy, xxx CRLF
* Antraštėje ir kiekviename įraše gali būti vienas ar daugiau laukų, atskirtų kableliais. Kiekvienoje eilutėje turi būti tiek pat laukų visame faile. Tarpai laikomi lauko dalimi ir neturėtų būti ignoruojami. Po paskutinio įrašo lauko negali būti kablelio. Pavyzdžiui:

  * aaa,bbb,ccc
* Kiekvienas laukas gali būti arba negali būti parašytas dvigubomis kabutėmis (tačiau kai kurios programos, pvz., Microsoft Excel, iš viso nenaudoja dvigubų kabučių). Jei laukuose nėra dvigubų kabučių, dvigubų kabučių laukuose gali nebūti. Pavyzdžiui:\

  * aaa, bbb, ccc CRLF
  * zzz, yyy, xxx
* Laukai, kuriuose yra eilučių lūžių (CRLF), dvigubos kabutės ir kableliai, turi būti pateikiami dvigubose kabutėse. Pavyzdžiui:

  * aaa, b CRLF
  * bb, ccc CRLF
  * zzz, yyy, xxx
* Jei laukams įterpti naudojamos dvigubos kabutės, lauke esančios dvigubos kabutės turi būti pašalintos, prieš ją įrašant kitą dvigubą kabutę. Pavyzdžiui:

  * aaa, b bb, ccc

Tačiau, atsižvelgiant į šiuolaikinę vartoseną, skyriklis neapsiriboja tik kableliu ir gali būti kabliataškis, skirtukas arba tarpai. Tokios programos kaip Microsoft Excel suteikia galimybę nurodyti skiriamąjį simbolį įrašams importuoti iš CSV failo.

## Nuorodos

* [RFC 4180](https://tools.ietf.org/html/rfc4180)

* [RFC 2048](https://tools.ietf.org/html/rfc2048)

* [CSV – Vikipedija](https://en.wikipedia.org/wiki/Comma-separated_values)


