---
date: 2019-10-11
keywords: step, .step, format pliku step, jak otwierać pliki step, rozszerzenie .step, rozszerzenie step
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku STEP
linktitle: STEP
description: "Dowiedz się więcej o formacie plików STEP i interfejsach API, które mogą tworzyć i otwierać pliki STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Czym jest plik STEP?

Plik STEP jest szeroko stosowanym formatem wymiany danych w projektowaniu wspomaganym komputerowo (CAD). Został znormalizowany w 1994 roku przez komitet ISO pod nazwą „ISO 10303-21”. ISO 10303-21 definiuje mechanizm kodowania reprezentacji danych w języku modelowania danych EXPRESS. Plik STEP jest również znany jako plik p21 i plik fizyczny STEP. Rozszerzenia plików używane dla pliku STEP to .stp i .step.

## Historia podstawowa

W 1994 roku wydano oryginalną specyfikację Part 21. Zawiera pewne błędy, które zostały poprawione w sprostowaniu technicznym wydanym w 1996 r. Drugie wydanie zostało opublikowane w 2002 r. i zawierało sprostowanie i rozszerzenia kilku sekcji danych. Trzecia edycja została opublikowana w 2016 roku i dodała sekcje zakotwiczenia i odniesienia, które umożliwiły przechowywanie jednostek i wartości w plikach zewnętrznych. Dodano obsługę UTF-8 ciągów znaków. Dodano podpisy cyfrowe, aby zweryfikować zawartość pliku i zweryfikować poświadczenia. Dodano również obsługę kompresji i przechowywania struktury wymiany przy użyciu ZIP.

## Format pliku STEP

Format zwykłego tekstu dla pliku STEP składa się z sekwencji rekordów. Zestaw znaków jest zdefiniowany jako punkty kodowe ISO 10646. „ISO-10303-21;” to pierwsze znaki w pierwszym rekordzie. Komentarze są otoczone znakami „/*” i „*/”. Ostatni rekord zawiera „END-ISO-10303-21;” czy plik STEP jest zgodny z wersją 2002. W przypadku zgodności z wersją 2016 po „END-ISO-10303-21” może znajdować się jeden lub więcej podpisów cyfrowych; terminator. Podziały wierszy są oznaczone przez „\N\”, a podziały stron przez „\F\”.

Plik STEP jest podzielony na sekcje, a ich nazwy są terminami zastrzeżonymi. Wszystkie sekcje kończą się zapisem „ENDSEC” i muszą być w kolejności pokazanej poniżej.

- **NAGŁÓWEK**: To jest obowiązkowa i niepowtarzalna sekcja. Składa się z następujących podmiotów:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Jest to opcjonalna, nie powtarzająca się sekcja, która została wprowadzona w wersji 2016. Definiuje zewnętrzne nazwy instancji, aby można było się do nich odwoływać.
- **REFERENCE**: Jest to opcjonalna, nie powtarzająca się sekcja, która została również wprowadzona w wersji 2016. Każdy wpis w tej sekcji wiąże nazwę instancji wpisu/wartości z instancją/wartością w pliku zewnętrznym.
- **DANE**: Jest to opcjonalna, powtarzalna sekcja zawierająca podstawową zawartość instancji modelu.
- **SIGNATURE**: Jest to opcjonalna powtarzalna sekcja, która została wprowadzona w wersji 2016. Przechowuje podpis cyfrowy w celu weryfikacji zawartości pliku lub potwierdzenia poświadczeń.

## Bibliografia

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

