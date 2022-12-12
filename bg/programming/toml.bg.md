---
date: 2019-10-11
keywords: toml, .toml, файлов формат toml, как да отваряте toml файлове, разширение .toml, разширение toml
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Файлов формат TOML
linktitle: TOML
description: "Научете за файловия формат TOML и API, които могат да създават и отварят TOML файлове."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Какво е TOML файл? ##

TOML (Tom's Obvious Minimal Language) е минимален конфигурационен файлов формат, който използва разширението .toml. TOML има за цел да бъде лесен за четене, да се съпоставя недвусмислено с речници и да бъде лесен за анализиране на различни структури от данни. TOML има спецификация с отворен код, която получи принос от общността. TOML се поддържа от много програмни езици като C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift и др. Типът MIME за TOML файлове е *application/toml*.


## TOML файлов формат ##

TOML файловете се състоят главно от двойки ключ/стойност, секции/таблици, коментари и трябва да бъдат валиден UTF-8 кодиран Unicode документ. TOML поддържа типове данни String, Integer, Float, Boolean, Datetime, Array и Table (хеш таблица/речник). TOML е език, чувствителен към малки и големи букви.

### Синтаксис ###

- **Двойки ключ-стойност**: Двойките ключ-стойност са разделени със знак за равенство (=). Всяка двойка трябва да е на нов ред.

``` toml
първо = "Том"
последно = "Престън-Вернер"
```

- **Коментари**: Коментарите започват със символа решетка (#).

``` toml
# Това е TOML документ.
```

- **Низове**: Низовете са заобиколени от кавички (").

``` toml
string = "Примерен низ"
```

- **Многоредови низове**: Многоредовите низове са заобиколени от три кавички („““).

``` toml
[домашен адрес]
улица = """123 Торнадо алея
Апартамент 16"""
град = "Източен Сентървил"
състояние = "KS"
```

- **Цели числа/плаващи числа**

``` toml
цяло число = 20
float = 20,5
```

- **Булеви стойности**: Булевите стойности винаги са с малки букви.

``` toml
bool1 = вярно
bool2 = невярно
```

- **Дата-час**: За DateTime можете да използвате форматирана дата-час в RFC 3339, както е показано в примера по-долу.

``` toml
отместване_дата_час = 1979-05-27 07:32:00Z
локална_дата_час = 1979-05-27T07:32:00
местна_дата = 1979-05-27
местно_време = 07:32:00
```

- **Масиви**: Масивите са оградени с квадратни скоби с елементи, разделени със запетаи (,).

``` toml
цветове = [ "червено", "жълто", "зелено" ]
```

- **Таблици**: Таблиците са колекции от двойки ключ/стойност, които се определят от заглавки на нов ред, оградени с квадратни скоби ([]). Таблицата завършва, когато се предостави нов хедър или когато файлът свърши.

``` toml
[домашен адрес]
улица = """123 Торнадо алея
Апартамент 16"""
град = "Източен Сентървил"
състояние = "KS"

[офис адрес]
улица = """123 Торнадо алея
Апартамент 16"""
град = "Източен Сентървил"
състояние = "KS"
```

Вградените таблици са оградени с фигурни скоби ({}), като всяка двойка ключ/стойност е разделена със запетая (,).

``` toml
име = { първо = "Том", последно = "Пит" }
```

## Препратки ##

– [TOML – Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)
