---
date: 2019-10-11
keywords: json, .json, format pliku json, jak otwierać pliki json, notacja obiektowa javascript, format danych json, format pliku .json
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku JSON - Co to jest plik JSON?
linktitle: JSON
description: "Dowiedz się więcej o formacie pliku JSON i interfejsach API, które umożliwiają tworzenie i otwieranie plików JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Czym jest plik JSON?

JSON (JavaScript Object Notation) to otwarty standardowy format plików do udostępniania danych, który wykorzystuje tekst czytelny dla człowieka do przechowywania i przesyłania danych. Pliki JSON są przechowywane z rozszerzeniem .json. JSON wymaga mniej formatowania i jest dobrą alternatywą dla [XML](/pl/web/xml/). JSON wywodzi się z języka JavaScript, ale jest formatem danych niezależnym od języka. Generowanie i parsowanie JSON jest obsługiwane przez wiele współczesnych języków programowania. *application/json* to typ nośnika używany w przypadku formatu JSON.

## Format pliku JSON — krótka historia

Zaistniała potrzeba komunikacji między serwerem a klientem w czasie rzeczywistym, która doprowadziła do stworzenia formatu JSON. Format JSON został po raz pierwszy określony przez Douglasa Crockforda w marcu 2001 r. JSON był oparty na standardzie ECMA-262, wydanie 3 — grudzień 1999 r., który jest podzbiorem języka JavaScript.

Pierwsza edycja standardu JSON ECMA-404 została opublikowana w październiku 2013 r. przez firmę Ecma International. RFC 7159 stał się głównym punktem odniesienia dla zastosowań internetowych JSON w 2014 r. W listopadzie 2017 r. ISO / IEC 21778: 2017 został opublikowany jako międzynarodowy standard. RFC 8259 został opublikowany 13 grudnia 2017 r. przez The Internet Engineering Task Force, który jest aktualną wersją standardu internetowego STD 90.

## Struktura pliku JSON

Dane JSON są zapisywane w parach **klucz/wartość**. Klucz i wartość są oddzielone dwukropkiem (:) w środku z kluczem po lewej i wartością po prawej. Różne pary klucz/wartość są oddzielone przecinkiem (,). Kluczem jest ciąg ujęty w podwójne cudzysłowy, na przykład „nazwa”. Wartości mogą być następujących typów.

- `Liczba`
- `String`: Sekwencja znaków Unicode ujęta w podwójne cudzysłowy.
- `Boolean`: Prawda lub Fałsz.
- `Tablica`: Na przykład lista wartości ujęta w nawiasy kwadratowe

```json
[ „Jabłko”, „Banan”, „Pomarańczowy” ]
```

- `Obiekt`: Na przykład kolekcja par klucz/wartość otoczona nawiasami klamrowymi

```json
{"name": "Jack", "wiek": 30, "ulubionySport": "Piłka nożna"}
```

Obiekty JSON można również zagnieżdżać w celu reprezentowania struktury danych. Poniżej podano przykład obiektu JSON.

### Przykład formatu JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Jaki jest maksymalny rozmiar pliku JSON?

Praktycznie nie ma ograniczeń co do maksymalnego rozmiaru pliku JSON. Może być tak długa, jak przestrzeń wymagana do przechowywania zawartości.

Jeśli chodzi o wykorzystanie formatu pliku JSON do przesyłania danych przez Internet, należy uważać na dostępne zasoby komputera. Jeśli przesyłane są duże dane JSON, transfer zostanie zakłócony, jeśli przeglądarka klienta ma ograniczoną pamięć.


Nie ma sztywnego limitu określonego przez specyfikację, ale musisz uważać, aby nie wyczerpać zasobów na komputerach użytkowników, ponieważ szybko pogorszy to ich komfort użytkowania i prawdopodobnie porzucą Twoją aplikację.

## JSON kontra XML

**XML** to kolejny popularny i szeroko stosowany format plików do wymiany danych przez Internet. Jeśli chodzi o wymianę danych pomiędzy aplikacjami, programiści mają możliwość korzystania zarówno z formatów plików XML, jak i JSON. Jednak JSON jest najwygodniejszym sposobem wymiany danych między aplikacjami przez Internet z następujących powodów.

1. JSON zapewnia przejrzysty i łatwiejszy do odczytania widok danych w porównaniu do formatów plików XML
1. JSON zmniejsza narzut związany z przesyłaniem danych przez Internet, ponieważ ma mniej znaków do zdefiniowania tego samego zestawu danych w porównaniu z XML
1. Nowoczesne języki programowania zapewniają wbudowane parsery do analizowania odpowiedzi JSON przez Internet.

## Czy wiedziałeś?

Możesz zostać współtwórcą w FileFormat.com, aby społeczność formatów plików była na bieżąco ze swoimi odkryciami. Jeśli chcesz podzielić się czymś na temat formatów JSON lub plików internetowych, możesz opublikować swoje odkrycia w sekcji [Wiadomości dotyczące formatu plików internetowych](https://news.fileformat.com/t/Web), aby ludzie mogli dowiedzieć się więcej z nich.

## Bibliografia

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Wprowadzenie do formatu JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

