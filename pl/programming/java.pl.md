---
date: 2019-10-11
keywords: java, .java, format pliku java, jak otwierać pliki java, jak uruchamiać pliki java, plik java, przykładowy kod java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku Java
linktitle: Java
description: "Dowiedz się więcej o formacie plików Java i interfejsach API, które umożliwiają tworzenie i otwieranie plików Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Co to jest plik Java? ##
Plik zawierający kod źródłowy Java i zapisany z rozszerzeniem pliku .java jest znany jako plik Java. Java jest jedną z najczęściej używanych technologii do tworzenia gier, aplikacji mobilnych, internetowych i stacjonarnych. Ponieważ Java jest niezależna od platformy, działa bezbłędnie w systemach Windows, Mac, Linux, Raspberry Pi itp. Java jest bardzo podobna do C# i C++, więc łatwiej jest przełączać się między tymi językami.

## Krótka historia ##

Projekt Java został zainicjowany w czerwcu 1991 roku przez Jamesa Goslinga, Mike'a Sheridana i Patricka Naughtona. Java początkowo nosiła nazwę Oak. Później przemianowano go na Green, a ostatecznie na Java. James Gosling zaprojektował Javę ze składnią podobną do C/C++. Pierwsza publiczna wersja Javy została wydana w 1996 roku przez firmę Sun Microsystems. Mogła działać na wszystkich popularnych systemach, co spowodowało, że Java szybko stała się popularna. Wraz z wydaniem Java 2 w grudniu 1998 r. zbudowano wiele konfiguracji dla różnych typów platform. Wersje były następujące

- J2EE (Java EE): dla rozwiązań dla przedsiębiorstw
- J2ME (Java ME): dla aplikacji mobilnych
- J2SE (Java SE): dla aplikacji komputerowych

19 listopada 2006 r. Firma Sun udostępniła wirtualną maszynę Java (JVM) jako bezpłatne oprogramowanie typu open source. Po tym, jak Oracle Corporation przejęła Sun Microsystems w latach 2009–2010, James Gosling zrezygnował z Oracle 2 kwietnia 2010 r.

## Jak uruchomić/wykonać kod Java ##

Aby wykonać kod Java, należy go najpierw skompilować. Do tego wymagany jest Java SDK. Java SDK kompiluje kod Java do pliku klasy kodu bajtowego. Istnieją IDE, takie jak Eclipse i IntelliJ Idea, które ułatwiają pracę z plikami Java, zapewniając uzupełnianie kodu i łatwy w użyciu interfejs do kompilowania i wykonywania kodu Java.

## Format pliku Java ##

Na składnię Javy duży wpływ miały C i C++, ale w przeciwieństwie do C++, Java została zbudowana prawie wyłącznie jako język obiektowy. W Javie cały kod jest zapisywany wewnątrz klas, a każdy element danych jest obiektem. W przeciwieństwie do C++, Java nie obsługuje przeciążania operatorów ani wielokrotnego dziedziczenia.

### Przykładowy kod Java ###

Poniżej znajduje się przykład składni języka Java.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
W powyższym kodzie słowo kluczowe **public** oznacza modyfikator dostępu. Stwierdza, że dostęp do tej klasy mogą mieć klasy spoza hierarchii klas. Modyfikator dostępu może być również **chroniony** (dostęp do tego samego pakietu) lub **prywatny** (dostęp do metod ma tylko ta sama klasa). **static** przed metodą wskazuje, że metodę można wywołać bez określonej instancji klasy. **void** wskazuje, że metoda nic nie zwróci. Aby wydrukować ciąg do konsoli. Używane jest polecenie System.out.println. W tym poleceniu klasa *System* ma pole statyczne *out*, które jest instancją klasy *PrintStream* zawierającą metodę *println*.

Nazwa pliku plików Java powinna być taka sama jak nazwa klasy. Tak więc plik Java dla przykładowego kodu miałby nazwę *ExampleApp.java*.

## Bibliografia ##

- [Java (język programowania) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

