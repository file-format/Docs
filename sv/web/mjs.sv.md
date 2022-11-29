{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Fil", "Tillägg", "Filformat", "Filtillägg", "Node.js ES Module File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES Module Javascript File",
  "description" :"Läs mer om vad en MJS-fil och API:er är som kan skapa och öppna MJS-fil.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Vad är en MJS fil?

En fil med filtillägget .mjs är en JavaScript-källkodsfil som används som en ECMA-modul (ECMAScript Module) i Node.js-applikationer. Node.jss natvie-modulsystem är CommonJS som används för att dela upp koden i olika filer för att hålla [JS](/sv/web/js/)-koden organiserad. MJS är det enda sättet som används av Node.js för att identifiera om modulen är en CommonJS eller en ES6. ECMAScript-moduler är standardformat för paketering av JavaScript-kod för återanvändning. MJS-filer kan öppnas i textredigerare som Atom, Vim, Apple xCode, Microsoft Visual Studio och Notepad.

## MJS-filformat - Mer information

MJS-filer sparas på skiva som vanligt textformat i JavaScript-syntax. Dessa kan öppnas i vilken textredigerare som helst och är läsbara för människor. Sedan 2018 har nästan alla större webbläsare nu stöd för ES-moduler.

## Skillnader mellan ES-moduler och CommonJS

Så vad gör MJS-filer annorlunda än vanliga JS-filer? Skillnaden mellan ES-moduler och CommonJS kan sammanfattas enligt följande:

* Inga krav, exporter eller module.exports
* Inget \__filnamn eller \__katalognamn
* Ingen JSON-modul laddas
* Ingen inbyggd modulladdning
* Inget require.resolve
* Ingen NODE_PATH
* Inga require.extensions
* Ingen require.cache

## Referenser

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Skillnaden mellan JS och MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

