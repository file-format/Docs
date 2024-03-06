{
  "date": "2021-07-20",
  "keywords": [
"MJS",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"Node.js ES moduļa fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MJS — Node.js ES moduļa Javascript fails",
  "description": "Uzziniet, kas ir MJS fails un API, kas var izveidot un atvērt MJS failu.",
  "linktitle": "MJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mj-lvs"
}
},
  "lastmod": "2021-07-20"
}

## Kas ir MJS fails?

A file with .mjs extension is a JavaScript source code file that is used as an ECMA Module (ECMAScript Module) in Node.js applications. Node.js's natvie module system is CommonJS that is used to split the code in different files to keep the [JS](/web/js/) code organized. MJS is the only way used by Node.js to identify if the module is a CommonJS or an ES6. ECMAScript moduļi ir standarta formāta JavaScript koda iesaiņošanai atkārtotai izmantošanai. MJS failus var atvērt tādos teksta redaktoros kā Atom, Vim, Apple xCode, Microsoft Visual Studio un Notepad.

## MJS faila formāts — vairāk informācijas

MJS faili tiek saglabāti diskā kā vienkārša teksta formātā JavaScript sintaksē. Tos var atvērt jebkurā teksta redaktorā, un tie ir lasāmi cilvēkiem. Kopš 2018. gada gandrīz visas lielākās pārlūkprogrammas tagad atbalsta ES moduļus.

## Atšķirības starp ES moduļiem un CommonJS

Tātad, ar ko MJS faili atšķiras no parastajiem JS failiem? Atšķirību starp ES moduļiem un CommonJS var apkopot šādi:

 * Nav nepieciešams, eksports vai module.exports
 * Nav \__faila nosaukuma vai \__dirname
 * Nav JSON moduļa ielādes
 * Nav vietējā moduļa ielādes
 * Nav nepieciešams.atrisināt
 * Nav NODE_PATH
 * Nav nepieciešams.paplašinājumi
 * Nav prasību.kešatmiņa

## Atsauces

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Difference Between JS And MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

