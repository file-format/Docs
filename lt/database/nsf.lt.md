{
  "date": "2020-11-11",
  "keywords": [
"NSF",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie NSF failo formatą ir API, kurios gali kurti ir atidaryti NSF failus.",
  "title": "NSF failo formatas – Lotus Notes duomenų bazės formatas",
  "linktitle": "NSF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ns-ltf"
}
},
  "lastmod": "2020-08-12"
}

## Kas yra NSF failas?

Failas su plėtiniu .nsf (Notes Storage Facility) yra duomenų bazės failo formatas, naudojamas [IBM Notes software](https://en.wikipedia.org/wiki/HCL_Notes), kuris anksčiau buvo žinomas kaip Lotus Notes. Ji apibrėžia schemą, skirtą įvairių tipų objektams, tokiems kaip el. laiškai, susitikimai, dokumentai, formos ir rodiniai, saugoti. Visa ši informacija yra viename verslo bendradarbiavimo NSF faile, panašiame į PST/OST failą. Kai kurios programos, galinčios atidaryti NSF failus, yra IBM Lotus Notes ir IBM Domino.

## NSF failo formato specifikacijos

NSF failai yra dvejetainio pobūdžio, o jų specifikacijas pateikia Joachimas Metzas adresu [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Remiantis šia informacija, NSF failą sudaro:

 * Failo antraštė
 * Duomenų bazės antraštė

Be to, jį sudaro:

 * Superblokas
 * Sezono aprašo blokas
 * Bitmap
 * Įrašų perkėlimo vektorinis kibiras
 * Suvestiniai kibirai
 * Ne apibendrinti kibirai


### NSF failo antraštė

NSF failo antraštė yra 6 baitų dydžio. Tai susideda iš:

|Poslinkis|Dydis|Vertė|Aprašymas|
---|---|---|---|
0|2|0x1a 0x00|Parašas|
2|4| |Duomenų bazės antraštės dydis|

### Duomenų bazės antraštė

NSD duomenų bazės antraštėje yra šios patvirtintos reikšmės.

 * Duomenų bazės informacija
   * Duomenų bazės identifikatorius (DBID)
 * Replikacijos informacija
 * Duomenų bazės informacijos buferio vėliavėlės
   * Pavadinimas
   * Kategorijos
   * Klasė
   * Dizaino klasė (šablono pavadinimas)
 * Specialūs pastabų identifikatoriai
 * Paminkštinimas
 * Duomenų bazės informacija 2
 * Duomenų bazės informacija 3
 * Informacija apie duomenų bazę 4
 * Duomenų bazės informacija 5
 * Paminkštinimas
 * Duomenų bazės egzemplioriaus identifikatorius (DBIID)
 * Replikacijos istorija

## Nuorodos

 * [NSF formatas – Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

