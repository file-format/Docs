---
date: 2019-10-11
keywords: sass, .sass, format de fișier sass, cum se deschide fișiere sass, foaie de stil minunată din punct de vedere sintactic, preprocesor css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier Sass
linktitle: Sass
description: "Aflați despre formatul de fișier Sass și despre API-urile care pot crea și deschide fișiere Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Ce este un fișier SASS? ##

Sass (foile de stil extraordinare din punct de vedere sintactic) este un limbaj de scriptare preprocesor. Este compilat în [CSS](/ro/web/css/) și este stocat cu extensia .sass. Sass este format din două sintaxe, originalul bazat pe indentări care utilizează extensia .sass și SCSS mai nou cu formatare bloc, cum ar fi CSS, care utilizează extensia .scss.

## De ce să folosiți Sass ##

Sass este foarte util în menținerea stilurilor, deoarece oferă multe caracteristici, cum ar fi introducerea de variabile, imbricarea, mixurile, importurile și moștenirea selectorului, care fac să lucreze cu stiluri distractiv.

## Cum se utilizează fișierele SASS ##

Fișierele SASS nu sunt incluse direct în documentul [HTML](/ro/web/html/), ci sunt mai degrabă convertite în fișiere CSS care sunt incluse în fișierele HTML. Puteți instala Sass pe sistemul dumneavoastră urmând instrucțiunile oferite pe [site-ul oficial Sass](https://sass-lang.com/install).

Sass poate fi convertit în CSS fie prin conversia unui fișier SASS deja salvat, fie prin urmărirea modificărilor și conversia pe măsură ce fișierul este salvat. Comenzile pentru ambele sunt date mai jos.

### Convertiți o dată ###

Primul parametru al comenzii este fișierul SASS sursă, iar al doilea parametru este fișierul CSS de ieșire.

```cmd
sass main.sass main.css
```

### Urmăriți modificările ###

Comanda de mai sus poate fi rulată cu un semnal suplimentar *watch* care menține comanda rulată și de îndată ce fișierul Sass este salvat, este generată CSS de ieșire.

```cmd
sass --watch main.sass main.css
```

## Sintaxa Sass ##

Sass acceptă variabile, imbricare, mixuri, importuri, moștenire selector, etc. Mai jos sunt prezentate exemple ale acestor caracteristici.

### Variabile ###

Variabilele pot fi folosite pentru a seta informații reutilizabile, cum ar fi culoarea primară sau umplutura pentru un buton. Acest lucru se poate dovedi util dacă în viitor ai nevoie să schimbi acele informații, doar le schimbi într-o singură locație și se actualizează peste tot.

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

Selectoarele CSS pot fi imbricate similar cu ierarhia HTML. În exemplul următor, intervalul este imbricat în interiorul blocului h1.

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

Mixinele sunt folosite pentru a grupa proprietăți similare împreună care sunt utilizate în mai multe locuri. Mixinele acceptă și parametrii.

**Sass**

**Declararea unui mixin**

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

**Folosind un mixing**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Extinderea/Moștenirea se poate dovedi a fi utilă în cazurile în care proprietățile unui selector trebuie să fie partajate cu un alt selector. În exemplul de mai jos, selectorul *.error-notice* preia toate proprietățile selectorului *.error-text* și adaugă proprietăți de chenar și de umplutură.

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

Importarea poate fi utilă dacă vă structurați stilurile în fișiere diferite pe baza funcționalității sau a oricărei alte structuri pe care o urmați. Puteți importa toate aceste fișiere într-un fișier SASS primar care este ulterior convertit în CSS. În timpul importului, nu trebuie să specificați extensia fișierului în instrucțiunea de import. Sass compilează toate fișierele SASS direct. Pentru a evita compilarea directă a fișierelor de import, le puteți face parțiale adăugând caractere de subliniere (_) la începutul numelui lor. Parțialele sunt importate similar fișierelor Sass normale.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Ieșirea CSS va avea stilurile din toate fișierele importate.

## Referințe ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

