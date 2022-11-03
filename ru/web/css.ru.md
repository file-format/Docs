---
date: 2019-10-11
keywords: css, .css, формат файла css, как открыть файлы css, каскадные таблицы стилей
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файла CSS
linktitle: CSS
description: "Узнайте о формате файла CSS и API, которые могут создавать и открывать файлы CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## .CSS вариант № ##

CSS (каскадные таблицы стилей) — это файлы, описывающие, как HTML-элементы отображаются на экране, бумаге и т. д. С помощью HTML вы можете иметь либо встроенные стили, либо стили, определяемые во внешней таблице стилей. Для встраивания стилей \ <style>\</style> используются теги. Внешние таблицы стилей хранятся в файлах с расширением .css. С помощью внешнего CSS вы можете включить его на несколько HTML-страниц, чтобы обновить стиль этих страниц. Даже один CSS-файл можно использовать для оформления всего веб-сайта.

## Краткая история ##

CSS1 был выпущен в 1996 году с Бертом Босом в качестве соавтора. Рабочая группа CSS начала работать над проблемами, которые не были учтены в CSS1. Это привело к созданию CSS2 в ноябре 1997 года, который был опубликован в качестве рекомендации W3C 12 мая 1998 года. В этой версии добавлена поддержка устройств, специфичных для медиа, таких как принтеры, загружаемые шрифты, таблицы и позиционирование элементов. В июне 1999 года CSS3 стал рекомендацией W3C. Это разделило документацию на модули, где каждый модуль имел функции расширения, определенные в CSS2.

## Как использовать файлы CSS ##

Чтобы использовать файл CSS, вы включаете его в раздел заголовка HTML-документа. Вы используете тег ссылки для включения файла, как показано ниже.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

атрибут *href* тега ссылки содержит путь к файлу CSS. При этом применимые стили, содержащиеся во включенном файле CSS, применяются к документу HTML.

## Синтаксис CSS ##

Правило CSS состоит из двух компонентов: селектора и объявления. Селектор указывает на элемент в документе HTML. Это может быть либо тег элемента, имя класса, имя идентификатора, несколько тегов, показывающих иерархию, и т. д. Объявление содержит определение стиля, состоящее из свойства и значения. Свойство определяет свойство элемента, которое вы хотите изменить, а значение определяет его новое значение. Каждое правило CSS может иметь несколько объявлений. Ниже приведен пример правила CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

В приведенном выше примере у нас есть **h1** в качестве селектора, который выбирает все теги h1 в HTML-документе. Правило имеет два объявления: одно для веса шрифта, а другое для цвета. *font-weight* и *color* — это свойства, а *700* и *forestgreen* — их значения соответственно.

## Пример использования CSS ##

Ниже показан пример HTML-документа и таблица стилей, используемая для его оформления. Также добавлено сравнительное изображение для сравнения стилизованных и простых HTML-документов.

### HTML-документ ###

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

### Таблица стилей CSS ###

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

### Сравнение результатов ###

В левой части изображения отображается HTML-документ без примененных стилей, а в правой части — HTML-документ с примененными стилями.

{{< figure src="../CssExample.jpg" alt="Пример изображения" >}}

## Использованная литература ##

- [CSS - Википедия](https://en.wikipedia.org/wiki/CSS)

