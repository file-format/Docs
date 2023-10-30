{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier CJS - Fichier de code CommonJS",
  "description":"Qu'est-ce qu'un fichier .cjs et comment l'ouvrir ?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## Qu'est-ce qu'un fichier CJS?

Un fichier CommonJS (CJS) est un fichier qui contient du code JavaScript écrit dans la syntaxe CommonJS. CommonJS est un système de modules conçu pour fonctionner dans des environnements autres que les navigateurs Web frontaux, et il est souvent utilisé dans des environnements JavaScript côté serveur, comme Node.js.

## Format de fichier CJS - Plus d'informations

Les fichiers CJS sont écrits dans la syntaxe CommonJS et peuvent être modifiés dans n'importe quel éditeur de texte tel que Microsoft Notepad ou Apple TextEdit. Les modules CommonJS sont généralement stockés dans des fichiers séparés et sont destinés à encapsuler et modulariser le code pour une meilleure organisation et maintenabilité. Ces modules utilisent la fonction require pour importer des dépendances et l'objet module.exports ou exports pour exposer des valeurs et des fonctions qui peuvent être utilisées par d'autres parties du code.

## Exemple de code CJS

Les modules CommonJS ont une syntaxe et une structure spécifiques qui incluent des fonctionnalités telles que la fonction require pour importer d'autres modules et les objets module.exports ou exports pour exporter des valeurs, des fonctions ou des objets à partir d'un module. Ces modules sont utilisés pour encapsuler et séparer des morceaux de code, facilitant ainsi la gestion et la maintenance de grandes bases de code JavaScript. Voici un exemple de base d’un module CommonJS:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## Les références

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)