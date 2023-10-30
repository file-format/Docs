{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS fájl - CommonJS kódfájl",
  "description":"Mi az a .cjs fájl, és hogyan lehet megnyitni?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## Mi az a CJS fájl?

A CommonJS (CJS) fájl olyan fájl, amely CommonJS szintaxisban írt JavaScript kódot tartalmaz. A CommonJS egy modulrendszer, amelyet a frontend webböngészőkön kívüli környezetekben való használatra terveztek, és gyakran használják szerveroldali JavaScript-környezetekben, például a Node.js-ben.

## CJS fájlformátum - További információk

A CJS fájlok CommonJS szintaxisban íródnak, és bármilyen szövegszerkesztőben szerkeszthetők, például a Microsoft Notepad vagy az Apple TextEdit segítségével. A CommonJS modulokat általában külön fájlokban tárolják, és célja a kód beágyazása és modularizálása a jobb rendszerezés és karbantarthatóság érdekében. Ezek a modulok a követelmény függvényt használják a függőségek importálásához, a module.exports vagy exports objektum pedig a kód más részei által használható értékek és függvények megjelenítéséhez.

## CJS kód példa

A CommonJS modulok sajátos szintaxissal és szerkezettel rendelkeznek, amely olyan funkciókat tartalmaz, mint például a követelmény függvény más modulok importálásához, illetve a module.exports vagy exports objektumokat értékek, függvények vagy objektumok modulból való exportálásához. Ezeket a modulokat kódrészletek beágyazására és elkülönítésére használják, megkönnyítve ezzel a nagy JavaScript-kódbázisok kezelését és karbantartását. Íme egy alapvető példa a CommonJS modulra:

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

## Referenciák

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
