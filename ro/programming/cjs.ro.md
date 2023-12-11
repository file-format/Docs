{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier CJS - Fișier cod CommonJS",
  "description":"Ce este un fișier .cjs și cum se deschide?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Ce este un fișier CJS?

Un fișier CommonJS (CJS) este un fișier care conține cod JavaScript scris în sintaxa CommonJS. CommonJS este un sistem de module conceput să funcționeze în medii dincolo de browserele web frontend și este adesea folosit în mediile JavaScript de pe partea de server, cum ar fi Node.js.

## Format fișier CJS - Mai multe informații

Fișierele CJS sunt scrise în sintaxa CommonJS și pot fi editate în orice editor de text, cum ar fi Microsoft Notepad sau Apple TextEdit. Modulele CommonJS sunt de obicei stocate în fișiere separate și sunt destinate să încapsuleze și să modulareze codul pentru o mai bună organizare și mentenanță. Aceste module folosesc funcția necesară pentru a importa dependențe și obiectul module.exports sau exports pentru a expune valori și funcții care pot fi utilizate de alte părți ale codului.

## Exemplu de cod CJS

Modulele CommonJS au o sintaxă și o structură specifice care include caracteristici precum funcția necesară pentru importarea altor module și module.exports sau exporta obiecte pentru exportul de valori, funcții sau obiecte dintr-un modul. Aceste module sunt utilizate pentru încapsularea și separarea bucăților de cod, facilitând gestionarea și întreținerea bazelor de cod JavaScript mari. Iată un exemplu de bază al unui modul CommonJS:

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

## Referințe

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
