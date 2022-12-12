{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "Plik modułu Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Plik Javascript modułu Node.js ES",
  "description" :"Dowiedz się, co to jest plik MJS i interfejsy API, które mogą tworzyć i otwierać plik MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Czym jest plik MJS?

Plik z rozszerzeniem .mjs to plik kodu źródłowego JavaScript, który jest używany jako moduł ECMA (moduł ECMAScript) w aplikacjach Node.js. Systemem modułów natvie Node.js jest CommonJS, który jest używany do dzielenia kodu na różne pliki, aby utrzymać porządek w kodzie [JS](/pl/web/js/). MJS to jedyny sposób używany przez Node.js do określenia, czy moduł to CommonJS, czy ES6. Moduły ECMAScript to standardowa forma pakowania kodu JavaScript do ponownego wykorzystania. Pliki MJS można otwierać w edytorach tekstu, takich jak Atom, Vim, Apple xCode, Microsoft Visual Studio i Notatnik.

## Format pliku MJS — więcej informacji

Pliki MJS są zapisywane na dysku jako zwykły format tekstowy w składni JavaScript. Można je otworzyć w dowolnym edytorze tekstu i są one czytelne dla człowieka. Od 2018 roku prawie wszystkie główne przeglądarki obsługują teraz moduły ES.

## Różnice między modułami ES a CommonJS

Co sprawia, że pliki MJS różnią się od zwykłych plików JS? Różnicę między modułami ES a CommonJS można podsumować w następujący sposób:

* Nie wymagaj, eksportu ani modułu. eksportu
* Brak \__nazwapliku lub \__nazwakatalogu
* Brak ładowania modułu JSON
* Brak ładowania modułu natywnego
* Nie wymagaj rozwiązania
* Brak ŚCIEŻKI_WĘZŁA
* Brak wymaganych rozszerzeń
* Nie wymaga pamięci podręcznej

## Bibliografia

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Różnica między JS a MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

