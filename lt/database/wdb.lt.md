{
  "date": "2021-08-24",
  "keywords": [
"wdb failą",
"wdb failo formatas",
"kas yra wdb failas",
"failą",
"wdb pavyzdys",
"wdb failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie WDB failo formatą ir API, kurios gali kurti ir atidaryti WDB failus.",
  "title": "WDB – SQL serverio sekimo failas",
  "linktitle": "WDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-wd-ltb"
}
},
  "lastmod": "2021-08-24"
}

## Kas yra WDB failas?
Failas su plėtiniu .wdb iš tikrųjų yra Microsoft Works sukurtas duomenų bazės failas, kuris buvo naudojamas atlikti tokias funkcijas kaip duomenų bazės valdymo sistema. WDB failas panašus į Access Database ([MDB](/database/mdb/)) failą, bet ne toks efektyvus ir didesni apribojimai. WDB failų negalima atidaryti naudojant Microsoft Access. Tačiau galite atidaryti WDB failą Microsoft Works ir eksportuoti jį į MDB failą, kad atidarytumėte WDB failą MS Access.

## WDB failo formatas
Microsoft Works duomenų bazė yra vietinis Microsoft Works biuro rinkinio duomenų bazės formatas. Dėl formato nuosavybės ir tam tikrų apribojimų. WDB failų negalima atidaryti jokia kita programine įranga, išskyrus Microsoft Works. Failo formatu pasikartojančią 10 baitų antraštę galima rasti prieš kiekvieną ASCII teksto eilutę, vaizduojančią laukų reikšmes, kurios buvo užbaigtos NULL reikšme. Antraštė paprastai prasideda **\x0f** baitu ir NULL, po to seka 4 duomenų baitai, pakaitomis su NULL.

### Failo struktūra

WDB failo struktūra pateikta žemiau:
- **1-oji antraštė**: nuo failo pradžios, baigiant \x25\x00\xf2 ir 244 NULL baitais
- **2-oji antraštė**: prasidedanti \xffT – ty \xff\x54 ir besitęsianti iki 4096 baitų, kurioje yra stulpelių / laukų pavadinimai ir kiti dalykai, ir atrodo, kad ji prasideda 6144 baito pozicijoje.
- **Field**: value has a 10 byte header, with the following format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3, part 2} {db 4} \x00. 2 duomenų baitas yra lauko numeris, 3 duomenų baitas yra įrašo numeris (pridedant 3 duomenų baitą, 2 dalį, kai viršija 256 įrašus).


## Nuorodos Nr.

* [Vartotojas:JesseW/wdb formatas](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)


