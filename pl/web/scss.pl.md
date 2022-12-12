---
date: 2019-10-11
keywords: scss, .scss, format pliku scss, jak otwierać pliki scss, świetny składniowo arkusz stylów, preprocesor css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku SCSS — kaskadowy arkusz stylów Sass
linktitle: SCSS
description: "Dowiedz się więcej o formacie plików SCSS i interfejsach API, które umożliwiają tworzenie i otwieranie plików SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Czym jest plik SCSS? ##

SCSS to druga składnia Sass (Syntactically Awesome Stylesheet), która używa nawiasów zamiast wcięć. SCSS został zaprojektowany w taki sposób, że prawidłowy plik CSS3 jest również prawidłowym plikiem SCSS. Pliki SCSS są przechowywane z rozszerzeniem .scss.

## Dlaczego warto używać SCSS ##

Projekty stron internetowych stają się coraz bardziej złożone, co skutkuje dużymi plikami [CSS](/pl/web/css/). Takie pliki są trudniejsze w utrzymaniu. Tutaj wkracza SCSS. SCSS wprowadza zmienne, zagnieżdżanie, domieszki, importy i dziedziczenie selektorów w rozwoju CSS. Te dodatki sprawiają, że praca z projektowaniem jest o wiele przyjemniejsza.

## Jak korzystać z plików SCSS ##

Pliki SCSS nie są dołączane bezpośrednio do dokumentu [HTML](/pl/web/html/), tak jak CSS. Zamiast tego pliki SCSS są konwertowane na pliki CSS zawarte w plikach HTML. Aby zainstalować SCSS w swoim systemie, postępuj zgodnie z instrukcjami podanymi na [Oficjalnej stronie Sass](https://sass-lang.com/install).
Aby przekonwertować SCSS na CSS, możesz przekonwertować już zapisany plik SCSS lub obserwować zmiany i konwertować podczas zapisywania pliku. Polecenia dla obu podano poniżej.

### Konwertuj raz ###

Pierwszy parametr to źródłowy plik SCSS, a drugi parametr to wyjściowy plik CSS.

```cmd
sass main.scss main.css
```

### Uważaj na zmiany ###

Polecenie ma dodatkową flagę *watch**, która utrzymuje polecenie w działaniu, a gdy tylko plik SCSS zostanie zapisany, generowany jest wyjściowy CSS.

```cmd
sass --watch main.scss main.css
```

## Składnia SCSS ##

SCSS obsługuje zmienne, zagnieżdżanie, domieszki, importy, dziedziczenie selektorów itp. Poniżej podano przykłady tych funkcji.

### Zmienne ###

Za pomocą zmiennych można ustawić informacje wielokrotnego użytku, takie jak kolor podstawowy lub kolor tła dla przycisku zapisu. Jest to przydatne, jeśli chcesz zmienić te informacje, po prostu zmieniasz je w jednym miejscu i aktualizuje się tam, gdzie jest używany.

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

**Wygenerowany CSS**

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

### Zagnieżdżanie ###

Możesz zagnieżdżać selektory CSS podobnie jak w hierarchii HTML. W poniższym przykładzie rozpiętość jest zagnieżdżona w bloku h1.

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

**Wygenerowany CSS**

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

### Mieszanki ###

Domieszek można używać do grupowania podobnych właściwości, które są używane razem w wielu miejscach. Możesz także przekazywać parametry do miksów.

**SCSS**

**Deklaracja mieszania**

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

**Korzystanie z miksu**

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

**Wygenerowany CSS**

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

### Rozszerzyć ###

Rozszerzanie/dziedziczenie jest przydatne w przypadkach, gdy właściwości jednego selektora muszą być współdzielone z innym selektorem. W poniższym przykładzie selektor *.error-notice* przyjmuje wszystkie właściwości selektora *.error-text* i dodaje właściwości obramowania i wypełnienia.

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

**Wygenerowany CSS**

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

Importowanie może być przydatne w rozdzielaniu obaw. Style można podzielić w taki sposób, że style nagłówków znajdują się w osobnym pliku, style stopek w osobnym pliku, wszystkie zmienne kolorów użyte w stylach mogą znajdować się w osobnym pliku itp. Dzięki tej technice style pozostają uporządkowane. Wystarczy zaimportować pliki do głównego pliku SCSS, jak pokazano w poniższym przykładzie. Nie musisz określać rozszerzenia pliku w instrukcji importu. Sass bezpośrednio kompiluje wszystkie pliki SCSS. Aby uniknąć bezpośredniej kompilacji importowanych plików, możesz uczynić je częściowymi, dodając podkreślenie (_) przed ich nazwą. Możesz importować fragmenty podobne do normalnych plików SCSS bez podkreślenia.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Wyjściowy CSS będzie zawierał style ze wszystkich zaimportowanych plików.

## Bibliografia ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

