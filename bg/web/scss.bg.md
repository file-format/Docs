---
date: 2019-10-11
keywords: scss, .scss, scss файлов формат, как да отваряте scss файлове, синтактично страхотен стилов лист, css препроцесор, sass
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS файлов формат - Sass Cascading Style Sheet
linktitle: SCSS
description: "Научете за SCSS файловия формат и API, които могат да създават и отварят SCSS файлове."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Какво е SCSS файл? ##

SCSS е вторият синтаксис на Sass (Syntactically Awesome Stylesheet), който използва скоби вместо вдлъбнатини. SCSS е проектиран по такъв начин, че валиден CSS3 файл също е валиден SCSS файл. SCSS файловете се съхраняват с разширение .scss.

## Защо да използвате SCSS ##

Тъй като дизайнът на уебсайтовете става сложен, което води до големи [CSS](/bg/web/css/) файлове. Такива файлове се поддържат по-трудно. Тук се намесва SCSS. SCSS въвежда променливи, влагане, миксини, импортиране и наследяване на селектори в разработката на CSS. Тези допълнения правят работата с дизайна много по-забавна.

## Как да използвате SCSS файлове ##

SCSS файловете не са включени директно в [HTML](/bg/web/html/) документа като CSS. Вместо това SCSS файловете се преобразуват в CSS файлове, които са включени в HTML файловете. За да инсталирате SCSS на вашата система, следвайте инструкциите, дадени на [Официалния сайт на Sass](https://sass-lang.com/install).
За да конвертирате SCSS в CSS, можете или да конвертирате вече записан SCSS файл, или да следите за промени и да конвертирате, докато файлът се записва. Командите и за двете са дадени по-долу.

### Преобразуване веднъж ###

Първият параметър е изходният SCSS файл, а вторият параметър е изходният CSS файл.

```cmd
sass main.scss main.css
```

### Следете за промени ###

Командата има допълнителен флаг *watch**, който поддържа изпълнението на командата и веднага щом SCSS файлът бъде записан, се генерира изходен CSS.

```cmd
sass --watch main.scss main.css
```

## Синтаксис на SCSS ##

SCSS поддържа променливи, влагане, миксини, импортиране, наследяване на селектор и т.н. По-долу са дадени примери за тези функции.

### Променливи ###

Чрез използването на променливи можете да зададете информация за многократна употреба, като основен цвят или цвят на фона за бутона за запазване. Това е полезно, ако трябва да промените тази информация, просто я променяте на едно място и тя се актуализира, където и да се използва.

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

**Генериран CSS**

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

### Вмъкване ###

Можете да вложите CSS селекторите подобно на йерархията на HTML. В примера, даден по-долу, диапазонът е вложен в блока h1.

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

**Генериран CSS**

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

### Миксини ###

Миксините могат да се използват за групиране на подобни свойства заедно, които се използват заедно на множество места. Можете също да предавате параметри на миксини.

**SCSS**

**Деклариране на миксин**

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

**Използване на миксин**

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

**Генериран CSS**

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

### Разшири ###

Разширяването/наследяването е полезно в случаите, когато свойствата на един селектор трябва да бъдат споделени с друг селектор. В примера по-долу селекторът *.error-notice* взема всички свойства на селектора *.error-text* и добавя свойства за рамка и подложка.

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

**Генериран CSS**

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

### Импортиране ###

Импортирането може да бъде полезно при разделянето на концерните. Можете да разделите стиловете по такъв начин, че стиловете на заглавния колонтитул да са в отделен файл, стиловете на долния колонтитул да са в отделен файл, всички цветови променливи, използвани в стиловете, да бъдат в отделен файл и т.н. Използвайки тази техника, стиловете остават организирани. Просто импортирате файловете във вашия основен SCSS файл, както е показано в примера по-долу. Не е необходимо да посочвате файловото разширение в инструкцията за импортиране. Sass компилира директно всички SCSS файлове. За да избегнете директното компилиране на импортирани файлове, можете да ги направите частични, като добавите долна черта (_) преди името им. Можете да импортирате части, подобни на нормалните SCSS файлове, без долната черта.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Изходният CSS ще съдържа стиловете от всички импортирани файлове.

## Препратки ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

