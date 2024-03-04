{
  "date": "2021-09-08",
  "keywords": [
"pcc failą",
"pcc failo formatas",
"kas yra pcc failas",
"failą",
"pcc pavyzdys",
"pcc failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie Mass Effect PCC failo formatą ir API, kurios gali kurti ir atidaryti PCC failus.",
  "title": "PCC – Mass Effect paketo failas",
  "linktitle": "PCC",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-pc-ltc"
}
},
  "lastmod": "2021-09-08"
}

## Kas yra PCC failas?

Failas su .pcc yra [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) failas, kuriame yra žaidimo duomenų, skirtų žaidimo turiniui, pvz., modeliams, tekstūroms ir patalpoms, keisti. Mass Effect 2 ir 3 yra pirmieji šaudyklės žaidimai, pagrįsti Unreal Engine 3 žaidimų varikliu. Iš pradžių žaidimą sukūrė [Bioware](https://www.bioware.com/about/), kuris didžiąją dalį žaidimo išteklių laikė savo patentuotu PCC failo formatu. Bioware įsigijo Electronic Arts, pirmaujanti pasaulinė interaktyvių pramogų leidėja.

## PCC failo formatas – daugiau informacijos

PCC failuose yra suspaustų ir (arba) nesuspaustų struktūrų, kurios prisideda prie bendro failų organizavimo.

### Suspausta PCC struktūra

Suglaudintas PCC failas susideda iš lentelių ir duomenų, suskirstytų į dalis. Kiekviename gabale yra kintamas suspaustų blokų skaičius.

 * Chunks Header – 16 baitų bendra antraštė, kurioje yra informacijos apie gabalus.
 * Chunk Header – 16 baitų antraštė, kurioje yra informacija apie neapdorotus suglaudintus duomenis, esančius bloko formoje.

### Nesuspausta PCC struktūra

Nesuspausti PCC failai yra suskirstyti į šias penkias dalis.

 * Antraštė – yra pagrindinė informacija apie PCC failo struktūrą.
 * Vardų lentelė – yra pavadinimas, rastas pakete, įskaitant importo klases, eksporto ir eksportavimo ypatybes.
 * Importavimo lentelė – yra visos klasės ir objektai, importuoti PCC.
 * Eksportuoti lentelę – yra visi pakete saugomi objektai. Kiekvienas eksportuojamas dydis gali skirtis.

## Nuorodos

 * [Me3Explorer – PCC failo formatas](https://me3explorer.fandom.com/wiki/PCC_File_Format)
 * [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)
 * [Bioware](https://www.bioware.com/about/)

