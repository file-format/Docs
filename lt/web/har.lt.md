{
  "date": "2021-07-08",
  "keywords": [
"HAR",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"JSON",
"Archyvo failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAR – HTTP archyvo failo formatas",
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra HAR failas ir API, kurios gali sukurti ir atidaryti HAR failą.",
  "linktitle": "HAR",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ha-ltr"
}
},
  "lastmod": "2021-07-08"
}

## Kas yra HAR failas?

Failas su .har (HTTP archyvo) failu yra HTTP archyvo failas, kuriame saugomi seanso duomenys, perduodami per daugelį naršyklių (pvz., Chrome, Safari, IE, Firefox ir kt.) [JSON](/web/json/) failo formatu. Duomenys, perduodami internetu tarp serverio ir kliento (šiuo atveju vartotojo naršyklės), turi HTTP užklausų ir atsakymų antraštes, kurios yra saugomos HAR faile. Jame taip pat pateikiama išsami informacija apie į naršyklę įkeltų tinklalapių našumo duomenis. HAR failus galima atidaryti bet kuriame teksto rengyklėje, pvz., Notepad Microsoft Windows OS ir TextEdit Apple MacOS.

## HAR failo formatas – daugiau informacijos

HAR failuose seanso informacija saugoma paprasto teksto faile, naudojant populiarų JSON formatą. HAR failo formato specifikacijas parengė Pasaulio žiniatinklio konsorciumo (W3C) Web Performance Group, tačiau jų paskelbti nepavyko. Tačiau jis sėkmingai apibrėžė HTTP operacijų archyvinį formatą.

Kūrėjai ne tik stebi užklausų ir atsakymų informacijos perdavimą, bet ir naudoja HAR failus, kad registruotų žiniatinklio naršyklės našumą, atsižvelgiant į puslapio įkėlimo greitį, turinio įkėlimo trukmę, įkeltą turinį, užklausas, vykdomas norint gauti atsakymą iš naršyklės ir daugelį kitų. .

## Kodėl verta naudoti HAR failus?

HAR failai gali padėti pagerinti svetainės našumą, įvertinant ilgą įkėlimo laiką, puslapio pateikimo laiką ir atsako laiką. HAR failus galima analizuoti, kad būtų galima rasti tokias problemas ir išspręsti visas su svetaine susijusias problemas, siekiant pagerinti našumą.

## Kaip sugeneruoti HAR failą?

Taigi, kaip sukurti HAR failą? Na, tai priklauso nuo to, kokio tipo naršyklę naudojate generuodami HAR failą. Šiame vadove pateikiame Google Chrome naršyklės veiksmus. HAR failų generavimo metodų naudojant Safari, Firefox ir kt. galima lengvai ieškoti internete ir sekti.

### Veiksmai, skirti generuoti HAR failą naudojant Google Chrome.

Toliau nurodytus veiksmus galima atlikti tinklalapyje, kuriame kyla problemų.

 1. Google Chrome atidarykite tinklalapį, kuriame kilo problema.
 1. Atidarykite kūrėjo įrankį (patikrinti elementą).
 1. Eikite į kairę skydelio pusę, kad pradėtumėte failo įrašymą. Šioje dalyje yra mažas apvalus raudonas mygtukas.
 1. Spustelėkite Išvalyti piktogramą, kad ištrintumėte visus naršyklėje saugomus žurnalo įrašus.
 1. Norėdami išsaugoti norimą turinį, kaip parodyta aukščiau, dešiniuoju pelės mygtuku spustelėkite ir spustelėkite Išsaugoti kaip HAR failą.

## Nuorodos

* [HAR failo formatas – Vikipedija](https://en.wikipedia.org/wiki/HAR_(file_format))


