{
  "date": "2021-09-08",
  "keywords": [
"mgx failą",
"mgx failo formatas",
"kas yra mgx failas",
"failą",
"mgx pavyzdys",
"mgx failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie Age of Empires 2 Expansion Replay MGX failo formatą ir API, kurios gali kurti ir atidaryti MGX failus.",
  "title": "MGX – „Age of Empires 2“ išplėtimo pakartojimas",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mg-ltx"
}
},
  "lastmod": "2021-09-08"
}

## Kas yra MGX failas?

Failas su plėtiniu .mgx yra įrašytas žaidimo Age of Empires II: The Conquerors failas, kurį galima pakartoti naudojant Age of Empires II programą. Jame yra visas vartotojo vykdomos kampanijos įrašas. Jį galima įkelti ir atkurti programoje Age of Empires II. Pakartojus žaidimą, rodomi visi įvykiai ir scenarijai, kuriuos vartotojas suplanavo kampanijai ir žaidė.

## MGX failo formatas – daugiau informacijos

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### Struktūros apibrėžimai

Manoma, kad GPX failo formato struktūros apibrėžimai yra pagrįsti [BinData Ruby Gem declarations](https://github.com/dmendel/bindata/wiki), kuris suteikia galimybę skaityti ir rašyti struktūrinius dvejetainius duomenis. Tai leidžia programuotojui nurodyti dvejetainių duomenų formatą, kurį vėliau nuskaito ir įrašo BinData.

### MGX Messaging

MGX pranešimų siuntimas yra pagrįstas dviejų tipų pranešimais.

 * GAMESTART – nurodo žaidimo pradžios komandas ir nėra patvirtinta iki šiol
 * CHAT – aprašo žaidimo pokalbių pranešimus. Tiek žaidėjai, tiek pats žaidimas (Gaia) gali siųsti žaidimo pranešimus.

### ŽAIDIMO VEIKSMAI

Yra keletas [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions), kurie buvo gauti ir kurių išsami informacija yra prieinama.

## Nuorodos

* [Age of Empires 2: The Conquerors – Savegame failo formato specifikacija](https://github.com/stefan-kolb/aoc-mgx-format)


