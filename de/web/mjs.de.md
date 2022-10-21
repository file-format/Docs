{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "Node.js ES-Moduldatei"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - JavaScript-Datei des Node.js ES-Moduls",
  "description" :"Erfahren Sie, was eine MJS-Datei und APIs sind, die eine MJS-Datei erstellen und öffnen können.",
  "linktitle" :"MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Was ist eine MJS-Datei?

Eine Datei mit der Erweiterung .mjs ist eine JavaScript-Quellcodedatei, die als ECMA-Modul (ECMAScript-Modul) in Node.js-Anwendungen verwendet wird. Das Natvie-Modulsystem von Node.js ist CommonJS, das verwendet wird, um den Code in verschiedene Dateien aufzuteilen, um den [JS](/de/web/js/)-Code organisiert zu halten. MJS ist die einzige Möglichkeit, die von Node.js verwendet wird, um festzustellen, ob das Modul ein CommonJS oder ein ES6 ist. ECMAScript-Module sind Standardformate zum Packen von JavaScript-Code zur Wiederverwendung. MJS-Dateien können in Texteditoren wie Atom, Vim, Apple xCode, Microsoft Visual Studio und Notepad geöffnet werden.

## MJS-Dateiformat – Weitere Informationen

MJS-Dateien werden im Nur-Text-Format in JavaScript-Syntax auf der Disc gespeichert. Diese können in jedem Texteditor geöffnet werden und sind für Menschen lesbar. Seit 2018 unterstützen nun fast alle gängigen Browser ES-Module.

## Unterschiede zwischen ES-Modulen und CommonJS

Was unterscheidet also MJS-Dateien von einfachen JS-Dateien? Der Unterschied zwischen ES Modules und CommonJS lässt sich wie folgt zusammenfassen:

* Keine Exporte oder module.exports erforderlich
* Kein \__Dateiname oder \__Verzeichnisname
* Kein Laden des JSON-Moduls
* Kein Laden des nativen Moduls
* Keine require.resolve
* Kein NODE_PATH
* Keine erforderlichen Erweiterungen
* Kein require.cache

## Verweise

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Unterschied zwischen JS und MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

