{
  "date": "2019-12-12",
  "keywords": [
"LRF",
"failą",
"pratęsimas",
"formatu",
"eBook",
"Skaitmeninė knyga"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie LRF failo formatą ir API, kurios gali kurti ir atidaryti LRF failus.",
  "title": "LRF failo formatas – „Sony“ nešiojamojo skaitytuvo failas",
  "linktitle": "LRF",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-lr-ltf"
}
},
  "lastmod": "2019-12-12"
}

## Kas yra LRF failas?

Failas su plėtiniu .lrf yra plačiajuosčio el. knygos (BBeB) failas, kuriame yra Sony BBeB duomenų, įskaitant tekstą, vaizdus ir puslapių numeravimo duomenis. Failas išsaugomas suspaustu dvejetainiu formatu, kuriame yra antraštė, nurodytas objektų skaičius ir objekto indeksas. LRF ir LRX failai apima du galimus BBeB knygų formatus. LRF failai nėra užšifruoti ir gali būti sudaryti iš [LRX](/ebook/lrf/) failų. LRF failus galima konvertuoti iš kelių kitų failų tipų, įskaitant PDF ir HTML. Jei jūsų kompiuteris negali atidaryti LRF failo, greičiausiai nesate įdiegę programinės įrangos, kad galėtumėte atidaryti ar redaguoti LRF failus. Programos, kuriomis galima atidaryti LRF failus, yra Caliber, BookDesigner, Makelrf ir Canon Book Creator, skirta Windows, Caliber, skirta Linux, Caliber ir Sony Reader, skirta Macintosh.

## Trumpa istorija

LRF failo tipas visų pirma yra susietas su Line Rider, kurį sukūrė [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider yra internetinis fizinis žaislas, kurį 2006 m. rugsėjį išrado Slovėnijos universiteto studentas Boštjanas Čadežas. Sony prekės ženklo el. knygų skaitytuvai (pvz., Sony PRS-500 skaitytuvai ir Sony Librie) savo dokumentams ir tekstams naudoja LRF failo plėtinį. Šis patentuotas failo tipas, kaip ir susiję LRS ir LRX failai, dabar yra pasenęs. Šie trys failų tipai sudarė BroadBand eBook (BBeB), kuris buvo nutrauktas 2010 m., kai Sony pradėjo pardavinėti savo elektronines knygas EPUB formatu.

## LRF failo formatas

Išsamias LRF failo formato specifikacijas rasite adresu [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). LRF failą sudaro:
* antraštė

* daug objektų

* objekto indeksas.


Visos šios reikšmės yra Intel (pirmiausia LSB) tvarka.

### LRF antraštė

|Poslinkis (šešioliktainis) |Dydis (baitai) |Vardas/prasmė| Pavyzdinė reikšmė|
---|---|---|---|
|0 |8| LRF parašas| 4C 00 52 00 46 00 00 00 = LRF Unicode|
|8 |2| versija?| 999 daugumoje failų|
|A |2| Psuedo-Encryption |rakto baitas 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| Objektų skaičius |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| nežinomas| 0|
|24 |1| Vėliavos| (16 - iš nugaros į priekį, 1 = iš priekio į galą) 16|
|25 |1| nežinomas |(pamušalas?) 0|
|26 |2| nežinomas| 1600|
|28 |2| nežinomas| (pamušalas?) 0|
|2A |2| Ūgis?| 600|
|2C |2| Plotis?| 800|
|2E |1| nežinomas| 24|
|2F |1| nežinomas |(pamušalas?) 0|
|30 |0x14| nežinomas| nuliai|
|44 |4| Tik PlaneStream (0x1E) objekto ID| 0x0042|
|48 |4| nežinomas |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Nuorodos

* [LRF failo formatas](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)

* [BBeB – Vikipedija](https://en.wikipedia.org/wiki/BBeB)


