---
date: 2019-10-11
keywords: scss, .scss, формат файлу scss, як відкрити файли scss, синтаксично чудова таблиця стилів, препроцесор css, sass
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файлу SCSS – каскадна таблиця стилів Sass
linktitle: SCSS
description: "Дізнайтеся про формат файлів SCSS та API, які можуть створювати та відкривати файли SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Що таке файл SCSS? ##

SCSS — це другий синтаксис Sass (Syntactically Awesome Stylesheet), який використовує дужки замість відступів. SCSS розроблено таким чином, що дійсний файл CSS3 також є дійсним файлом SCSS. Файли SCSS зберігаються з розширенням .scss.

## Навіщо використовувати SCSS ##

Дизайн веб-сайтів стає складнішим, що призводить до появи великих файлів [CSS](/uk/web/css/). Такі файли важче підтримувати. Тут на допомогу приходить SCSS. SCSS представляє змінні, вкладення, міксини, імпорт та успадкування селекторів у розробці CSS. Ці доповнення роблять роботу з дизайном набагато цікавішою.

## Як використовувати файли SCSS ##

Файли SCSS не включені безпосередньо в документ [HTML](/uk/web/html/), як CSS. Натомість файли SCSS перетворюються на файли CSS, які входять до файлів HTML. Щоб установити SCSS у вашій системі, дотримуйтесь інструкцій, наведених на [офіційному сайті Sass](https://sass-lang.com/install).
Щоб конвертувати SCSS у CSS, ви можете конвертувати вже збережений файл SCSS або спостерігати за змінами та конвертувати, коли файл буде збережено. Нижче наведено команди для обох.

### Перетворити один раз ###

Перший параметр – вихідний файл SCSS, а другий параметр – вихідний файл CSS.

```cmd
sass main.scss main.css
```

### Слідкуйте за змінами ###

Команда має додатковий прапорець *watch**, який підтримує виконання команди, і щойно файл SCSS буде збережено, буде створено вихідний CSS.

```cmd
sass --watch main.scss main.css
```

## Синтаксис SCSS ##

SCSS підтримує змінні, вкладення, міксини, імпорт, успадкування селекторів тощо. Нижче наведено приклади цих функцій.

### Змінні ###

Використовуючи змінні, ви можете встановити багаторазову інформацію, таку як основний колір або колір фону для кнопки збереження. Це корисно, якщо вам потрібно змінити цю інформацію, ви просто змінюєте її в одному місці, і вона оновлюється там, де вона використовується.

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

**Згенерований CSS**

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

### вкладення ###

Ви можете вкладати селектори CSS подібно до ієрархії HTML. У наведеному нижче прикладі span вкладено всередину блоку h1.

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

**Згенерований CSS**

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

### Міксини ###

Міксини можна використовувати для групування схожих властивостей, які використовуються разом у кількох місцях. Ви також можете передавати параметри в міксини.

**SCSS**

**Оголошення міксину**

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

**Використання міксина**

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

**Згенерований CSS**

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

### Розширити ###

Extend/Inheritance корисно у випадках, коли властивості одного селектора потрібно поділити з іншим селектором. У наведеному нижче прикладі селектор *.error-notice* приймає всі властивості селектора *.error-text* і додає властивості рамки та відступу.

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

**Згенерований CSS**

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

### Імпорт ###

Імпортування може бути корисним для поділу концернів. Ви можете розділити стилі таким чином, щоб стилі заголовка були в окремому файлі, стилі нижнього колонтитула були в окремому файлі, усі змінні кольору, які використовуються в стилях, могли бути в окремому файлі тощо. Використовуючи цю техніку, стилі залишаються організованими. Ви просто імпортуєте файли у свій основний файл SCSS, як показано в прикладі нижче. Вам не потрібно вказувати розширення файлу в інструкції з імпорту. Sass компілює всі файли SCSS безпосередньо. Щоб уникнути безпосередньої компіляції файлів імпорту, ви можете зробити їх частковими, додавши символ підкреслення (_) перед їхнім ім’ям. Ви можете імпортувати частини, подібні до звичайних файлів SCSS, без підкреслення.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Вихідний CSS матиме стилі з усіх імпортованих файлів.

## Посилання ##

– [SCSS – Вікіпедія](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

