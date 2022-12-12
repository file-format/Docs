---
date: 2019-10-11
keywords: css, .css, формат файлу css, як відкрити файли css, каскадні таблиці стилів
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файлу CSS
linktitle: CSS
description: "Дізнайтеся про формат файлів CSS та API, які можуть створювати та відкривати файли CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Що таке файл CSS? ##

CSS (каскадні таблиці стилів) — це файли, які описують, як елементи HTML відображаються на екрані, папері тощо. За допомогою HTML ви можете мати або вбудовані стилі, або стилі можна визначати у зовнішній таблиці стилів. Для вбудовування стилів \ <style>\</style> використовуються теги. Зовнішні таблиці стилів зберігаються у файлах із розширенням .css. За допомогою зовнішнього CSS ви можете включити його на кілька сторінок HTML, щоб оновити стиль цих сторінок. Навіть один файл CSS можна використовувати для оформлення повного веб-сайту.

## Коротка історія ##

CSS1 був випущений у 1996 році з Бертом Босом як співавтором. Робоча група CSS почала працювати над питаннями, які не були розглянуті в CSS1. Це призвело до створення CSS2 у листопаді 1997 року, який був опублікований як рекомендація W3C 12 травня 1998 року. У цій версії додано підтримку пристроїв, пов’язаних із медіафайлами, таких як принтери, шрифти, які можна завантажити, таблиці та позиціонування елементів. У червні 1999 року CSS3 став рекомендацією W3C. Це розділило документацію на модулі, де кожен модуль мав функції розширення, визначені в CSS2.

## Як використовувати файли CSS ##

Щоб використовувати файл CSS, ви додаєте його в головний розділ документа HTML. Ви використовуєте тег посилання, щоб включити файл, як показано нижче.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

атрибут *href* тегу посилання містить шлях до файлу CSS. Таким чином, застосовні стилі, що містяться у включеному файлі CSS, застосовуються до документа HTML.

## Синтаксис CSS ##

Правило CSS складається з двох компонентів: селектора та оголошення. Селектор вказує на елемент у документі HTML. Це може бути тег елемента, ім’я класу, ім’я ідентифікатора, кілька тегів, що показують ієрархію тощо. Оголошення містить визначення стилю, що складається з властивості та значення. Властивість визначає властивість елемента, який потрібно змінити, а значення визначає його нове значення. Кожне правило CSS може мати кілька декларацій. Нижче наведено приклад правила CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

У наведеному вище прикладі ми маємо **h1** як селектор, який вибирає всі теги h1 у документі HTML. Правило має два оголошення, одне для font-weight, інше для кольору. *font-weight* і *color* є властивостями, а *700* і *forestgreen* є їхніми значеннями відповідно.

## Приклад використання CSS ##

Нижче показано приклад HTML-документа та таблицю стилів, використану для його стилізації. Порівняльне зображення також додається для порівняння стилізованих і простих документів HTML

### Документ HTML ###

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

### Таблиця стилів CSS ###

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

### Порівняння результатів ###

Ліва частина зображення відображає HTML-документ без застосованих стилів, а права – HTML-документ із застосованими стилями.

{{< figure src="../CssExample.jpg" alt="Приклад зображення" >}}

## Посилання ##

– [CSS – Вікіпедія](https://en.wikipedia.org/wiki/CSS)

