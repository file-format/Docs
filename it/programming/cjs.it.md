{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "File CJS: file di codice CommonJS",
  "description":"Cos'è un file .cjs e come aprirlo?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## Cos'è un file CJS?

Un file CommonJS (CJS) è un file che contiene codice JavaScript scritto nella sintassi CommonJS. CommonJS è un sistema di moduli progettato per funzionare in ambienti diversi dai browser Web frontend ed è spesso utilizzato in ambienti JavaScript lato server, come Node.js.

## Formato file CJS - Ulteriori informazioni

I file CJS sono scritti nella sintassi CommonJS e possono essere modificati in qualsiasi editor di testo come Microsoft Notepad o Apple TextEdit. I moduli CommonJS sono generalmente archiviati in file separati e hanno lo scopo di incapsulare e modularizzare il codice per una migliore organizzazione e manutenibilità. Questi moduli utilizzano la funzione require per importare le dipendenze e l'oggetto module.exports o exports per esporre valori e funzioni che possono essere utilizzati da altre parti del codice.

## Esempio di codice CJS

I moduli CommonJS hanno una sintassi e una struttura specifiche che include funzionalità come la funzione require per importare altri moduli e module.exports o esporta oggetti per esportare valori, funzioni o oggetti da un modulo. Questi moduli vengono utilizzati per incapsulare e separare parti di codice, semplificando la gestione e il mantenimento di basi di codice JavaScript di grandi dimensioni. Ecco un esempio base di un modulo CommonJS:

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

## Riferimenti

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)