---
date: 2019-10-11
keywords: js, .js, js файлов формат, как да отваряте js файлове, javascript файлове
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS файлов формат
linktitle: JS
description: "Научете за JS файловия формат и API, които могат да създават и отварят JS файлове."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Какво е JS файл? ##

JS (JavaScript) са файлове, които съдържат JavaScript код за изпълнение на уеб страници. JavaScript файловете се съхраняват с разширение .js. В документа [HTML](/bg/web/html/) можете или да вградите JavaScript кода, като използвате \ <script>\</script> тагове или включете JS файл. Подобно на [CSS](/bg/web/css/) файловете, JS файловете могат да бъдат включени в множество HTML документи за повторно използване на кода. JavaScript може да се използва за манипулиране на HTML DOM.

## Кратка история ##

JavaScript беше доставен за първи път като част от браузъра Navigator през септември 1995 г. с името LiveScript от Netscape. Три месеца по-късно беше преименуван на JavaScript. През 1996 г. Microsoft реконструира интерпретатора на Navigator, за да създаде JScript. JScript беше пуснат с Internet Explorer и беше много различен от JavaScript.

Netscape изпрати JavaScript на ECMA International, което доведе до официалното издаване на първата спецификация на ECMAScript през 1997 г. ECMAScript 2 беше пуснат през 1998 г., ECMAScript 3 през 1999 г., а работата по ECMAScript 4 започна през 2000 г., но така и не достигна до успех.

Джеси Джеймс Гарет през 2005 г. публикува бяла книга, в която въвежда термина *Ajax*. Това използва JavaScript като гръбнак за създаване на уеб приложения, които зареждат данни във фонов режим и избягват пълно презареждане на страници. Това доведе до създаването на библиотеки като JQuery, Prototype, Dojo и др.

Google пусна браузъра Chrome с V8 JavaScript двигател през 2008 г. В началото на 2009 г. беше сключено споразумение за комбиниране на цялата съответна работа и за придвижване на JavaScript напред. Това доведе до пускането на стандарта ECMAScript 5 през декември 2009 г.

## Как да използвате JS файлове ##

За да използвате JS файл, вие го включвате в HTML документа. Използвате етикета за връзка, за да включите файла, както е показано по-долу.

```html
<script src="site.js"></script>
```

Атрибутът *src* на маркера *script* съдържа пътя до JS файла. По този начин JS функционалността се добавя към HTML документа.

## JS синтаксис ##

JavaScript файловете могат да съдържат променливи, оператори, функции, условия, цикли, масиви, обекти и т.н. По-долу е даден кратък преглед на синтаксиса на JavaScript.

- Всяка команда завършва с точка и запетая (;).
- Използвайте ключовата дума *var* за деклариране на променливи.
- Поддържа аритметични оператори ( + - * / ) за изчисляване на стойности.
- Едноредовите коментари се добавят с //, а многоредовите са оградени с /* и */.
- Всички идентификатори са чувствителни към регистъра, т.е. *modelNo* и *modelno* са две различни променливи.
- Функциите се дефинират с помощта на ключовата дума *function*.
- Масивите могат да бъдат дефинирани с квадратни скоби [].
- JS поддържа оператори за сравнение като ==, !=, >=, !== и др.
- Класовете могат да бъдат дефинирани с помощта на ключовата дума *class*.

## Пример за използване на JS ##

По-долу е показан прост пример за използване на JavaScript файл.

### HTML документ ###

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

### JS код ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Препратки ##

– [JS – Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

