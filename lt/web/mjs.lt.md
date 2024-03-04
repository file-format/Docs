{
  "date": "2021-07-20",
  "keywords": [
"MJS",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"Node.js ES modulio failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MJS – Node.js ES modulio Javascript failas",
  "description": "Sužinokite, kas yra MJS failas ir API, kurios gali sukurti ir atidaryti MJS failą.",
  "linktitle": "MJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mj-lts"
}
},
  "lastmod": "2021-07-20"
}

## Kas yra MJS failas?

A file with .mjs extension is a JavaScript source code file that is used as an ECMA Module (ECMAScript Module) in Node.js applications. Node.js's natvie module system is CommonJS that is used to split the code in different files to keep the [JS](/web/js/) code organized. MJS is the only way used by Node.js to identify if the module is a CommonJS or an ES6. ECMAScript moduliai yra standartinė forma, skirta pakuoti JavaScript kodą pakartotiniam naudojimui. MJS failus galima atidaryti naudojant teksto redaktorius, tokius kaip Atom, Vim, Apple xCode, Microsoft Visual Studio ir Notepad.

## MJS failo formatas – daugiau informacijos

MJS failai išsaugomi diske paprasto teksto formatu JavaScript sintaksėje. Juos galima atidaryti bet kuriame teksto rengyklėje ir juos skaityti galima. Nuo 2018 m. beveik visos pagrindinės naršyklės dabar palaiko ES modulius.

## ES modulių ir CommonJS skirtumai

Taigi, kuo MJS failai skiriasi nuo paprastų JS failų? ES modulių ir CommonJS skirtumą galima apibendrinti taip:

 * Nereikia, eksportas arba modulis.eksportas
 * Nėra \__failo pavadinimo arba \__dirname
 * Neįkeliamas JSON modulis
 * Nėra vietinio modulio įkėlimo
 * Nereikia.išspręsti
 * Nėra NODE_PATH
 * Nereikia.plėtiniai
 * Nereikia.cache

## Nuorodos

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Difference Between JS And MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

