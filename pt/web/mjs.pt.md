{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "Arquivo de módulo Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - arquivo Javascript do módulo Node.js ES",
  "description" :"Saiba mais sobre o que é um arquivo MJS e APIs que podem criar e abrir um arquivo MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## O que é um arquivo MJS?

Um arquivo com extensão .mjs é um arquivo de código-fonte JavaScript que é usado como um Módulo ECMA (Módulo ECMAScript) em aplicativos Node.js. O sistema de módulos natvie do Node.js é o CommonJS que é usado para dividir o código em diferentes arquivos para manter o código [JS](/pt/web/js/) organizado. MJS é a única maneira usada pelo Node.js para identificar se o módulo é um CommonJS ou um ES6. Os módulos ECMAScript são formatos padrão para empacotar código JavaScript para reutilização. Os arquivos MJS podem ser abertos em editores de texto como Atom, Vim, Apple xCode, Microsoft Visual Studio e Notepad.

## Formato de arquivo MJS - Mais informações

Os arquivos MJS são salvos em disco como formato de texto simples na sintaxe JavaScript. Estes podem ser abertos em qualquer editor de texto e são legíveis por humanos. Desde 2018, quase todos os principais navegadores agora suportam módulos ES.

## Diferenças entre módulos ES e CommonJS

Então, o que torna os arquivos MJS diferentes dos arquivos JS simples? A diferença entre Módulos ES e CommonJS pode ser resumida da seguinte forma:

* Não requer, exporta ou module.exports
* Sem \__filename ou \__dirname
* Sem carregamento do módulo JSON
* Sem carregamento de módulo nativo
* Não requer.resolver
* Não NODE_PATH
* Não requer.extensões
* Não requer.cache

## Referências

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Diferença entre JS e MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

