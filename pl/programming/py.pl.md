---
date: 2019-10-11
keywords: py, python, .py, format pliku py, jak otworzyć plik py, jak uruchomić pliki py, jak uruchomić pliki python, jak uruchomić python
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku PY
linktitle: PY
description: "Dowiedz się więcej o formacie plików PY i interfejsach API, które umożliwiają tworzenie i otwieranie plików PY."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Czym jest plik PY? ##

Pliki z rozszerzeniem .py zawierają kod źródłowy Pythona. Język Python stał się bardzo znanym językiem od kilku dni. Może być używany do pisania skryptów systemowych, tworzenia stron internetowych i oprogramowania oraz matematyki. Python obsługuje kompatybilność między platformami; oznacza, że tworzone aplikacje w Pythonie mogą działać na różnych platformach, takich jak Windows, MAC, Linux, Raspberry Pi itp. Python zapewnia prostą i czytelną składnię, która jest podobna do języka angielskiego. Deweloperzy mogą napisać rozsądną aplikację, pisząc kilka wierszy kodu w Pythonie. Ponieważ Python działa w systemie interpretera, więc kod można wykonać natychmiast po jego napisaniu, co czyni go bardzo dobrym do prototypowania.

## Krótka historia ##

Python został wymyślony pod koniec lat 80. przez Guido van Rossuma jako następca języka programowania ABC. Jego wdrożenie rozpoczęło się w grudniu 1989 roku, a jedynym głównym deweloperem był Van Rossum. Pracował nad pythonem do 12 lipca 2018 r. W styczniu 2019 r. aktywni programiści rdzenia Pythona wybrali pięcioosobową „Radę Sterującą”, w skład której weszli Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw i Van Rossum do kierowania projektem.

### Wersje ###

- Python 2.0 został wydany 16 października 2000 roku.
- Python 3.0 został wydany 3 grudnia 2008 roku.

## Jak uruchomić plik py ##

Aby sprawdzić zainstalowaną wersję Pythona, możesz użyć następującego polecenia:

```cmd
python --version
```

Spowoduje to wyświetlenie wersji na konsoli

```cmd
Python 3.7.4
```

Jeśli Python nie jest zainstalowany na twoim komputerze, możesz przejść do [python.org](https://www.python.org/) i pobrać i zainstalować Pythona dla odpowiedniego systemu operacyjnego.

Aby wykonać skrypt w języku Python, możesz użyć następującego polecenia:

```cmd
python helloworld.py
```

*helloworld.py* to plik skryptu zawierający następujący kod

```py
print("Hello World from Python")
```

Spowoduje to wydrukowanie następujących informacji w oknie konsoli.

```cmd
Hello World from Python
```

Uwaga: jeśli używasz IDE, zapewniają one przyciski na ekranie lub różne skróty klawiaturowe do uruchamiania Pythona. Na przykład przycisk odtwarzania jest wyświetlany w rynnie z edytorem w PyCharm, który umożliwia wykonanie skryptu Pythona.

## Format pliku PY ##

Python został zaprojektowany z myślą o czytelności i ma podobieństwa do języka angielskiego i matematyki. Python używa nowych wierszy, aby wskazać całe polecenie, w przeciwieństwie do średników lub nawiasów używanych w innych językach. W przypadku zakresów, pętli i funkcji Python opiera się na wcięciach i białych znakach, w przeciwieństwie do nawiasów klamrowych używanych w innych językach.

### Składnia ###

Poniżej znajduje się przykład składni języka Python.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Bibliografia ##

- [Python (język programowania) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

