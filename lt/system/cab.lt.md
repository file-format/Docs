{
  "date": "2021-06-29",
  "keywords": [
"TAKSI",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Windows kabineto failas",
"Microsoft",
"Montuotojas",
"Sąranka",
"AdvPak"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CAB – „Windows“ kabineto failas",
  "description": "Sužinokite apie CAB failo formatą ir API, kurios gali kurti ir atidaryti CAB failus.",
  "linktitle": "CAB",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ca-ltb"
}
},
  "lastmod": "2021-06-29"
}

## Kas yra CAB failas? ##

Failas su plėtiniu .cab priklauso Windows kabineto failui, kuris priklauso sistemos failų kategorijai. Tai failas, kuris išsaugomas archyvo failo formatu Microsoft Windows versijose, kurios palaiko suspaustų duomenų algoritmus, pvz., [LZX](/compression/lzx/), Quantum ir [ZIP](/compression/zip/). Failas yra labai svarbus, kai vartotojas ar kūrėjas nori turėti programinės įrangos diegimo duomenis ir failus ir jais dalytis. Dėl duomenų be nuostolių glaudinimo ir į šiuos failus įtraukto skaitmeninio sertifikavimo šis failas puikiai tinka tokiems failams saugoti ir dalytis. Jis palaiko įvairias Microsoft diegimo programas, tokias kaip Device Installer, SetUp API ir AdvPak.

## Trumpa istorija ##

CAB failas yra duomenų glaudinimo failo tipas, kurį sukūrė Microsoft. Iš pradžių jis buvo vadinamas Deimantu, bet vėliau jis tapo žinomas kaip CAB failas, trumpinys iš žodžio kabinetas.

## Techninė specifikacija Nr.

CAB faile paprastai gali būti ne daugiau kaip 65 535 aplankai, kuriuose savo ruožtu gali būti daugiausia 65 536 failai. CAB failų saugojimo mechanizmas taupo laiką ir erdvę, nes kiekvieną aplanką išsaugo kaip suglaudintą bloką, o ne suglaudina ir saugo kiekvieną failą atskirai. Tušti aplankai negali būti saugomi CAB archyvo aplankuose. CAB failą pirmą kartą sukūrė Microsoft ir jis naudojamas įvairiose diegimo programose, pvz., InstallShield su šiek tiek kitokiu formatu. CAB failai paprastai yra prijungti prie savaiminio išskleidimo programų. Microsoft CAB failai yra lengvai atpažįstami dėl jų unikalaus žymeklio, padedančio nustatyti formatą. Unikalus visų Microsoft CAB failų žymeklis yra keturių žodžių priešdėlis MSCF. Pamatęs šį kodą, vartotojas gali lengvai atskirti Microsoft CAB failą nuo kitų failų ir atitinkamai naudoti jį kompresoriuose ar versijose. Failus galima suglaudinti naudojant daugiau programinės įrangos diegimo duomenų arba esamus duomenis galima išspausti naudojant tinkamą programinę įrangą.


## CAB pavyzdys Nr.

Šis pavyzdys iliustruoja ryšį tarp failų ir aplankų CAB failų struktūroje:

{{< figure src="../cab.png" alt="CAB failo formatas" >}}

## Nuoroda ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
