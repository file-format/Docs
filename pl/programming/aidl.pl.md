{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik AIDL - plik języka definicji interfejsu systemu Android",
  "description":"Dowiedz się, czym jest format pliku AIDL wraz z przykładami i interfejsami API, które mogą tworzyć i otwierać pliki AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Czym jest plik AIDL?

Plik AIDL (Android Interface Definition Language) umożliwia programistom Androida ustanowienie komunikacji między różnymi aplikacjami. Na podstawie interfejsu programistycznego zarówno klient, jak i usługa zgadzają się na komunikację za pomocą komunikacji międzyprocesowej (IPC). Plik AIDL zawiera kod źródłowy [Java](/pl/programming/java/) do definiowania tych interfejsów i umów dotyczących komunikacji między aplikacjami.

Możesz otwierać pliki AIDL za pomocą Google Android Studio lub dowolnego edytora tekstu, takiego jak Microsoft Notepad i Notepad ++.

## Format pliku AIDL — więcej informacji

AIDL to pliki tekstowe zawierające interfejsy do komunikacji między aplikacjami. System operacyjny Android nie zezwala jednemu procesowi na dostęp do pamięci innego procesu. Powoduje to, że procesy dzielą swoje obiekty na prymitywy w celu zrozumienia bazowego systemu operacyjnego i ustanowienia procesu struktur komunikacyjnych dla programisty.

### Jakie typy danych są obsługiwane przez AIDL?

AIDL domyślnie obsługuje następujące typy danych.

* Wszystkie typy pierwotne w języku programowania Java (takie jak int, long, char, boolean itd.)
* Strunowy
* Sekwencja znaków
* Lista
* Mapa

## Przykład pliku AIDL

Poniżej znajduje się przykładowy plik AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Bibliografia

* [Język definicji interfejsu Androida (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

