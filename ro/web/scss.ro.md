---
date: 2019-10-11
keywords: scss, .scss, format de fișier scss, cum se deschide fișiere scss, foaie de stil minunată din punct de vedere sintactic, preprocesor css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier SCSS - Sass Cascading Style Sheet
linktitle: SCSS
description: "Aflați despre formatul de fișier SCSS și despre API-urile care pot crea și deschide fișiere SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Ce este un fișier SCSS? ##

SCSS este a doua sintaxă a Sass (Syntactically Awesome Stylesheet) care folosește paranteze în loc de indentări. SCSS a fost proiectat în așa fel încât un fișier CSS3 valid să fie și un fișier SCSS valid. Fișierele SCSS sunt stocate cu extensia .scss.

## De ce să folosiți SCSS ##

Pe măsură ce design-urile site-urilor web devin complexe, rezultă fișiere [CSS](/ro/web/css/) mari. Astfel de fișiere sunt mai greu de întreținut. Aici intervine SCSS. SCSS introduce variabile, imbricare, mixuri, importuri și moștenire a selectorului în dezvoltarea CSS. Aceste completări fac lucrul cu designul mult mai distractiv.

## Cum se utilizează fișierele SCSS ##

Fișierele SCSS nu sunt incluse direct în documentul [HTML](/ro/web/html/), precum CSS. În schimb, fișierele SCSS sunt convertite în fișiere CSS care sunt incluse în fișierele HTML. Pentru a instala SCSS pe sistemul dvs., urmați instrucțiunile oferite pe [site-ul oficial Sass](https://sass-lang.com/install).
Pentru a converti SCSS în CSS, puteți fie să convertiți un fișier SCSS deja salvat, fie să urmăriți modificările și să le convertiți pe măsură ce fișierul este salvat. Comenzile pentru ambele sunt date mai jos.

### Convertiți o dată ###

Primul parametru este fișierul SCSS sursă, iar al doilea parametru este fișierul CSS de ieșire.

```cmd
sass main.scss main.css
```

### Urmăriți modificările ###

Comanda are un indicator suplimentar *watch** care menține comanda să ruleze și de îndată ce fișierul SCSS este salvat, este generată CSS de ieșire.

```cmd
sass --watch main.scss main.css
```

## Sintaxa SCSS ##

SCSS acceptă variabile, imbricare, mixin, importuri, moștenire selector, etc. Mai jos sunt date exemple ale acestor caracteristici.

### Variabile ###

Prin utilizarea variabilelor, puteți seta informații reutilizabile, cum ar fi culoarea primară sau culoarea de fundal pentru butonul de salvare. Acest lucru este util dacă trebuie să modificați aceste informații, doar o schimbați într-o locație și se actualizează oriunde este folosită.

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

**CSS generat**

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

### Cuibărire ###

Puteți imbrica selectoarele CSS similar cu ierarhia HTML. În exemplul de mai jos, intervalul este imbricat în interiorul blocului h1.

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

**CSS generat**

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

### Mixins ###

Mixinele pot fi folosite pentru a grupa proprietăți similare împreună care sunt utilizate împreună în mai multe locuri. De asemenea, puteți transmite parametri mixin-urilor.

**SCSS**

**Declararea unui mixin**

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

**Folosind un mixing**

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

**CSS generat**

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

### Extinde ###

Extindere/Moștenire este utilă în cazurile în care proprietățile unui selector trebuie să fie partajate cu un alt selector. În exemplul de mai jos, selectorul *.error-notice* preia toate proprietățile selectorului *.error-text* și adaugă proprietăți de chenar și de umplutură.

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

**CSS generat**

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

### Import ###

Importul poate fi util în separarea preocupărilor. Puteți împărți stilurile în așa fel încât stilurile de antet să fie într-un fișier separat, stilurile de subsol să fie într-un fișier separat, toate variabilele de culoare utilizate în stiluri să poată fi într-un fișier separat etc. Folosind această tehnică, stilurile rămân organizate. Doar importați fișierele din fișierul SCSS principal, așa cum se arată în exemplul de mai jos. Nu trebuie să specificați extensia fișierului în instrucțiunea de import. Sass compilează toate fișierele SCSS direct. Pentru a evita compilarea directă a fișierelor de import, le puteți face parțiale adăugând caractere de subliniere (_) înaintea numelui lor. Puteți importa parțiale similare fișierelor SCSS normale fără caracterul de subliniere.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Ieșirea CSS va avea stilurile din toate fișierele importate.

## Referințe ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

