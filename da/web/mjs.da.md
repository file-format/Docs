{
  "date": "2021-07-20",
  "keywords": [
"MJS",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"Node.js ES-modulfil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MJS - Node.js ES Module Javascript-fil",
  "description": "Lær om, hvad en MJS-fil og API'er er, der kan oprette og åbne MJS-fil.",
  "linktitle": "MJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mj-das"
}
},
  "lastmod": "2021-07-20"
}

## Hvad er en MJS fil?

A file with .mjs extension is a JavaScript source code file that is used as an ECMA Module (ECMAScript Module) in Node.js applications. Node.js's natvie module system is CommonJS that is used to split the code in different files to keep the [JS](/web/js/) code organized. MJS is the only way used by Node.js to identify if the module is a CommonJS or an ES6. ECMAScript-moduler er standardformater til emballering af JavaScript-kode til genbrug. MJS-filer kan åbnes i teksteditorer som Atom, Vim, Apple xCode, Microsoft Visual Studio og Notepad.

## MJS-filformat - flere oplysninger

MJS-filer gemmes på disken som almindeligt tekstformat i JavaScript-syntaks. Disse kan åbnes i en hvilken som helst teksteditor og kan læses af mennesker. Siden 2018 understøtter næsten alle større browsere nu ES-moduler.

## Forskelle mellem ES-moduler og CommonJS

Så hvad gør MJS-filer anderledes end almindelige JS-filer? Forskellen mellem ES-moduler og CommonJS kan opsummeres som følger:

 * Ingen krav, eksport eller modul.eksport
 * Intet \__filnavn eller \__dirnavn
 * Intet JSON-modul indlæses
 * Ingen indbygget modul indlæsning
 * Ingen kræve.opløsning
 * Ingen NODE_PATH
 * Ingen kræve.udvidelser
 * Ingen kræve.cache

## Referencer

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Difference Between JS And MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

