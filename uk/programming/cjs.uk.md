{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Файл CJS – файл коду CommonJS",
  "description":"Що таке файл .cjs і як його відкрити?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Що таке файл CJS?

Файл CommonJS (CJS) — це файл, який містить код JavaScript, написаний у синтаксисі CommonJS. CommonJS — це модульна система, розроблена для роботи в середовищах поза зовнішніми веб-браузерами, і вона часто використовується в серверних середовищах JavaScript, як-от Node.js.

## Формат файлу CJS - Додаткова інформація

Файли CJS написані в синтаксисі CommonJS і можуть редагуватися в будь-якому текстовому редакторі, наприклад Microsoft Notepad або Apple TextEdit. Модулі CommonJS зазвичай зберігаються в окремих файлах і призначені для інкапсуляції та модульування коду для кращої організації та зручності обслуговування. Ці модулі використовують необхідну функцію для імпорту залежностей і об’єкт module.exports або exports для надання значень і функцій, які можуть використовуватися іншими частинами коду.

## Приклад коду CJS

Модулі CommonJS мають спеціальний синтаксис і структуру, яка включає такі функції, як необхідна функція для імпорту інших модулів і module.exports або експортує об’єкти для експорту значень, функцій або об’єктів із модуля. Ці модулі використовуються для інкапсуляції та розділення фрагментів коду, що полегшує керування та підтримку великих кодових баз JavaScript. Ось базовий приклад модуля CommonJS:

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

## Посилання

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
