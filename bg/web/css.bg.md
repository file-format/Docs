---
date: 2019-10-11
keywords: css, .css, css файлов формат, как да отваряте css файлове, каскадни стилови таблици
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS файлов формат
linktitle: CSS
description: "Научете за CSS файловия формат и API, които могат да създават и отварят CSS файлове."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Какво е CSS файл? ##

CSS (Cascading Style Sheets) са файлове, които описват как HTML елементите се показват на екрана, хартията и т.н. С HTML можете да имате или вградени стилове, или стиловете могат да бъдат дефинирани във външен лист със стилове. За вграждане на стиловете, \ <style>\</style> се използват етикети. Външните таблици със стилове се съхраняват във файлове с разширение .css. С външния CSS можете да го включите в множество HTML страници, за да актуализирате стила на тези страници. Дори един CSS файл може да се използва за стилизиране на цял уебсайт.

## Кратка история ##

CSS1 беше пуснат през 1996 г. със съавтор Берт Бос. Работната група на CSS започна работа по проблемите, които не бяха разгледани в CSS1. Това доведе до създаването на CSS2 през ноември 1997 г., който беше публикуван като препоръка на W3C на 12 май 1998 г. Тази версия добави поддръжка за специфични за медия устройства като принтери, шрифтове за изтегляне, таблици и позициониране на елементи. През юни 1999 г. CSS3 стана препоръка на W3C. Това раздели документацията на модули, като всеки модул имаше функции за разширение, дефинирани в CSS2.

## Как да използвате CSS файлове ##

За да използвате CSS файл, вие го включвате в секцията head на HTML документа. Използвате етикета за връзка, за да включите файла, както е показано по-долу.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

атрибутът *href* на етикета за връзка съдържа пътя до CSS файла. По този начин приложимите стилове, съдържащи се във включения CSS файл, се прилагат към HTML документа.

## CSS синтаксис ##

CSS правилото се състои от два компонента, селектор и декларация. Селекторът сочи към елемент в HTML документа. Това може да бъде етикет на елемент, име на клас, име на идентификатор, множество тагове, показващи йерархията и т.н. Декларацията съдържа дефиницията на стил, състояща се от свойство и стойност. Свойството идентифицира свойството на елемента, което искате да промените, и стойността определя неговата нова стойност. Всяко CSS правило може да има множество декларации. Следното е пример за CSS правило.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

В горния пример имаме **h1** като селектор, който избира всички h1 тагове в HTML документа. Правилото има две декларации, едната за теглото на шрифта, а другата за цвета. *font-weight* и *color* са свойства, а *700* и *forestgreen* са съответно техните стойности.

## Пример за използване на CSS ##

Следното показва примерния HTML документ и таблицата със стилове, използвана за стилизирането му. Изображението за сравнение също се добавя за сравняване на стилизираните и обикновените HTML документи

### HTML документ ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS таблица със стилове ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Сравнение на изхода ###

Лявата страна на изображението показва HTML документа без приложените стилове, а дясната страна показва HTML документа с приложените стилове.

{{< figure src="../CssExample.jpg" alt="Примерно изображение" >}}

## Препратки ##

– [CSS – Wikipedia](https://en.wikipedia.org/wiki/CSS)

