{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "Archivo de módulo ES de Node.js"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Archivo Javascript del módulo ES de Node.js",
  "description" :"Obtenga información sobre qué es un archivo MJS y las API que pueden crear y abrir un archivo MJS",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## ¿Qué es un archivo MJS?

Un archivo con la extensión .mjs es un archivo de código fuente de JavaScript que se utiliza como módulo ECMA (módulo ECMAScript) en aplicaciones Node.js. El sistema de módulos naturales de Node.js es CommonJS, que se usa para dividir el código en diferentes archivos para mantener el código [JS](/es/web/js/) organizado. MJS es la única forma que utiliza Node.js para identificar si el módulo es CommonJS o ES6. Los módulos ECMAScript son formatos estándar para empaquetar código JavaScript para su reutilización. Los archivos MJS se pueden abrir en editores de texto como Atom, Vim, Apple xCode, Microsoft Visual Studio y Notepad.

## Formato de archivo MJS - Más información

Los archivos MJS se guardan en el disco como formato de texto sin formato en la sintaxis de JavaScript. Estos se pueden abrir en cualquier editor de texto y son legibles por humanos. Desde 2018, casi todos los principales navegadores ahora admiten módulos ES.

## Diferencias entre módulos ES y CommonJS

Entonces, ¿qué hace que los archivos MJS sean diferentes de los archivos JS simples? La diferencia entre ES Modules y CommonJS se puede resumir de la siguiente manera:

* No requiere, exportaciones o módulos.exportaciones
* No \__filename o \__dirname
* Sin carga de módulo JSON
* Sin carga de módulo nativo
* No require.resolver
* Sin NODE_PATH
* No requieren extensiones
* No require.cache

## Referencias

* [ESM de Node.js](https://nodejs.org/docs/latest/api/esm.html)
* [Diferencia entre JS y MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_ between_es_modules_and_commonjs)

