{
  "date": "2021-07-20",
  "keywords": [
"MJS",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"Node.js ES-moduulitiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MJS - Node.js ES-moduulin Javascript-tiedosto",
  "description": "Opi, mikä on MJS-tiedosto ja API:t, jotka voivat luoda ja avata MJS-tiedoston.",
  "linktitle": "MJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mj-fis"
}
},
  "lastmod": "2021-07-20"
}

## Mikä on MJS-tiedosto?

A file with .mjs extension is a JavaScript source code file that is used as an ECMA Module (ECMAScript Module) in Node.js applications. Node.js's natvie module system is CommonJS that is used to split the code in different files to keep the [JS](/web/js/) code organized. MJS is the only way used by Node.js to identify if the module is a CommonJS or an ES6. ECMAScript-moduulit ovat vakiomuotoisia JavaScript-koodin pakkaamiseen uudelleenkäyttöä varten. MJS-tiedostoja voidaan avata tekstieditoreilla, kuten Atom, Vim, Apple xCode, Microsoft Visual Studio ja Notepad.

## MJS-tiedostomuoto - lisätietoja

MJS-tiedostot tallennetaan levylle vain tekstimuodossa JavaScript-syntaksissa. Ne voidaan avata missä tahansa tekstieditorissa ja ne ovat ihmisen luettavissa. Vuodesta 2018 lähtien lähes kaikki suurimmat selaimet tukevat nyt ES-moduuleja.

## Erot ES-moduulien ja CommonJS:n välillä

Joten mikä tekee MJS-tiedostoista erilaisia kuin tavallisia JS-tiedostoja? ES-moduulien ja CommonJS:n välinen ero voidaan tiivistää seuraavasti:

 * Ei vaadi, vienti tai module.exports
 * Ei \__tiedoston nimeä tai \__hakemistoa
 * Ei JSON-moduulin latausta
 * Ei alkuperäistä moduulin latausta
 * Ei vaadi.resolve
 * Ei NODE_PATH
 * Ei vaadi.laajennuksia
 * Ei vaadi.välimuistia

## Viitteet

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Difference Between JS And MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

