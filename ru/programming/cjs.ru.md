{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Файл CJS — файл кода CommonJS",
  "description":"Что такое файл .cjs и как его открыть?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Что такое файл CJS?

Файл CommonJS (CJS) — это файл, содержащий код JavaScript, написанный с использованием синтаксиса CommonJS. CommonJS — это система модулей, предназначенная для работы в средах, выходящих за рамки веб-браузеров, и она часто используется в серверных средах JavaScript, таких как Node.js.

## Формат файла CJS – дополнительная информация

Файлы CJS написаны с использованием синтаксиса CommonJS и могут редактироваться в любом текстовом редакторе, например Microsoft Notepad или Apple TextEdit. Модули CommonJS обычно хранятся в отдельных файлах и предназначены для инкапсуляции и модуляризации кода для лучшей организации и удобства обслуживания. Эти модули используют требуемую функцию для импорта зависимостей и объект Module.exports или Exports для предоставления значений и функций, которые могут использоваться другими частями кода.

## Пример кода CJS

Модули CommonJS имеют особый синтаксис и структуру, которая включает в себя такие функции, как обязательная функция для импорта других модулей и модуль.exports или экспортирует объекты для экспорта значений, функций или объектов из модуля. Эти модули используются для инкапсуляции и разделения фрагментов кода, что упрощает управление и поддержку больших баз кода JavaScript. Вот базовый пример модуля CommonJS:

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

## Использованная литература

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
