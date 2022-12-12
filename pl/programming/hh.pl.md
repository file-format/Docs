{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh", "co to jest plik .hh", "jak otworzyć plik .hh", "rozszerzenie", "plik", "plik .hh", "format pliku .hh", " rozszerzenie pliku .hh","Przykład pliku .HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - Format pliku nagłówka C++",
  "description":"Dowiedz się o formacie pliku HH i interfejsach API, które mogą tworzyć i otwierać plik HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Czym jest plik HH?

Plik z rozszerzeniem .hh to plik nagłówkowy C++, który zawiera deklarację zmiennych, stałych i funkcji. Te deklaracje są używane przez odpowiednie pliki implementacji C++, zwykle zapisywane jako pliki [.cpp](/pl/programming/cpp/), które zawierają rzeczywistą implementację logiki użytkownika. Pliki nagłówkowe .hh są przywoływane w plikach CPP implementacji przy użyciu dyrektywy `#include`. Możesz dodać jak najwięcej plików nagłówkowych do swojego projektu C++, aby uwzględnić deklaracje na poziomie projektu.

## Format pliku .HH

Plik .hh jest zwykłym plikiem tekstowym tworzonym z uwzględnieniem zasad definiowania plików nagłówkowych. Najczęstsze informacje zadeklarowane w pliku .hh obejmują następujące informacje.

**`Zmienne`** — w przypadku programowania obiektowego (OOP) plik nagłówka klasy zawiera definicje wszystkich zmiennych na poziomie klasy, które są dostępne w plikach kodu źródłowego implementacji
**`Deklaracja metod`** — wszystkie deklaracje metod są zawarte w plikach nagłówkowych .h, aby były dostępne w wielu plikach implementacji.
**`Definicje funkcji nieliniowych`** — pliki nagłówkowe mogą również zawierać definicje metod nieliniowych.
**`Mapy wiadomości`** — plik nagłówkowy może również zawierać mapy wiadomości w przypadku implementacji kodu źródłowego MFC. W takim przypadku mapy komunikatów są powiązane z implementacją funkcjonalności, która jest powiązana z elementami interfejsu użytkownika, takimi jak przycisk, pole wyboru, przyciski radiowe itp.

## Różnica między plikami .H i .HH

Najwyraźniej nie ma takiej różnicy między plikami nagłówkowymi .h i .hh poza zalecanym sposobem ich używania dla odpowiednich języków, tj. [C](/pl/programming/c/) lub C++. Nazywanie plików nagłówkowych zgodnie z tymi językami pomaga rozróżnić je w dużym projekcie, który może być mieszanką implementacji C i C++.

Ponadto, jeśli nagłówki są oddzielone rozszerzeniem, Twój edytor może automatycznie zastosować odpowiednie formatowanie dla odpowiednio.

Ogólnie rzecz biorąc, rozróżnienie tych dwóch formatów plików nie zaszkodzi, ale będzie korzystne i zachęca się do naśladowania rozróżnienia C i C++.

### Osłony nagłówka

Pliki nagłówkowe mogą powodować złożone błędy, gdy wiele deklaracji jest zawartych w tym samym pliku w wyniku dodania innych plików nagłówkowych. Te zduplikowane definicje powodują błędy kompilatora. Tej problematycznej sytuacji można uniknąć za pomocą mechanizmu zwanego strażnikiem nagłówka, który jest dyrektywą kompilacji warunkowej, jak pokazano poniżej.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Za pomocą tego nagłówka preprocesor sprawdza, czy `ANY_UNIQUE_NAME_HERE_HPP` zostało już zdefiniowane. Jeśli nagłówek jest wielokrotnie dołączany do tego samego pliku, zawartość nagłówka zostanie zignorowana.

## Bibliografia

* [Pliki nagłówkowe — Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Różnice między formatami plików .h i .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

