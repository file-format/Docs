---
date: 2019-10-11
keywords: kt, .kt, format pliku kotlin, jak otwierać pliki kotlin, jak uruchamiać pliki kotlin, format pliku .kt, plik kt, rozszerzenie pliku kotlin, rozszerzenie .kt, kotlin vs java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku KT
linktitle: KT
description: "Dowiedz się o formacie pliku KT i interfejsach API, które mogą tworzyć i otwierać pliki KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Czym jest plik KKT? ##

Kod źródłowy napisany w Kotlinie jest zapisywany z rozszerzeniem .kt, które jest powszechnie znane jako **rozszerzenie pliku Kotlin**. Kotlin to wieloplatformowy język programowania ogólnego przeznaczenia opracowany przez JetBrains w celu pełnej współpracy z [Java](/pl/programming/java/). Znak towarowy Kotlin jest chroniony przez Fundację Kotlin.

Kotlin został ogłoszony przez Google jako preferowany język programowania do tworzenia aplikacji na Androida 7 maja 2019 r. Android Studio 3.0 zaczęło obsługiwać Kotlin jako alternatywę dla tworzenia aplikacji na Androida w październiku 2017 r.

## Krótka historia formatu pliku Kotlin KT##

Kotlin został zaprezentowany przez JetBrains w lipcu 2011 roku jako nowy język programowania dla JVM. Kierownik JetBrains, Dmitry Jemerov, powiedział, że w większości języków brakowało funkcji, których szukali, z wyjątkiem Scali, ale powolna kompilacja Scali była wadą. Jednym z głównych celów Kotlina była kompilacja tak szybka jak Java. Projekt Kotlin został otwarty na licencji Apache 2 w lutym 2012 roku.

Wersja 1.0 Kotlina została wydana 15 lutego 2015 r. Android ogłosił pierwszorzędne wsparcie dla Kotlina na Androida podczas Google I / O 2017. Kotlin 1.2 został wydany 28 listopada 2017 r. Z możliwością współdzielenia kodu między platformami JVM i JavaScript. Kotlin 1.3 został wydany 29 października 2018 roku ze wsparciem dla programowania asynchronicznego. Google ogłosił Kotlin jako preferowany język programowania do tworzenia aplikacji na Androida 7 maja 2019 r. Kotlin 1.4 został wydany w sierpniu 2020 r. Z niewielkimi zmianami w celu obsługi interoperacyjności z Swift / Objective-C.

## Składnia Kotlina ##

Kotlin został zaprojektowany tak, aby był lepszy niż Java, ale nadal współpracował z kodem Java, aby umożliwić stopniową migrację z Javy do Kotlina.

* Średniki są opcjonalne w Kotlinie. Nowa linia wystarczy, aby wskazać koniec instrukcji.
* Kotlin obsługuje dwa typy zmiennych, tylko do odczytu, zdefiniowane przez słowo kluczowe *val* i zmienne, zdefiniowane przez słowo kluczowe *var*.
* Zajęcia są domyślnie prywatne i ostateczne. Aby wywodzić się z klasy, klasa bazowa musi zostać zadeklarowana za pomocą słowa kluczowego *open*.
* Kotlin obsługuje również programowanie proceduralne.
* Punktem wejścia do programu Kotlin jest „główna” funkcja podobna do Javy, C# itp.

### Przykład składni ###

Poniżej znajduje się przykład składni Kotlina.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

W powyższym kodzie słowo kluczowe **fun** definiuje funkcję o nazwie main. Wewnątrz funkcji za pomocą słowa kluczowego **val** deklarowana jest zmienna tylko do odczytu 'audience'. Za pomocą metody **println** na konsoli zostanie wydrukowany komunikat „Hello World from Kotlin”. Wartość zmiennej Audience jest wstrzykiwana do łańcucha ze znakiem **$**.

## Kotlin kontra Java
Kotlin jest oficjalnym językiem do pisania aplikacji na Androida i oferuje wiele zaawansowanych funkcji, ale wielu doświadczonych programistów Java wciąż nie wykazuje zainteresowania przejściem na Kotlin. Myślą, że wszystko mogą zrobić tylko z Javą. Poniżej znajduje się porównanie dwóch technologii, które mogą przekonać programistów Java do zmiany:

| Parametr | Jawa | Kotlin |
|--------------------|-----------|---------------- -|
| Singletony Obiekty | √ | √ |
| Typy symboli wieloznacznych | √ | Χ |
| Kompilacja | Kody bajtowe | Maszyna wirtualna |
| Wyrażenie lambda | Χ | √ |
| niezmienna tablica | Χ | √ |
| Pola nieprywatne | √ | Χ |
| Inteligentne rzuty | Χ | √ |
| Zerowe bezpieczeństwo | Χ | √ |
| Członkowie statyczni | √ | Χ |

## Bibliografia ##

- [Kotlin (język programowania) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(język_programowania))

