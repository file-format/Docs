---
date: 2019-10-11
keywords: js, .js, format pliku js, jak otwierać pliki js, pliki javascript
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku JS
linktitle: JS
description: "Dowiedz się więcej o formacie plików JS i interfejsach API, które umożliwiają tworzenie i otwieranie plików JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Czym jest plik JSZ? ##

JS (JavaScript) to pliki zawierające kod JavaScript do wykonania na stronach internetowych. Pliki JavaScript są przechowywane z rozszerzeniem .js. W dokumencie [HTML](/pl/web/html/) możesz osadzić kod JavaScript za pomocą \ <script>\</script> tagi lub dołączyć plik JS. Podobnie jak pliki [CSS](/pl/web/css/), pliki JS można dołączać do wielu dokumentów HTML w celu ponownego wykorzystania kodu. JavaScript może być używany do manipulowania HTML DOM.

## Krótka historia ##

JavaScript został po raz pierwszy dostarczony jako część przeglądarki Navigator we wrześniu 1995 roku pod nazwą LiveScript przez firmę Netscape. Został przemianowany na JavaScript trzy miesiące później. W 1996 roku Microsoft dokonał inżynierii wstecznej interpretera Navigatora, aby stworzyć JScript. JScript został wydany wraz z Internet Explorerem i bardzo różnił się od JavaScript.

Netscape przesłał JavaScript do ECMA International, co doprowadziło do oficjalnego wydania pierwszej specyfikacji ECMAScript w 1997 r. ECMAScript 2 został wydany w 1998 r., ECMAScript 3 w 1999 r., a prace nad ECMAScript 4 rozpoczęły się w 2000 r., ale nigdy nie przyniosły rezultatu.

Jesse James Garrett w 2005 roku opublikował białą księgę, w której ukuł termin *Ajax*. To wykorzystywało JavaScript jako podstawę do tworzenia aplikacji internetowych, które ładowały dane w tle i unikały ponownego ładowania całej strony. Doprowadziło to do powstania bibliotek takich jak JQuery, Prototype, Dojo itp.

Firma Google wypuściła przeglądarkę Chrome z silnikiem JavaScript V8 w 2008 roku. Na początku 2009 roku zawarto porozumienie w sprawie połączenia wszystkich istotnych prac i rozwoju JavaScript. Doprowadziło to do wydania standardu ECMAScript 5 w grudniu 2009 roku.

## Jak korzystać z plików JS ##

Aby użyć pliku JS, należy dołączyć go do dokumentu HTML. Używasz tagu łącza, aby dołączyć plik, jak pokazano poniżej.

```html
<script src="site.js"></script>
```

Atrybut *src* znacznika *script* zawiera ścieżkę do pliku JS. W ten sposób funkcjonalność JS jest dodawana do dokumentu HTML.

## Składnia JS ##

Pliki JavaScript mogą zawierać zmienne, operatory, funkcje, warunki, pętle, tablice, obiekty itp. Poniżej znajduje się krótki przegląd składni JavaScript.

- Każde polecenie kończy się średnikiem (;).
- Użyj słowa kluczowego *var*, aby zadeklarować zmienne.
- Obsługuje operatory arytmetyczne ( + - * / ) do obliczania wartości.
- Komentarze jednowierszowe są dodawane za pomocą //, a komentarze wielowierszowe są otoczone znakami /* i */.
- We wszystkich identyfikatorach rozróżniana jest wielkość liter, np. *modelNo* i *modelno* to dwie różne zmienne.
- Funkcje są definiowane za pomocą słowa kluczowego *function*.
- Tablice można definiować za pomocą nawiasów kwadratowych [].
- JS obsługuje operatory porównania, takie jak ==, != , >=, !== itp.
- Klasy można definiować za pomocą słowa kluczowego *class*.

## Przykład użycia JS ##

Poniżej przedstawiono przykład prostego użycia pliku JavaScript.

### Dokument HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Kod JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Bibliografia ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

