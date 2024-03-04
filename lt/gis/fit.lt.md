{
  "date": "2022-05-06",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FIT failo formatas – Garmin veiklos failas",
  "description": "Sužinokite apie FIT failo formatą ir API, kurios gali kurti ir atidaryti FIT failus.",
  "linktitle": "FIT",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-fi-ltt"
}
},
  "lastmod": "2022-05-06"
}

## Kas yra FIT failas?

FIT failas yra GIS failas, sukurtas Garmin sportinių nešiojamų įrenginių. Jis naudojamas fiksuoti asmens veiklą, kai jis juda dėvėdamas šiuos prietaisus. Veiklos duomenys apima GPS įrenginio įrašytą vietą ir laiką. FIT failai taip pat naudojami įrašytiems veiklos duomenims perkelti naudojant žiniatinklio API. Štai kodėl FIT failai yra dažniausiai naudojamas failų formatas dalintis kūno rengybos duomenimis su kitomis kūno rengybos platformomis. Kiti įprasti failų formatai yra [GPX](/gis/gpx/), TCX ir [KML](/gis/kml/).

## FIT failo formatas – daugiau informacijos

FIT failai išsaugomi diske kaip dvejetainiai failai su Garmin įrenginių įrašyta informacija apie veiklą. FIT faile saugoma informacija apima:

 * Data ir laikas
 * Sporto rūšys
 * Duomenų perkėlimas ir padalijimas
 * GPS takelis
 * Jutiklio duomenys
 * Renginiai aktyviems užsiėmimams

Veiklos duomenys gali būti įrašomi į failą realiuoju laiku arba eksportuojami, kai veiklos įrašymas baigtas.

### FIT veiklos pranešimai

FIT veiklos faile gali būti kai kurių būtinų pranešimų tipų. Toliau pateikiami būtini pranešimai veiklos failui.

|Pranešimas|Tikslas|
---|---|
|Failo ID| Failo ID pranešimas reikalingas visiems FIT failų tipams ir turėtų būti pirmasis failo pranešimas. Veiklos failams ypatybė Type turėtų būti nustatyta į 4.|
|Veikla| FIT veiklos faile būtinas vienas veiklos pranešimas. Į veiklos pranešimą įtrauktos vietos laiko žymos ir seansų skaičiaus ypatybės. Vietinė laiko žyma naudojama norint nustatyti laiko juostos poslinkį, kuris gali būti taikomas visoms failo laiko žymoms. Dauguma įrenginių įrašo FIT failus realiuoju laiku, o seansų skaičius bus nežinomas iki įrašymo pabaigos. Dėl šios priežasties veiklos pranešimas dažnai bus paskutinis failo pranešimas.|
|Seansas| Veiklos failuose bus vienas ar daugiau seanso pranešimų. Seanso pranešimas yra suvestinės pranešimo tipas. Pradžios laikas, Bendras praėjęs laikas, Bendras laikmačio laikas ir Laiko žyma yra privalomi visų suvestinių pranešimų laukai.|
|Ratas| Rapų pranešimai nurodo ratus arba intervalus sesijos metu. Lapo pranešimas yra suvestinės pranešimo tipas. Pradžios laikas, Bendras praėjęs laikas, Bendras laikmačio laikas ir Laiko žyma yra privalomi visų suvestinių pranešimų laukai.|
|Įrašas| Įrašyti pranešimai apima GPS koordinates, greitį, atstumą, širdies ritmą, galią ir kt.|

## FIT failas, naudingi ištekliai

 * [FIT veiklos failų dekodavimas](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
 * [FIT veiklos failų kodavimas](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 
## Nuorodos Nr.

* [FIT veiklos failas](https://developer.garmin.com/fit/file-types/activity/)


