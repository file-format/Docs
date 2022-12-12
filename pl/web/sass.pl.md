---
date: 2019-10-11
keywords: sass, .sass, format pliku sass, jak otwierać pliki sass, świetny składniowo arkusz stylów, preprocesor css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku Sass
linktitle: Sass
description: "Dowiedz się o formacie plików Sass i interfejsach API, które mogą tworzyć i otwierać pliki Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Czym jest plik SASS? ##

Sass (składniowo niesamowite arkusze stylów) to język skryptowy preprocesora. Jest kompilowany do [CSS](/pl/web/css/) i przechowywany z rozszerzeniem .sass. Sass składa się z dwóch składni, oryginalnej opartej na wcięciach, która wykorzystuje rozszerzenie .sass, oraz nowszej SCSS z formatowaniem blokowym, takim jak CSS, która wykorzystuje rozszerzenie .scss.

## Dlaczego warto używać Sass ##

Sass jest naprawdę pomocny w utrzymywaniu stylów, ponieważ zapewnia wiele funkcji, takich jak wprowadzanie zmiennych, zagnieżdżanie, domieszki, importy i dziedziczenie selektorów, dzięki którym praca ze stylami jest przyjemna.

## Jak korzystać z plików SASS ##

Pliki SASS nie są dołączane bezpośrednio do dokumentu [HTML](/pl/web/html/), ale są konwertowane na pliki CSS zawarte w plikach HTML. Możesz zainstalować Sass w swoim systemie, postępując zgodnie z instrukcjami podanymi na [Oficjalnej stronie Sass](https://sass-lang.com/install).

Sass można przekonwertować na CSS, konwertując już zapisany plik SASS lub obserwując zmiany i konwertując podczas zapisywania pliku. Polecenia dla obu podano poniżej.

### Konwertuj raz ###

Pierwszym parametrem polecenia jest źródłowy plik SASS, a drugim parametrem wyjściowy plik CSS.

```cmd
sass main.sass main.css
```

### Uważaj na zmiany ###

Powyższe polecenie można uruchomić z dodatkową flagą *watch*, która utrzymuje działanie polecenia i gdy tylko plik Sass zostanie zapisany, generowany jest wyjściowy CSS.

```cmd
sass --watch main.sass main.css
```

## Składnia Sass ##

Sass obsługuje zmienne, zagnieżdżanie, domieszki, importy, dziedziczenie selektorów itp. Poniżej podano przykłady tych funkcji.

### Zmienne ###

Zmiennych można używać do ustawiania informacji wielokrotnego użytku, takich jak kolor podstawowy lub dopełnienie przycisku. Może się to okazać przydatne, jeśli w przyszłości będziesz musiał zmienić te informacje, po prostu zmienisz je w jednym miejscu i zostaną one zaktualizowane wszędzie.

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

Selektory CSS można zagnieżdżać podobnie do hierarchii HTML. W poniższym przykładzie zakres jest zagnieżdżony w bloku h1.

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

Domieszki służą do grupowania podobnych właściwości, które są używane w wielu miejscach. Mixiny obsługują również parametry.

**Sass**

**Deklaracja mieszania**

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

**Korzystanie z miksu**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Rozszerzanie/dziedziczenie może okazać się przydatne w przypadkach, gdy właściwości jednego selektora muszą być współdzielone z innym selektorem. W poniższym przykładzie selektor *.error-notice* przyjmuje wszystkie właściwości selektora *.error-text* i dodaje właściwości obramowania i wypełnienia.

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

Importowanie może być przydatne, jeśli uporządkujesz swoje style w różne pliki w oparciu o funkcjonalność lub inną strukturę, którą stosujesz. Możesz zaimportować wszystkie te pliki w podstawowym pliku SASS, który jest później konwertowany na CSS. Podczas importu nie trzeba podawać rozszerzenia pliku w instrukcji importu. Sass bezpośrednio kompiluje wszystkie pliki SASS. Aby uniknąć bezpośredniej kompilacji importowanych plików, możesz uczynić je częściowymi, dodając podkreślenie (_) na początku ich nazwy. Częściowe są importowane podobnie jak zwykłe pliki Sass.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Wyjściowy CSS będzie zawierał style ze wszystkich importowanych plików.

## Bibliografia ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

