---
date: 2019-10-11
keywords: js, .js, формат файла js, как открыть файлы js, файлы javascript
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат JS-файла
linktitle: JS
description: "Узнайте о формате файлов JS и API, которые могут создавать и открывать файлы JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## .JS вариант № ##

JS (JavaScript) — это файлы, содержащие код JavaScript для выполнения на веб-страницах. Файлы JavaScript хранятся с расширением .js. Внутри документа [HTML](/ru/web/html/) вы можете либо встроить код JavaScript, используя \ <script>\</script> теги или включить файл JS. Подобно файлам [CSS](/ru/web/css/), файлы JS можно включать в несколько документов HTML для повторного использования кода. JavaScript можно использовать для управления моделью HTML DOM.

## Краткая история ##

JavaScript был впервые выпущен Netscape как часть браузера Navigator в сентябре 1995 года под названием LiveScript. Три месяца спустя он был переименован в JavaScript. В 1996 году Microsoft реконструировала интерпретатор Navigator для создания JScript. JScript был выпущен вместе с Internet Explorer и сильно отличался от JavaScript.

Netscape представила JavaScript в ECMA International, что привело к официальному выпуску первой спецификации ECMAScript в 1997 году. ECMAScript 2 был выпущен в 1998 году, ECMAScript 3 в 1999 году, а работа над ECMAScript 4 началась в 2000 году, но так и не была реализована.

Джесси Джеймс Гарретт в 2005 году выпустил официальный документ, в котором он ввел термин *Ajax*. Это использовало JavaScript в качестве основы для создания веб-приложений, которые загружали данные в фоновом режиме и избегали полной перезагрузки страницы. Это привело к созданию таких библиотек, как JQuery, Prototype, Dojo и т. д.

Google выпустила браузер Chrome с движком JavaScript V8 в 2008 году. В начале 2009 года было заключено соглашение об объединении всей соответствующей работы и продвижении JavaScript вперед. Это привело к выпуску стандарта ECMAScript 5 в декабре 2009 года.

## Как использовать файлы JS ##

Чтобы использовать файл JS, вы включаете его в документ HTML. Вы используете тег ссылки для включения файла, как показано ниже.

```html
<script src="site.js"></script>
```

Атрибут *src* тега *script* содержит путь к файлу JS. При этом функциональные возможности JS добавляются в HTML-документ.

## JS-синтаксис ##

Файлы JavaScript могут содержать переменные, операторы, функции, условия, циклы, массивы, объекты и т. д. Ниже приведен краткий обзор синтаксиса JavaScript.

- Каждая команда заканчивается точкой с запятой (;).
- Используйте ключевое слово *var* для объявления переменных.
- Поддерживает арифметические операторы ( + - * / ) для вычисления значений.
- Однострочные комментарии добавляются с //, а многострочные комментарии заключаются в /* и */.
- Все идентификаторы чувствительны к регистру, т.е. *modelNo* и *modelno* — это две разные переменные.
- Функции определяются с помощью ключевого слова *function*.
- Массивы могут быть определены с помощью квадратных скобок [].
- JS поддерживает операторы сравнения, такие как ==, != , >=, !== и т. д.
- Классы могут быть определены с помощью ключевого слова *class*.

## Пример использования JS ##

Ниже показан простой пример использования файла JavaScript.

### HTML-документ ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### JS-код ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Использованная литература ##

- [JS - Википедия](https://en.wikipedia.org/wiki/JavaScript)

