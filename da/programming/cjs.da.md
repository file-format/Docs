{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CJS-fil - CommonJS-kodefil",
  "description": "Hvad er en .cjs-fil, og hvordan åbner man den?",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cj-das"
}
},
  "lastmod": "2023-10-26"
}

## Hvad er en CJS fil?

En CommonJS (CJS) fil er en fil, der indeholder JavaScript-kode skrevet i CommonJS syntaks. CommonJS er et modulsystem designet til at fungere i miljøer ud over frontend-webbrowsere, og det bruges ofte i JavaScript-miljøer på serversiden, såsom Node.js.

## CJS-filformat - flere oplysninger

CJS-filer er skrevet i CommonJS-syntaks og kan redigeres i en hvilken som helst teksteditor, såsom Microsoft Notepad eller Apple TextEdit. CommonJS-moduler gemmes typisk i separate filer og er beregnet til at indkapsle og modularisere kode for bedre organisering og vedligeholdelse. Disse moduler bruger kræve funktionen til at importere afhængigheder og module.exports eller exports objektet til at afsløre værdier og funktioner, der kan bruges af andre dele af koden.

### CJS-kodeeksempel

CommonJS-moduler har en specifik syntaks og struktur, der inkluderer funktioner såsom kræve funktionen til at importere andre moduler og modulet.eksporterer eller eksporterer objekter til eksport af værdier, funktioner eller objekter fra et modul. Disse moduler bruges til at indkapsle og adskille stykker kode, hvilket gør det nemmere at administrere og vedligeholde store JavaScript-kodebaser. Her er et grundlæggende eksempel på et CommonJS-modul:

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

## Referencer

* [Designkurser i Visual Studio](https://en.wikipedia.org/wiki/CommonJS)


