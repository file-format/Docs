{
  "date": "2019-10-11",
  "keywords": [
"AVI",
"Suspaustas garso vaizdo įrašas",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Multimedijos konteineris",
"XVId",
"DivX",
"Kodekai",
"Išteklių mainų failo formatas",
"RIFF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AVI failo formatas – garso ir vaizdo įrašų tarpinis failas",
  "description": "Sužinokite apie AVI failo formatą ir API, kurios gali kurti ir atidaryti AVI failus.",
  "linktitle": "AVI",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-av-lti"
}
},
  "lastmod": "2021-04-23"
}

## Kas yra AVI failas? ##

**AVI** failo formatas yra garso ir vaizdo daugialypės terpės konteinerio failo formatas, kurį pristatė Microsoft. Jame saugomi garso ir vaizdo duomenys, sukurti ir suspausti naudojant kelis kodekus (koderius/dekoderius), pvz., **XVid** ir **DivX**. Kadangi AVI turiniui koduoti gali būti naudojami skirtingi kodekai, nuskaitančios programos, ty AVI grotuvai, turėtų galėti juos atidaryti tik tuo atveju, jei jose yra įdiegti reikalingi kodekai, su kuriais buvo sukurtas AVI turinys. Formatas pagal numatytuosius nustatymus palaikomas visose **Microsoft Windows** platformose ir beveik visose kitose pagrindinėse platformose. Kelios programos ir API suteikia galimybę kurti / įrašyti, skaityti ir konvertuoti AVI į kitus populiarius formatus, tokius kaip MP4, MOV, WMV ir kt.

## AVI failo formatas ##

Failas su plėtiniu .avi yra AVI failas. Tai RIFF (Resource Interchange File Format) antrinis formatas. RIFF suskirsto duomenis į blokus arba gabalus, kurie identifikuojami FourCC žyma. AVI failas yra tiesiog vienas gabalas RIFF formato faile.

Pirmajame pogrupyje failo antraštė identifikuojama pagal hdrl žymą; jo turinys apima vaizdo įrašo plotį, aukštį ir kadrų dažnį. Antroje dalyje judesio žyma nurodo vaizdo įrašo kadrų dažnį. AVI vaizdo įrašą sudaro tikri garso / vaizdo duomenys šioje dalyje. Taip pat yra trečias pasirenkamas pogrupis su idx1 žyma, kuri nurodo atskirų failo duomenų dalių, priklausančių failui, vietą faile.

### Apribojimai ###

* Kraštinių santykio informacija negali būti užkoduota originalioje AVI specifikacijoje, nors vėlesnė OpenDML specifikacija (AVI 2.0) siūlo standartizuotą metodą

* Nors AVI failai yra plačiai naudojami filmų ir televizijos postprodukcijoje, įvairūs laiko kodo pridėjimo būdai konkuruoja, o tai turi įtakos formato naudojimui.

* Vaizdo įrašo faile, užkoduotame AVI formatu, negalima naudoti glaudinimo technikos, kuriai reikalingi būsimų kadrų duomenys už koduojamo kadro ribų (B kadras)

* Sunku naudoti AVI failus su kintamu bitų dažniu (VBR) (pvz., MP3 garsą, kai atrankos dažnis mažesnis nei 32 kHz)

* AVI failas, koduojantis standartinės raiškos vaidybinius filmus, kaip įprastai naudojamas, gali patirti apie 5 MB per valandą, priklausomai nuo to, kaip failas naudojamas.

* Subtitrai turi būti užkoduoti vaizdo įrašų sraute arba išplatinti atskirame faile, jei AVI failuose negali būti priedų, pvz., šriftų ir subtitrų


## Trumpa istorija ##

AVI pristatė Microsoft 1992 m., siekdama pateikti patikimesnį ir pažangesnį garso ir vaizdo failų formatą. Formatas greitai išpopuliarėjo naudojant internetą, leisdamas asmenims tiesiogiai ir netiesiogiai dalytis vaizdo failais per debesyje pagrįstą medijos saugyklą.

## Nuorodos Nr.

* [AVI – pateikė Vikipedija](https://en.wikipedia.org/wiki/Audio_Video_Interleave)


