{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Файл", "Розширення", "Формат файлу", "Розширення файлу", "Файл модуля Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - файл Javascript модуля Node.js ES",
  "description" :"Дізнайтеся, що таке файл MJS та API, які можуть створювати та відкривати файл MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Що таке файл MJS?

Файл із розширенням .mjs — це файл вихідного коду JavaScript, який використовується як модуль ECMA (модуль ECMAScript) у програмах Node.js. Модульна система natvie Node.js — це CommonJS, який використовується для поділу коду на різні файли, щоб упорядкувати код [JS](/uk/web/js/). MJS — це єдиний спосіб, який Node.js використовує для визначення того, чи є модуль CommonJS чи ES6. Модулі ECMAScript є стандартною формою для упаковки коду JavaScript для повторного використання. Файли MJS можна відкривати в текстових редакторах, таких як Atom, Vim, Apple xCode, Microsoft Visual Studio та Notepad.

## Формат файлу MJS – додаткова інформація

Файли MJS зберігаються на диску як звичайний текстовий формат із синтаксисом JavaScript. Їх можна відкрити в будь-якому текстовому редакторі, і вони зрозумілі людині. З 2018 року майже всі основні браузери підтримують модулі ES.

## Відмінності між модулями ES і CommonJS

Отже, чим файли MJS відрізняються від звичайних файлів JS? Різницю між модулями ES і CommonJS можна підсумувати так:

* Не вимагає, експортує або module.exports
* Немає імені \__файлу або \__dirname
* Немає завантаження модуля JSON
* Немає завантаження рідного модуля
* Немає require.resolve
* Немає NODE_PATH
* Не вимагає розширень
* Немає require.cache

## Список літератури

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Різниця між JS і MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

