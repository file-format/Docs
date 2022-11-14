{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "Fichier de module Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Fichier Javascript du module Node.js ES",
  "description" :"Découvrez ce qu'est un fichier MJS et les API qui peuvent créer et ouvrir un fichier MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Qu'est-ce qu'un fichier MJS ?

Un fichier avec l'extension .mjs est un fichier de code source JavaScript utilisé comme module ECMA (module ECMAScript) dans les applications Node.js. Le système de module natvie de Node.js est CommonJS qui est utilisé pour diviser le code en différents fichiers afin de garder le code [JS](/fr/web/js/) organisé. MJS est le seul moyen utilisé par Node.js pour identifier si le module est un CommonJS ou un ES6. Les modules ECMAScript sont des formulaires standard pour empaqueter le code JavaScript en vue de sa réutilisation. Les fichiers MJS peuvent être ouverts dans des éditeurs de texte tels que Atom, Vim, Apple xCode, Microsoft Visual Studio et Notepad.

## Format de fichier MJS - Plus d'informations

Les fichiers MJS sont enregistrés sur le disque au format texte brut dans la syntaxe JavaScript. Ceux-ci peuvent être ouverts dans n'importe quel éditeur de texte et sont lisibles par l'homme. Depuis 2018, presque tous les principaux navigateurs prennent désormais en charge les modules ES.

## Différences entre les modules ES et CommonJS

Alors, qu'est-ce qui différencie les fichiers MJS des fichiers JS simples ? La différence entre les modules ES et CommonJS peut être résumée comme suit :

* Aucune exigence, exportation ou module.exports
* Pas de \__filename ou \__dirname
* Pas de chargement de module JSON
* Pas de chargement de module natif
* Aucune résolution requise
* Pas de NODE_PATH
* Aucune extension requise
* Pas de cache requis

## Références

* [ESM Node.js](https://nodejs.org/docs/latest/api/esm.html)
* [Différence entre JS et MJS] (https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

