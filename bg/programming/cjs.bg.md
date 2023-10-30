{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CJS файл - файл с CommonJS код",
  "description":"Какво е .cjs файл и как да го отворите?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2023-10-29"
}

## Какво е CJS файл?

Файлът CommonJS (CJS) е файл, който съдържа JavaScript код, написан в синтаксиса на CommonJS. CommonJS е модулна система, предназначена да работи в среди извън уеб браузърите на предния интерфейс и често се използва в среди на JavaScript от страна на сървъра, като Node.js.

## CJS файлов формат - повече информация

CJS файловете са написани в синтаксис CommonJS и могат да се редактират във всеки текстов редактор като Microsoft Notepad или Apple TextEdit. Модулите CommonJS обикновено се съхраняват в отделни файлове и са предназначени да капсулират и модулират кода за по-добра организация и поддръжка. Тези модули използват функцията require за импортиране на зависимости и обекта module.exports или exports за излагане на стойности и функции, които могат да се използват от други части на кода.

## Пример за CJS код

Модулите CommonJS имат специфичен синтаксис и структура, която включва функции като функцията за изискване за импортиране на други модули и module.exports или експортира обекти за експортиране на стойности, функции или обекти от модул. Тези модули се използват за капсулиране и отделяне на части от код, което улеснява управлението и поддържането на големи кодови бази на JavaScript. Ето основен пример за CommonJS модул:

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

## Препратки

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
