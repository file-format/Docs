{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "Soubor modulu Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES Module Javascript File",
  "description" :"Zjistěte, co je soubor MJS a rozhraní API, která mohou vytvořit a otevřít soubor MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Co je soubor MJS?

Soubor s příponou .mjs je soubor zdrojového kódu JavaScript, který se používá jako modul ECMA (modul ECMAScript) v aplikacích Node.js. Modulový systém natvie Node.js je CommonJS, který se používá k rozdělení kódu do různých souborů, aby byl kód [JS](/cs/web/js/) uspořádaný. MJS je jediný způsob, který Node.js používá k identifikaci, zda je modul CommonJS nebo ES6. Moduly ECMAScript jsou standardním formátem pro balení kódu JavaScript pro opětovné použití. Soubory MJS lze otevřít v textových editorech, jako je Atom, Vim, Apple xCode, Microsoft Visual Studio a Notepad.

## Formát souboru MJS – Další informace

Soubory MJS se ukládají na disk jako prostý textový formát v syntaxi JavaScriptu. Ty lze otevřít v libovolném textovém editoru a jsou čitelné pro člověka. Od roku 2018 nyní téměř všechny hlavní prohlížeče podporují moduly ES.

## Rozdíly mezi moduly ES a CommonJS

V čem se tedy soubory MJS liší od obyčejných souborů JS? Rozdíl mezi moduly ES a CommonJS lze shrnout takto:

* Žádné požadavky, exporty nebo module.exports
* Žádné \__filename nebo \__dirname
* Žádné načítání modulu JSON
* Žádné načítání nativního modulu
* Není vyžadováno. vyřešit
* Žádná NODE_PATH
* Nejsou vyžadována žádná rozšíření
* Není vyžadována mezipaměť

## Reference

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Rozdíl mezi JS a MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

