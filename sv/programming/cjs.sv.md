{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS-fil - CommonJS-kodfil",
  "description":"Vad är en .cjs-fil och hur öppnar man den?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Vad är en CJS-fil?

En CommonJS (CJS) fil är en fil som innehåller JavaScript-kod skriven i CommonJS syntax. CommonJS är ett modulsystem designat för att fungera i miljöer bortom frontend-webbläsare, och det används ofta i JavaScript-miljöer på serversidan, som Node.js.

## CJS-filformat - Mer information

CJS-filer är skrivna i CommonJS-syntax och kan redigeras i vilken textredigerare som helst som Microsoft Notepad eller Apple TextEdit. CommonJS-moduler lagras vanligtvis i separata filer och är avsedda att kapsla in och modularisera kod för bättre organisation och underhåll. Dessa moduler använder den nödvändiga funktionen för att importera beroenden och objektet module.exports eller exports för att exponera värden och funktioner som kan användas av andra delar av koden.

## CJS-kodexempel

CommonJS-moduler har en specifik syntax och struktur som inkluderar funktioner som den nödvändiga funktionen för att importera andra moduler och modulen.exporterar eller exporterar objekt för att exportera värden, funktioner eller objekt från en modul. Dessa moduler används för att kapsla in och separera kodbitar, vilket gör det lättare att hantera och underhålla stora JavaScript-kodbaser. Här är ett grundläggande exempel på en CommonJS-modul:

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

## Referenser

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
