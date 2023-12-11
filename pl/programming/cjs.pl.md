{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Plik CJS — plik kodu CommonJS",
  "description":"Co to jest plik .cjs i jak go otworzyć?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Co to jest plik CJS?

Plik CommonJS (CJS) to plik zawierający kod JavaScript napisany w składni CommonJS. CommonJS to system modułowy zaprojektowany do pracy w środowiskach innych niż frontendowe przeglądarki internetowe i często jest używany w środowiskach JavaScript po stronie serwera, takich jak Node.js.

## Format pliku CJS — więcej informacji

Pliki CJS są zapisywane w składni CommonJS i można je edytować w dowolnym edytorze tekstu, takim jak Microsoft Notatnik lub Apple TextEdit. Moduły CommonJS są zwykle przechowywane w oddzielnych plikach i mają na celu hermetyzację i modularyzację kodu w celu lepszej organizacji i łatwości konserwacji. Moduły te używają wymaganej funkcji do importowania zależności, a obiekt module.exports lub eksportuje do udostępniania wartości i funkcji, które mogą być używane w innych częściach kodu.

## Przykład kodu CJS

Moduły CommonJS mają specyficzną składnię i strukturę, która obejmuje takie funkcje, jak funkcja wymagana do importowania innych modułów oraz moduł.eksportuje lub eksportuje obiekty w celu eksportowania wartości, funkcji lub obiektów z modułu. Moduły te służą do hermetyzacji i oddzielania fragmentów kodu, co ułatwia zarządzanie i utrzymywanie dużych baz kodu JavaScript. Oto podstawowy przykład modułu CommonJS:

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

## Bibliografia

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
