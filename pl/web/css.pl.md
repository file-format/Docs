---
date: 2019-10-11
keywords: css, .css, format pliku css, jak otwierać pliki css, kaskadowe arkusze stylów
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku CSS
linktitle: CSS
description: "Dowiedz się więcej o formacie plików CSS i interfejsach API, które umożliwiają tworzenie i otwieranie plików CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Co to jest plik CSS? ##

CSS (kaskadowe arkusze stylów) to pliki opisujące, w jaki sposób elementy HTML są wyświetlane na ekranie, papierze itp. Dzięki HTML można osadzać style lub definiować style w zewnętrznym arkuszu stylów. Aby osadzić style, \ <style>\</style> tagi są używane. Zewnętrzne arkusze stylów są przechowywane w plikach z rozszerzeniem .css. Dzięki zewnętrznemu CSS możesz umieścić go na wielu stronach HTML, aby zaktualizować styl tych stron. Nawet pojedynczy plik CSS może być użyty do nadania stylu całej stronie internetowej.

## Krótka historia ##

CSS1 został wydany w 1996 roku z Bertem Bosem jako współautorem. Grupa robocza CSS rozpoczęła pracę nad kwestiami, które nie zostały uwzględnione w CSS1. Doprowadziło to do stworzenia CSS2 w listopadzie 1997 r., które zostało opublikowane jako zalecenie W3C 12 maja 1998 r. Ta wersja dodała obsługę urządzeń specyficznych dla mediów, takich jak drukarki, pobieralne czcionki, tabele i pozycjonowanie elementów. W czerwcu 1999 CSS3 stał się rekomendacją W3C. To podzieliło dokumentację na moduły, gdzie każdy moduł miał funkcje rozszerzenia zdefiniowane w CSS2.

## Jak korzystać z plików CSS ##

Aby użyć pliku CSS, umieść go w sekcji head dokumentu HTML. Używasz tagu łącza, aby dołączyć plik, jak pokazano poniżej.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

atrybut *href* tagu link zawiera ścieżkę do pliku CSS. W ten sposób odpowiednie style zawarte w dołączonym pliku CSS są stosowane do dokumentu HTML.

## Składnia CSS ##

Reguła CSS składa się z dwóch komponentów, selektora i deklaracji. Selektor wskazuje element w dokumencie HTML. Może to być znacznik elementu, nazwa klasy, nazwa id, wiele znaczników pokazujących hierarchię itp. Deklaracja zawiera definicję stylu składającą się z właściwości i wartości. Właściwość identyfikuje właściwość elementu, który chcesz zmienić, a wartość określa jego nową wartość. Każda reguła CSS może mieć wiele deklaracji. Poniżej znajduje się przykład reguły CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

W powyższym przykładzie mamy **h1** jako selektor, który wybiera wszystkie znaczniki h1 w dokumencie HTML. Reguła ma dwie deklaracje, jedną dla font-weight, a drugą dla color. *font-weight* i *color* to właściwości, a *700* i *forestgreen* to odpowiednio ich wartości.

## Przykład użycia CSS ##

Poniżej przedstawiono przykładowy dokument HTML i arkusz stylów użyty do nadania mu stylu. Obraz porównawczy jest również dodawany w celu porównania stylizowanych i zwykłych dokumentów HTML

### Dokument HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Arkusz stylów CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Porównanie wyjścia ###

Po lewej stronie obrazu wyświetlany jest dokument HTML bez zastosowanych stylów, a po prawej dokument HTML z zastosowanymi stylami.

{{< figure src="../CssExample.jpg" alt="Przykładowy obraz" >}}

## Bibliografia ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

