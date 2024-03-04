{
  "date": "2021-05-03",
  "keywords": [
"SDF",
"sdf failą",
"kas yra sdf failas",
"kaip atidaryti sdf failą",
"pratęsimas",
"failą",
"sdf failo formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie SDF failo formatą ir API, kurios gali kurti ir atidaryti SDF failus.",
  "title": "SDF – SQL serverio kompaktiškas duomenų bazės failas",
  "linktitle": "SDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sd-ltf"
}
},
  "lastmod": "2021-05-03"
}

## Kas yra SDF failas?
Faile su .sdf plėtiniu yra Microsoft SQL Server Compact (SQL CE) duomenų bazė, kuri taip pat žinoma kaip kompaktiška reliacinė duomenų bazė; Microsoft sukūrė programoms, skirtoms mobiliesiems įrenginiams ir staliniams kompiuteriams. Jis palaiko ir 32, ir 64 bitų operacinę sistemą, o visas duomenų bazės turinys yra įtrauktas į vieną SDF failą ir gali užimti daugiau nei 4 GB vietos diske. Saugumo sumetimais .sdf failas gali būti užšifruotas 128 bitų šifravimu. SQL CE vykdymo laikas nustato lygiagrečią kelių vartotojų prieigą prie .sdf failo. SDF failą galima nukopijuoti naudojant **QuickOnce** arba tiesiog jį galima nukopijuoti į paskirties vietą, kad būtų galima įdiegti sistemą.

## SDF failo formatas
SDF faile yra duomenų bazė, kuri paprastai vadinama kompaktine reliacine duomenų baze. SDF faile yra visa su duomenų baze susijusi informacija, o SQL Server Compact yra lengvas ir nemokamas duomenų bazės variklis, naudojamas .sdf failams valdyti. .sdf failo dydis neturėtų viršyti 4 GB dydžio limito. SDF failuose nesaugoma informacija apie saugomas procedūras, aktyviklius ar rodinius. Programoms, naudojančioms SQL CE duomenų bazę, ADO.NET ryšio eilutėje nereikia nurodyti kelio į SDF failą, vietoj to jis gali būti minimas kaip |DataDirectory|\database_name.sdf, apibrėžiantis duomenų katalogą, apibrėžtą programos surinkimo manifeste
.sdf pavadinimo susitarimas yra neprivalomas, o failui išsaugoti galima naudoti bet kokį plėtinį. Duomenų bazės failo slaptažodžio nustatymas yra neprivalomas veiksmas. Norėdami suspausti arba pataisyti duomenų bazę, failas turi būti išsaugotas naudojant **suglaudinta / suremontuota duomenų bazė** parinktį.

## Nuorodos

 * [SQL Server Compact – Vikipedija](https://en.wikipedia.org/wiki/SQL_Server_Compact)
 * [SQL Server Compact naudojimas ASP.NET žiniatinklio programoms](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


