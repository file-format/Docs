{
  "date": "2021-09-08",
  "keywords": [
"mgx fails",
"mgx faila formātā",
"kas ir mgx fails",
"failu",
"mgx piemērs",
"mgx faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par Age of Empires 2 Expansion Replay MGX faila formātu un API, kas var izveidot un atvērt MGX failus.",
  "title": "MGX — Age of Empires 2 paplašināšanas atkārtojums",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mg-lvx"
}
},
  "lastmod": "2021-09-08"
}

## Kas ir MGX fails?

Fails ar paplašinājumu .mgx ir ierakstīts fails spēlei Age of Empires II: The Conquerors, ko var atkārtoti atskaņot programmā Age of Empires II. Tas satur pilnīgu lietotāja atskaņotās kampaņas ierakstu. To var ielādēt un atskaņot programmā Age of Empires II. Pēc atkārtotas atskaņošanas spēle parāda visus notikumus un scenārijus, ko lietotājs plānoja kampaņai un spēlēja.

## MGX faila formāts — vairāk informācijas

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### Struktūras definīcijas

Tiek uzskatīts, ka GPX faila formāta struktūras definīcijas ir balstītas uz [BinData Ruby Gem declarations](https://github.com/dmendel/bindata/wiki), kas nodrošina veidu, kā lasīt un rakstīt strukturētus bināros datus. Tas ļauj programmētājam norādīt bināro datu formātu, ko pēc tam nolasa un raksta BinData.

### MGX ziņojumapmaiņa

MGX ziņojumapmaiņas pamatā ir divu veidu ziņojumi.

 * GAMESTART — norāda spēles sākuma komandas un līdz šim nav apstiprināta
 * CHAT — apraksta spēles tērzēšanas ziņojumus. Gan spēlētāji, gan pati spēle (Gaia) var raidīt spēles ziņojumus.

### SPĒLES DARBĪBAS

Ir izgūti vairāki [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions), kuru informācija ir pieejama.

## Atsauces

* [Age of Empires 2: The Conquerors — Savegame faila formāta specifikācija](https://github.com/stefan-kolb/aoc-mgx-format)


