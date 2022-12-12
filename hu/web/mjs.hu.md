{
  "date" : "2021-07-20",
  "keywords" :["MJS", "File", "Extension", "File Format", "File Extension", "Node.js ES Module File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS – Node.js ES modul Javascript fájl",
  "description" :"Tudjon meg többet az MJS-fájlról és az API-król, amelyek MJS-fájlt hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Mi az MJS fájl?

Az .mjs kiterjesztésű fájl egy JavaScript-forráskódfájl, amelyet ECMA-modulként (ECMAScript-modul) használnak a Node.js-alkalmazásokban. A Node.js natvie modulrendszere a CommonJS, amely a kód különböző fájlokra való felosztására szolgál, hogy a [JS](/hu/web/js/) kódot rendezve tartsa. Az MJS az egyetlen módja annak, hogy a Node.js azonosítsa, hogy a modul CommonJS vagy ES6-e. Az ECMAScript modulok szabványos formátumúak az újrafelhasználásra szánt JavaScript kód csomagolására. Az MJS fájlok olyan szövegszerkesztőkkel nyithatók meg, mint az Atom, Vim, Apple xCode, Microsoft Visual Studio és Notepad.

## MJS fájlformátum - További információ

Az MJS-fájlokat a rendszer a lemezre menti egyszerű szöveges formátumban, JavaScript szintaxisban. Ezek bármelyik szövegszerkesztőben megnyithatók, és ember által is olvashatók. 2018 óta szinte minden nagyobb böngésző támogatja az ES modulokat.

## Az ES modulok és a CommonJS közötti különbségek

Tehát miben különböznek az MJS-fájlok az egyszerű JS-fájloktól? Az ES modulok és a CommonJS közötti különbség a következőképpen foglalható össze:

* Nincs szükség, export vagy module.exports
* Nincs \__fájlnév vagy \__könyvtárnév
* Nincs JSON-modul betöltése
* Nincs natív modul betöltése
* Nem szükséges.megoldani
* Nincs NODE_PATH
* Nincs szükség.kiterjesztésekre
* Nincs követelmény.gyorsítótár

## Hivatkozások

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Különbség a JS és az MJS között](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

