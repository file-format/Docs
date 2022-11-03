---
date: 2019-10-11
keywords: sass, .sass, формат файла sass, как открыть файлы sass, синтаксически классная таблица стилей, препроцессор css, sass
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файла Sass
linktitle: Sass
description: "Узнайте о формате файлов Sass и API, которые могут создавать и открывать файлы Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## .SASS вариант № ##

Sass (синтаксически удивительные таблицы стилей) — это язык сценариев с препроцессором. Он скомпилирован в [CSS](/ru/web/css/) и хранится с расширением .sass. Sass состоит из двух синтаксисов: исходный, основанный на отступах, который использует расширение .sass, и более новый SCSS с блочным форматированием, такой как CSS, который использует расширение .scss.

## Зачем использовать Sass ##

Sass действительно полезен для поддержки стилей, поскольку он предоставляет множество функций, таких как введение переменных, вложенность, примеси, импорт и наследование селекторов, которые делают работу со стилями увлекательной.

## Как использовать файлы SASS ##

Файлы SASS не включаются непосредственно в документ [HTML](/ru/web/html/), а преобразуются в файлы CSS, которые включаются в файлы HTML. Вы можете установить Sass в своей системе, следуя инструкциям на [Официальном сайте Sass] (https://sass-lang.com/install).

Sass можно преобразовать в CSS либо путем преобразования уже сохраненного файла SASS, либо путем отслеживания изменений и преобразования по мере сохранения файла. Команды для обоих приведены ниже.

### Преобразовать один раз ###

Первый параметр команды — это исходный файл SASS, а второй параметр — выходной файл CSS.

```cmd
sass main.sass main.css
```

### Следите за изменениями ###

Приведенную выше команду можно запустить с дополнительным флагом *watch*, который поддерживает выполнение команды, и как только файл Sass будет сохранен, будет сгенерирован выходной CSS.

```cmd
sass --watch main.sass main.css
```

## Синтаксис Sass ##

Sass поддерживает переменные, вложенность, примеси, импорт, наследование селекторов и т. д. Ниже приведены примеры этих функций.

### Переменные ###

Переменные можно использовать для установки многократно используемой информации, такой как основной цвет или отступ для кнопки. Это может оказаться полезным, если в будущем вам понадобится изменить эту информацию, вы просто меняете ее в одном месте, и она обновляется везде.

**Сасс**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

Селекторы CSS могут быть вложены подобно иерархии HTML. В следующем примере диапазон вложен в блок h1.

**Сасс**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

Миксины используются для группировки похожих свойств, которые используются в нескольких местах. Миксины также поддерживают параметры.

**Сасс**

**Объявление миксина**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Использование миксина**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Расширение/наследование может оказаться полезным в случаях, когда свойства одного селектора необходимо использовать совместно с другим селектором. В приведенном ниже примере селектор *.error-notice* принимает все свойства селектора *.error-text* и добавляет свойства границы и заполнения.

**Сасс**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

Импорт может быть полезен, если вы структурируете свои стили в разные файлы на основе функциональности или любой другой структуры, которой вы следуете. Вы можете импортировать все эти файлы в основной файл SASS, который позже преобразуется в CSS. При импорте не нужно указывать расширение файла в инструкции по импорту. Sass компилирует все файлы SASS напрямую. Чтобы файлы импорта не компилировались напрямую, вы можете сделать их частичными, добавив подчеркивание (_) в начале их имени. Частичные импортируются аналогично обычным файлам Sass.

**Сасс**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Выходной CSS будет содержать стили из всех импортированных файлов.

## Использованная литература ##

- [Sass - Википедия](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Сасс] (https://sass-lang.com/)

