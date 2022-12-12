---
date: 2019-10-11
keywords: sass, .sass, формат файлу sass, як відкрити файли sass, синтаксично чудова таблиця стилів, препроцесор css, sass
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файлу Sass
linktitle: Sass
description: "Дізнайтеся про формат файлу Sass та API, які можуть створювати та відкривати файли Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Що таке файл SASS? ##

Sass (синтаксично чудові таблиці стилів) — це мова сценаріїв препроцесора. Він скомпільований у [CSS](/uk/web/css/) і зберігається з розширенням .sass. Sass складається з двох синтаксисів: оригінального на основі відступів, що використовує розширення .sass, і новішого SCSS із блоковим форматуванням, як CSS, який використовує розширення .scss.

## Навіщо використовувати Sass ##

Sass дійсно корисний у підтримці стилів, оскільки він надає багато функцій, як-от введення змінних, вкладення, міксини, імпорт та успадкування селектора, які роблять роботу зі стилями веселою.

## Як використовувати файли SASS ##

Файли SASS не включаються безпосередньо в документ [HTML](/uk/web/html/), а перетворюються на файли CSS, які входять до файлів HTML. Ви можете інсталювати Sass у своїй системі, дотримуючись інструкцій, наданих на [офіційному сайті Sass](https://sass-lang.com/install).

Sass можна перетворити на CSS шляхом конвертації вже збереженого файлу SASS або шляхом спостереження за змінами та конвертації під час збереження файлу. Нижче наведено команди для обох.

### Перетворити один раз ###

Перший параметр команди – вихідний файл SASS, а другий параметр – вихідний файл CSS.

```cmd
sass main.sass main.css
```

### Слідкуйте за змінами ###

Наведену вище команду можна запустити з додатковим прапорцем *watch*, який підтримує виконання команди, і щойно файл Sass буде збережено, буде створено вихідний CSS.

```cmd
sass --watch main.sass main.css
```

## Синтаксис Sass ##

Sass підтримує змінні, вкладення, міксини, імпорт, успадкування селекторів тощо. Нижче наведено приклади цих функцій.

### Змінні ###

Змінні можна використовувати для встановлення повторно використовуваної інформації, такої як основний колір або відступ для кнопки. Це може виявитися корисним, якщо в майбутньому вам знадобиться змінити цю інформацію, ви просто змінюєте її в одному місці, і вона оновлюється всюди.

**Зухвалий**

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

Селектори CSS можуть бути вкладені подібно до ієрархії HTML. У наступному прикладі span вкладено всередину блоку h1.

**Зухвалий**

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

Міксини використовуються для групування схожих властивостей, які використовуються в кількох місцях. Міксини також підтримують параметри.

**Зухвалий**

**Оголошення міксину**

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

**Використання міксина**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Extend/Inheritance може виявитися корисним у випадках, коли властивості одного селектора потрібно поділити з іншим селектором. У наведеному нижче прикладі селектор *.error-notice* приймає всі властивості селектора *.error-text* і додає властивості рамки та відступу.

**Зухвалий**

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

Імпортування може бути корисним, якщо ви структуруєте свої стилі в різні файли на основі функціональності чи будь-якої іншої структури, якої ви дотримуєтесь. Ви можете імпортувати всі ці файли в основний файл SASS, який пізніше буде перетворено на CSS. Під час імпорту вам не потрібно вказувати розширення файлу в інструкції з імпорту. Sass компілює всі файли SASS безпосередньо. Щоб уникнути безпосередньої компіляції файлів імпорту, ви можете зробити їх частковими, додавши символ підкреслення (_) на початку їх назви. Часткові елементи імпортуються подібно до звичайних файлів Sass.

**Зухвалий**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Вихідний CSS матиме стилі з усіх імпортованих файлів.

## Посилання ##

- [Sass - Вікіпедія](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

