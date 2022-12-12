---
date: 2019-10-11
keywords: sass, .sass, sass файлов формат, как да отваряте sass файлове, синтактично страхотен стилов лист, css препроцесор, sass
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Файлов формат Sass
linktitle: Sass
description: "Научете за файловия формат на Sass и API, които могат да създават и отварят Sass файлове."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Какво е SASS файл? ##

Sass (синтактично страхотни стилови таблици) е скриптов език за препроцесор. Той се компилира в [CSS](/bg/web/css/) и се съхранява с разширението .sass. Sass се състои от два синтаксиса, оригиналът, базиран на вдлъбнатини, който използва разширението .sass, и по-новият SCSS с блоково форматиране като CSS, който използва разширението .scss.

## Защо да използвате Sass ##

Sass е наистина полезен при поддържането на стилове, тъй като предоставя много функции като въвеждане на променливи, влагане, миксини, импортиране и наследяване на селектори, които правят работата със стилове забавна.

## Как да използвате SASS файлове ##

SASS файловете не са включени директно в документа [HTML](/bg/web/html/), а по-скоро се конвертират в CSS файлове, които са включени в HTML файловете. Можете да инсталирате Sass на вашата система, като следвате инструкциите, дадени на [Официалния сайт на Sass](https://sass-lang.com/install).

Sass може да бъде преобразуван в CSS или чрез конвертиране на вече записан SASS файл, или чрез наблюдение за промени и конвертиране, докато файлът се запазва. Командите и за двете са дадени по-долу.

### Преобразуване веднъж ###

Първият параметър на командата е изходният SASS файл, а вторият параметър е изходният CSS файл.

```cmd
sass main.sass main.css
```

### Следете за промени ###

Горната команда може да се изпълни с допълнителен флаг *watch*, който поддържа командата да работи и веднага щом файлът Sass бъде запазен, се генерира изходен CSS.

```cmd
sass --watch main.sass main.css
```

## Синтаксис на Sass ##

Sass поддържа променливи, влагане, миксини, импортиране, наследяване на селектора и т.н. По-долу са дадени примери за тези функции.

### Променливи ###

Променливите могат да се използват за задаване на информация за многократна употреба, като основен цвят или подложка за бутон. Това може да се окаже полезно, ако в бъдеще трябва да промените тази информация, просто я промените на едно място и тя се актуализира навсякъде.

**Sass**

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

CSS селекторите могат да бъдат вложени подобно на йерархията на HTML. В следващия пример обхватът е вложен в блока h1.

**Sass**

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

Миксините се използват за групиране на подобни свойства заедно, които се използват на множество места. Миксините също поддържат параметри.

**Sass**

**Деклариране на миксин**

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

**Използване на миксин**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Разширяването/Наследяването може да се окаже полезно в случаите, когато свойствата на един селектор трябва да бъдат споделени с друг селектор. В примера по-долу селекторът *.error-notice* взема всички свойства на селектора *.error-text* и добавя свойства за рамка и подложка.

**Sass**

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

Импортирането може да бъде полезно, ако структурирате вашите стилове в различни файлове въз основа на функционалност или всяка друга структура, която следвате. Можете да импортирате всички тези файлове в първичен SASS файл, който по-късно се преобразува в CSS. Докато импортирате, не е необходимо да указвате разширението на файла в инструкцията за импортиране. Sass компилира директно всички SASS файлове. За да избегнете директното компилиране на импортирани файлове, можете да ги направите частични, като добавите долна черта (_) в началото на името им. Частичните елементи се импортират подобно на нормалните Sass файлове.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Изходният CSS ще съдържа стиловете от всички импортирани файлове.

## Препратки ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

