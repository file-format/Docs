{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "Fișier modul Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Fișier Javascript al modulului Node.js ES",
  "description" :"Aflați despre ce este un fișier MJS și API-urile care pot crea și deschide fișierul MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Ce este un fișier MJS?

Un fișier cu extensia .mjs este un fișier cod sursă JavaScript care este utilizat ca modul ECMA (modul ECMAScript) în aplicațiile Node.js. Sistemul de module natvie al Node.js este CommonJS care este folosit pentru a împărți codul în diferite fișiere pentru a menține organizat codul [JS](/ro/web/js/). MJS este singura modalitate folosită de Node.js pentru a identifica dacă modulul este un CommonJS sau un ES6. Modulele ECMAScript sunt forme standard pentru ambalarea codului JavaScript pentru reutilizare. Fișierele MJS pot fi deschise în editori de text precum Atom, Vim, Apple xCode, Microsoft Visual Studio și Notepad.

## Format de fișier MJS - Mai multe informații

Fișierele MJS sunt salvate pe disc ca format text simplu în sintaxa JavaScript. Acestea pot fi deschise în orice editor de text și pot fi citite de om. Din 2018, aproape toate browserele majore acceptă acum module ES.

## Diferențele dintre modulele ES și CommonJS

Deci, ce face fișierele MJS diferite de fișierele simple JS? Diferența dintre modulele ES și CommonJS poate fi rezumată după cum urmează:

* Nu necesită, exporturi sau module.exports
* Fără \__filename sau \__dirname
* Nu se încarcă modulul JSON
* Nu se încarcă modulul nativ
* Nu necesită.rezolvare
* Fără NODE_PATH
* Nu necesită.extensii
* Nu necesită.cache

## Referințe

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Diferența dintre JS și MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

