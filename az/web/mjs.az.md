{
  "date": "2021-07-20",
  "keywords": [
"MJS",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"Node.js ES Modul Faylı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MJS - Node.js ES Modulu Javascript Faylı",
  "description": "MJS faylının nə olduğunu və MJS faylını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "MJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mj-azs"
}
},
  "lastmod": "2021-07-20"
}

## MJS faylı nədir?

A file with .mjs extension is a JavaScript source code file that is used as an ECMA Module (ECMAScript Module) in Node.js applications. Node.js's natvie module system is CommonJS that is used to split the code in different files to keep the [JS](/web/js/) code organized. MJS is the only way used by Node.js to identify if the module is a CommonJS or an ES6. ECMAScript modulları təkrar istifadə üçün JavaScript kodunun qablaşdırılması üçün standart formalardır. MJS faylları Atom, Vim, Apple xCode, Microsoft Visual Studio və Notepad kimi mətn redaktorlarında açıla bilər.

## MJS Fayl Format - Ətraflı Məlumat

MJS faylları JavaScript sintaksisində düz mətn formatı kimi diskdə saxlanılır. Bunlar istənilən mətn redaktorunda açıla bilər və insanlar tərəfindən oxuna bilər. 2018-ci ildən, demək olar ki, bütün əsas brauzerlər indi ES modullarını dəstəkləyir.

## ES modulları ilə CommonJS arasındakı fərqlər

Beləliklə, MJS fayllarını adi JS fayllarından fərqləndirən nədir? ES Modulları ilə CommonJS arasındakı fərqi aşağıdakı kimi ümumiləşdirmək olar:

 * Tələb yoxdur, ixrac və ya module.exports
 * \__fayl adı və ya \__dirname yoxdur
 * JSON Modulu Yüklənmir
 * Doğma Modul Yüklənmir
 * Tələb yoxdur.həll et
 * NODE_PATH yoxdur
 * Tələb yoxdur. uzantılar
 * Tələb yoxdur.cache

## İstinadlar

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Difference Between JS And MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

