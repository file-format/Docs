---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format pliku PYI — definicja interfejsu Pythona
linktitle: PYI
description: "Dowiedz się o formacie plików PYI i interfejsach API, które mogą tworzyć i otwierać pliki PYI."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Czym jest plik PYI?

Plik PYI to plik definicji interfejsu Pythona, który zawiera odniesienie do kodu pośredniczącego do implementacji interfejsu. Każdy moduł Pythona jest reprezentowany jako kod pośredniczący .pyi, który jest normalnym plikiem Pythona, ale z pustymi metodami. Składnia plików PYI jest taka sama jak zwykłego modułu Pythona. Implementacja pustych metod jest pozostawiona użytkownikowi końcowemu do osiągnięcia określonego celu, dla którego moduł jest napisany. W tym miejscu pliki PYI różnią się od plików [PY](/pl/programming/py/), które zawierają pełną implementację programu. Pliki PYI można otwierać za pomocą edytorów tekstu, takich jak Notatnik, Notepad ++, Microsoft Visual Studio Code i JetBrains PyCharm.

## Format pliku PYI

Pliki PYI są zapisywane jako zwykłe pliki tekstowe, które można otworzyć w dowolnym edytorze tekstu. Python to język interpretera, który sprawdza typ podczas wykonywania kodu. W takim przypadku pliki PYI są korzystne, ponieważ programiści mogą ręcznie definiować i sprawdzać typy modułów podczas pisania aplikacji.

## Bibliografia ##

* [Interfejsy — Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [Tłumacze PYM](https://github.com/interpreters/pym)

