{
  "date": "2021-09-08",
  "keywords": [
"mgx fil",
"mgx filformat",
"hvad er en mgx-fil",
"fil",
"mgx eksempel",
"mgx filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om Age of Empires 2 Expansion Replay MGX-filformat og API'er, der kan oprette og åbne MGX-filer.",
  "title": "MGX - Age of Empires 2 Expansion Replay",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mg-dax"
}
},
  "lastmod": "2021-09-08"
}

## Hvad er en MGX fil?

En fil med filtypenavnet .mgx er en optaget fil til Age of Empires II: The Conquerors-spillet, der kan afspilles igen i programmet Age of Empires II. Den indeholder komplet optagelse af den kampagne, som brugeren har spillet. Den kan indlæses og afspilles i programmet Age of Empires II. Når spillet er afspillet igen, viser det alle de begivenheder og scenarier, som brugeren planlagde for kampagnen og spillede.

## MGX-filformat - flere oplysninger

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### Strukturdefinitioner

Strukturdefinitionerne af GPX-filformatet menes at være baseret på [BinData Ruby Gem declarations](https://github.com/dmendel/bindata/wiki), der giver en måde at læse og skrive strukturerede binære data på. Dette lader programmøren specificere formatet for de binære data, som derefter læses og skrives af BinData.

### MGX Messaging

MGX-meddelelser er baseret på to typer meddelelser.

 * GAMESTART - specificerer spillets startkommandoer og er ikke valideret til dato
 * CHAT - beskriver chatbeskederne i spillet. Både spillere og selve spillet (Gaia) kan udsende beskeder i spillet.

### GAMEPLAY-HANDLINGER

Der er flere [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions), der er blevet hentet, og hvis detaljer er tilgængelige.

## Referencer

* [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format)


