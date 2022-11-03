---
date: 2019-10-11
keywords: scss, .scss, формат файла scss, как открыть файлы scss, синтаксически классная таблица стилей, препроцессор css, sass
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файла SCSS — каскадная таблица стилей Sass
linktitle: SCSS
description: "Узнайте о формате файлов SCSS и API, которые могут создавать и открывать файлы SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## .SCSS вариант № ##

SCSS — это второй синтаксис Sass (Syntactically Awesome Stylesheet), в котором вместо отступов используются скобки. SCSS был разработан таким образом, что действительный файл CSS3 также является действительным файлом SCSS. Файлы SCSS хранятся с расширением .scss.

## Зачем использовать SCSS ##

Поскольку дизайн веб-сайтов становится все более сложным, это приводит к большим файлам [CSS](/ru/web/css/). Такие файлы сложнее поддерживать. Вот тут-то и появляется SCSS. SCSS вводит переменные, вложенность, примеси, импорт и наследование селекторов в разработке CSS. Эти дополнения делают работу с дизайном намного веселее.

## Как использовать файлы SCSS ##

Файлы SCSS не включаются непосредственно в документ [HTML](/ru/web/html/), как CSS. Вместо этого файлы SCSS преобразуются в файлы CSS, которые включаются в файлы HTML. Чтобы установить SCSS в вашей системе, следуйте инструкциям на [Официальном сайте Sass] (https://sass-lang.com/install).
Чтобы преобразовать SCSS в CSS, вы можете либо преобразовать уже сохраненный файл SCSS, либо следить за изменениями и преобразовывать по мере сохранения файла. Команды для обоих приведены ниже.

### Преобразовать один раз ###

Первый параметр — это исходный файл SCSS, а второй параметр — выходной файл CSS.

```cmd
sass main.scss main.css
```

### Следите за изменениями ###

У команды есть дополнительный флаг *watch**, который поддерживает выполнение команды, и как только файл SCSS будет сохранен, будет сгенерирован выходной CSS.

```cmd
sass --watch main.scss main.css
```

## Синтаксис SCSS ##

SCSS поддерживает переменные, вложенность, примеси, импорт, наследование селекторов и т. д. Ниже приведены примеры этих функций.

### Переменные ###

Используя переменные, вы можете установить многократно используемую информацию, такую как основной цвет или цвет фона для кнопки сохранения. Это полезно, если вам нужно изменить эту информацию, вы просто меняете ее в одном месте, и она обновляется везде, где она используется.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**Сгенерированный CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Вложение ###

Вы можете вкладывать селекторы CSS подобно иерархии HTML. В приведенном ниже примере диапазон вложен в блок h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**Сгенерированный CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Миксины ###

Примеси можно использовать для группировки похожих свойств, которые используются вместе в нескольких местах. Вы также можете передавать параметры миксинам.

**SCSS**

**Объявление миксина**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Использование миксина**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**Сгенерированный CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Продлевать ###

Расширение/наследование полезно в тех случаях, когда свойства одного селектора необходимо использовать совместно с другим селектором. В приведенном ниже примере селектор *.error-notice* принимает все свойства селектора *.error-text* и добавляет свойства границы и заполнения.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**Сгенерированный CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Импорт ###

Импорт может быть полезен при разделении ответственности. Вы можете разделить стили таким образом, что стили заголовка находятся в отдельном файле, стили нижнего колонтитула — в отдельном файле, все цветовые переменные, используемые в стилях, могут быть в отдельном файле и т. д. Используя эту технику, стили остаются организованными. Вы просто импортируете файлы в свой основной файл SCSS, как показано в примере ниже. Вам не нужно указывать расширение файла в инструкции по импорту. Sass компилирует все файлы SCSS напрямую. Чтобы файлы импорта не компилировались напрямую, вы можете сделать их частичными, добавив подчеркивание (_) перед их именем. Вы можете импортировать частичные файлы, аналогичные обычным файлам SCSS, без подчеркивания.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Выходной CSS будет содержать стили из всех импортированных файлов.

## Использованная литература ##

- [SCSS - Википедия](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Сасс] (https://sass-lang.com/)

