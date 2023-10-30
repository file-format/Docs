
{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS File - CommonJS Code File",
  "description":"Co je soubor .cjs a jak jej otevřít?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## Co je soubor CJS?

Soubor CommonJS (CJS) je soubor, který obsahuje kód JavaScript napsaný v syntaxi CommonJS. CommonJS je modulový systém navržený pro práci v prostředích mimo frontendové webové prohlížeče a často se používá v prostředích JavaScript na straně serveru, jako je Node.js.

## Formát souboru CJS – více informací

Soubory CJS jsou napsány v syntaxi CommonJS a lze je upravovat v libovolném textovém editoru, jako je Microsoft Notepad nebo Apple TextEdit. Moduly CommonJS jsou obvykle uloženy v samostatných souborech a jsou určeny k zapouzdření a modularizaci kódu pro lepší organizaci a údržbu. Tyto moduly používají funkci require k importu závislostí a objekt module.exports or exports k odhalení hodnot a funkcí, které mohou být použity jinými částmi kódu.

## Příklad kódu CJS

Moduly CommonJS mají specifickou syntaxi a strukturu, která zahrnuje funkce, jako je funkce require pro import jiných modulů a modul.exportuje nebo exportuje objekty pro export hodnot, funkcí nebo objektů z modulu. Tyto moduly se používají k zapouzdření a oddělení částí kódu, což usnadňuje správu a údržbu velkých kódových bází JavaScriptu. Zde je základní příklad modulu CommonJS:

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

## Reference

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)