---
date: 2019-10-11
keywords: js, .js, формат файлу js, як відкрити файли js, файли javascript
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файлу JS
linktitle: JS
description: "Дізнайтеся про формат файлів JS та API, які можуть створювати та відкривати файли JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Що таке файл JS? ##

JS (JavaScript) — це файли, які містять код JavaScript для виконання на веб-сторінках. Файли JavaScript зберігаються з розширенням .js. У документ [HTML](/uk/web/html/) ви можете вставити код JavaScript за допомогою \ <script>\</script> теги або включити файл JS. Подібно до файлів [CSS](/uk/web/css/), файли JS можна включати в кілька документів HTML для повторного використання коду. JavaScript можна використовувати для маніпулювання HTML DOM.

## Коротка історія ##

У вересні 1995 року під назвою LiveScript компанія Netscape вперше представила JavaScript як частину браузера Navigator. Через три місяці він був перейменований у JavaScript. У 1996 році Microsoft переробила інтерпретатор Navigator для створення JScript. JScript був випущений разом з Internet Explorer і сильно відрізнявся від JavaScript.

Netscape надіслав JavaScript до ECMA International, що призвело до офіційного випуску першої специфікації ECMAScript у 1997 році. ECMAScript 2 був випущений у 1998 році, ECMAScript 3 у 1999 році, а робота над ECMAScript 4 почалася у 2000 році, але так і не була завершена.

Джессі Джеймс Гаррет у 2005 році випустив білу книгу, де ввів термін *Ajax*. Це використовувало JavaScript як основу для створення веб-додатків, які завантажували дані у фоновому режимі та уникали повного перезавантаження сторінки. Це призвело до створення таких бібліотек, як JQuery, Prototype, Dojo тощо.

У 2008 році Google випустив браузер Chrome із механізмом JavaScript V8. На початку 2009 року було укладено угоду про об’єднання всіх відповідних робіт і просування JavaScript вперед. Це призвело до випуску стандарту ECMAScript 5 у грудні 2009 року.

## Як використовувати файли JS ##

Щоб використовувати файл JS, ви включаєте його в документ HTML. Ви використовуєте тег посилання, щоб включити файл, як показано нижче.

```html
<script src="site.js"></script>
```

Атрибут *src* тегу *script* містить шлях до файлу JS. Завдяки цьому до документа HTML додається функція JS.

## Синтаксис JS ##

Файли JavaScript можуть містити змінні, оператори, функції, умови, цикли, масиви, об’єкти тощо. Нижче наведено короткий огляд синтаксису JavaScript.

- Кожна команда закінчується крапкою з комою (;).
- Використовуйте ключове слово *var* для оголошення змінних.
- Підтримує арифметичні оператори ( + - * / ) для обчислення значень.
- Однорядкові коментарі додаються за допомогою //, а багаторядкові коментарі оточуються /* і */.
- Усі ідентифікатори чутливі до регістру, тобто *modelNo* і *modelno* – це дві різні змінні.
- Функції визначаються за допомогою ключового слова *function*.
- Масиви можна визначити за допомогою квадратних дужок [].
- JS підтримує такі оператори порівняння, як ==, != , >=, !== тощо.
- Класи можна визначити за допомогою ключового слова *class*.

## Приклад використання JS ##

Нижче показано простий приклад використання файлу JavaScript.

### Документ HTML ###

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

### Код JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Посилання ##

– [JS – Вікіпедія](https://en.wikipedia.org/wiki/JavaScript)

