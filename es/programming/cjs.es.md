{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS-fail – CommonJS-koodifail",
  "description":"Mis on .cjs-fail ja kuidas seda avada?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Mis on CJS-fail?

CommonJS-fail (CJS) on fail, mis sisaldab CommonJS-i süntaksis kirjutatud JavaScripti koodi. CommonJS on moodulsüsteem, mis on loodud töötama keskkondades väljaspool esiserva veebibrausereid ja seda kasutatakse sageli serveripoolsetes JavaScripti keskkondades, nagu Node.js.

## CJS-failivorming – rohkem teavet

CJS-failid on kirjutatud CommonJS-i süntaksis ja neid saab redigeerida mis tahes tekstiredaktoris, nagu Microsoft Notepad või Apple TextEdit. CommonJS-i mooduleid hoitakse tavaliselt eraldi failides ja need on ette nähtud koodi kapseldamiseks ja moduleerimiseks, et tagada parem korraldamine ja hooldatavus. Need moodulid kasutavad sõltuvuste importimiseks funktsiooni Nõua ja objekti module.exports või exports, et paljastada väärtused ja funktsioonid, mida saavad kasutada koodi muud osad.

## CJS-koodi näide

CommonJS-i moodulitel on spetsiifiline süntaks ja struktuur, mis sisaldab selliseid funktsioone nagu nõutav funktsioon teiste moodulite importimiseks ja module.ekspordib või ekspordib objekte väärtuste, funktsioonide või objektide eksportimiseks moodulist. Neid mooduleid kasutatakse koodiosade kapseldamiseks ja eraldamiseks, mis muudab suurte JavaScripti koodibaaside haldamise ja hooldamise lihtsamaks. Siin on CommonJS-i mooduli põhinäide:


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

## Viited

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)