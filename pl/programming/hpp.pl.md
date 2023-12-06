{
"data": "2023-06-08",
  "keywords": [
"plik hp",
"co to jest plik hpp",
"co zawiera plik hpp",
"przykład pliku hpp",
"jaki jest format pliku hpp",
"plik",
"rozszerzenie pliku hp",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku HPP - plik nagłówkowy C++",
  "description":"Dowiedz się o formacie HPP i interfejsach API, które umożliwiają tworzenie i otwieranie plików HPP.",
"tytuł łącza": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Czym jest plik HPP?

Format pliku ".hpp" jest powszechnie używany w przypadku plików nagłówkowych w języku programowania C++. Pliki nagłówkowe zazwyczaj zawierają deklaracje i definicje funkcji, klas, zmiennych i stałych, które są używane przez inne pliki kodu źródłowego w projekcie C++.

Celem używania plików nagłówkowych jest umożliwienie współużytkowania wspólnego kodu w wielu plikach kodu źródłowego bez duplikowania samego kodu. Kiedy plik źródłowy C++ potrzebuje dostępu do deklaracji lub definicji z pliku nagłówkowego, dołącza plik nagłówkowy przy użyciu dyrektywy preprocesora `#include`.

Rozszerzenie pliku ".hpp" jest często używane do wskazania, że plik jest plikiem nagłówkowym C++. Używanie tego konkretnego rozszerzenia dla plików nagłówkowych nie jest wymagane, ale możesz także natknąć się na pliki nagłówkowe z rozszerzeniem ".h" lub innymi. Wybór rozszerzenia jest w dużej mierze kwestią konwencji i osobistych preferencji.

Gdy plik źródłowy C++ zawiera plik nagłówkowy za pomocą `#include`, kompilator skutecznie łączy zawartość pliku nagłówkowego z plikiem źródłowym przed skompilowaniem go jako jednostki. Umożliwia to plikowi źródłowemu dostęp do deklaracji i definicji w pliku nagłówkowym, dostarczając kompilatorowi niezbędnych informacji do sprawdzania typu i generowania kodu.

## Co zawiera plik HPP?

Oto kilka typowych treści, które można znaleźć w pliku ".hpp":

- **Deklaracje funkcji:** Pliki nagłówkowe często zawierają deklaracje funkcji bez ich rzeczywistej implementacji. Deklaracje te dostarczają informacji o nazwie funkcji, typie zwracanym i parametrach, umożliwiając innym plikom kodu źródłowego korzystanie z funkcji bez konieczności znajomości szczegółów implementacji.
- **Deklaracje klas:** Pliki nagłówkowe mogą zawierać deklaracje klas, w tym nazwę klasy, zmienne składowe, funkcje składowe i specyfikatory dostępu. Dołączając deklarację klasy do pliku nagłówkowego, inne pliki kodu źródłowego mogą tworzyć obiekty tej klasy i uzyskiwać dostęp do jej elementów.
- **Deklaracja stałych:** Pliki nagłówkowe mogą definiować stałe, takie jak zmienne globalne lub wartości wyliczeniowe, które mają być współdzielone przez wiele plików kodu źródłowego. Dostęp do tych stałych można uzyskać poprzez dołączenie pliku nagłówkowego do innych plików źródłowych, co umożliwi im użycie zdefiniowanych stałych.
- **Definicje typów:** Pliki nagłówkowe mogą zawierać definicje typów przy użyciu słowa kluczowego "typedef" lub aliasy typów przy użyciu słowa kluczowego "using". Te definicje tworzą nowe nazwy dla istniejących typów, dzięki czemu kod jest bardziej czytelny i łatwiejszy w utrzymaniu.
- **Definicje funkcji inline:** W niektórych przypadkach pliki nagłówkowe mogą zawierać definicje funkcji inline. Funkcje wbudowane to małe funkcje, które są rozwijane w witrynie wywołania, a nie wywoływane jako osobna funkcja. Dołączenie definicji funkcji wbudowanej do pliku nagłówkowego umożliwia kompilatorowi bezpośrednie zastąpienie wywołania funkcji treścią funkcji, co potencjalnie poprawia wydajność.

## Przykład pliku HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Jaki jest format pliku HPP?

HPP to zwykły plik tekstowy, ale przestrzega ogólnych zasad i składni języka programowania C++. Oto zestawienie ogólnego formatu i struktury pliku ".hpp":

- **Ochrona nagłówka:** Zazwyczaj plik ".hpp" zaczyna się od osłon nagłówka, aby zapobiec wielokrotnemu dołączeniu tego samego pliku. Osiąga się to za pomocą dyrektyw preprocesora, takich jak `#ifndef`, `#define` i `#endif`. Ochrona nagłówka zapewnia, że zawartość pliku zostanie uwzględniona tylko raz podczas procesu kompilacji.
- **Dołącz instrukcje:** Po osłonach nagłówka możesz dołączyć inne niezbędne pliki nagłówkowe, używając dyrektywy `#include`. Mogą one obejmować standardowe nagłówki bibliotek lub inne niestandardowe nagłówki wymagane przez Twój kod.
- **Deklaracje i definicje:** Podstawową zawartością pliku ".hpp" są deklaracje oraz, w niektórych przypadkach, definicje klas, funkcji, stałych, aliasów typów i innych elementów. Na przykład możesz zadeklarować klasy za pomocą słowa kluczowego "class", funkcje używając ich typu zwracanego sygnału, nazwy i listy parametrów, a stałe za pomocą słowa kluczowego "const", po którym następuje ich typ i nazwa.
- **Definicje funkcji inline:** W niektórych przypadkach można załączyć definicje funkcji inline bezpośrednio w pliku ".hpp". Funkcje inline są zwykle definiowane w treści klasy, co oznacza, że definicja funkcji jest dołączona do jej deklaracji. Można tego dokonać poprzedzając definicję funkcji słowem kluczowym `inline`.
- **Deklaracje przestrzeni nazw:** Jeśli używasz przestrzeni nazw w swoim kodzie, możesz je zadeklarować w pliku ".hpp". Odbywa się to za pomocą słowa kluczowego `namespace`, po którym następuje nazwa przestrzeni nazw i załączenie odpowiedniego kodu w bloku przestrzeni nazw.

## Bibliografia
* [Pliki nagłówkowe (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

