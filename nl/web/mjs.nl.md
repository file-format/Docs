{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Bestand", "Extensie", "Bestandsindeling", "Bestandsextensie", "Node.js ES-modulebestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES Module Javascript-bestand",
  "description" :"Meer informatie over wat een MJS-bestand is en API's die een MJS-bestand kunnen maken en openen.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Wat is een MJS-bestand?

Een bestand met de extensie .mjs is een JavaScript-broncodebestand dat wordt gebruikt als een ECMA-module (ECMAScript-module) in Node.js-toepassingen. Het natvie-modulesysteem van Node.js is CommonJS dat wordt gebruikt om de code in verschillende bestanden te splitsen om de [JS](/nl/web/js/)-code georganiseerd te houden. MJS is de enige manier die door Node.js wordt gebruikt om te bepalen of de module een CommonJS of een ES6 is. ECMAScript-modules zijn standaardformaten voor het verpakken van JavaScript-code voor hergebruik. MJS-bestanden kunnen worden geopend in teksteditors zoals Atom, Vim, Apple xCode, Microsoft Visual Studio en Notepad.

## MJS-bestandsindeling - Meer informatie

MJS-bestanden worden op schijf opgeslagen als tekst zonder opmaak in JavaScript-syntaxis. Deze kunnen in elke teksteditor worden geopend en zijn leesbaar voor mensen. Sinds 2018 ondersteunen bijna alle grote browsers nu ES-modules.

## Verschillen tussen ES-modules en CommonJS

Dus wat maakt MJS-bestanden anders dan gewone JS-bestanden? Het verschil tussen ES-modules en CommonJS kan als volgt worden samengevat:

* Geen vereist, export of module.exports
* Geen \__bestandsnaam of \__dirnaam
* Geen JSON-module wordt geladen
* Geen native module laden
* Geen vereiste.resolve
* Geen NODE_PATH
* Geen extensies nodig
* Geen cache nodig

## Referenties

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Verschil tussen JS en MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

