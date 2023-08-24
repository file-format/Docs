{
  "date" : "2021-06-30",
  "keywords" :["plik msi", "format pliku MSI", "co to jest plik msi", "plik", "przykład msi", "rozszerzenie pliku msi", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku MSI i interfejsy API, które mogą tworzyć i otwierać pliki MSI.",
  "title" :"MSI - plik pakietu instalatora Windows",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Czym jest plik MSI?
Plik MSI używany do instalowania i uruchamiania programów Windows; kompletny pakiet dla systemu Microsoft Windows zawierający informacje dotyczące instalacji typowego oprogramowania, w tym niezbędne pliki do zainstalowania oraz informacje o miejscu instalacji. Pliki MSI mogą również zawierać pakiet aktualizacji oprogramowania. Pliki MSI są podobne do [EXE](/pl/executable/exe/), ale EXE czasami może nie zawierać informacji o instalatorze, a program może działać bezpośrednio podczas wykonywania pliku EXE.

## Format pliku MSI
Instalator Windows jest w rzeczywistości interfejsem API (interfejsem programowania aplikacji) i składnikiem oprogramowania systemu Microsoft Windows używanym do instalacji, usuwania i konserwacji oprogramowania. Informacje instalacyjne i opcjonalne pliki są spakowane jako pakiety instalacyjne i luźno relacyjne bazy danych o strukturze magazynu strukturalnego COM; dobrze znane jako **pliki MSI**, mające rozszerzenie .msi. Pakiety z rozszerzeniem pliku **.mst** zawierają **Skrypty transformacji** Instalatora Windows, pliki z rozszerzeniem **.msm** zawierają **Merge Modules** i plik z rozszerzeniem **.pcp** służy do **Właściwości tworzenia poprawek**. Instalator Windows staje się bardziej zaawansowany po wprowadzeniu znaczących zmian w stosunku do swoich wcześniejszych wersji, Setup API. Środowisko GUI i automatyczne generowanie sekwencji dezinstalacji to nowe funkcje Instalatora Windows. Obecnie jest rozważany jako alternatywa dla samodzielnych, wykonywalnych ram instalacyjnych.

### Struktura logiczna pakietów MSI
Pakiet oznacza instalację jednego lub więcej pełnych produktów i jest ogólnie identyfikowany przez **GUID**. Produkt składa się z jednego lub wielu komponentów i jest pogrupowany w różne funkcje. Instalator Windows nie obsługuje jednocześnie zależności między różnymi produktami. Logiczna struktura pakietów składa się z następujących elementów:

- **Produkty**: Pojedynczy, zainstalowany, działający program lub zestaw połączonych ze sobą wielu programów jest produktem. Produkt jest identyfikowany za pomocą unikalnego identyfikatora GUID.
- **Funkcje**: Może zawierać dowolną liczbę komponentów i innych funkcji podrzędnych. Mniejsze pakiety mogą składać się z jednej funkcji.
- **Komponenty**: Komponent jest traktowany przez Instalatora Windows jako jednostka; może zawierać pliki programów, foldery, klucze rejestru, komponenty COM i skróty.
- **Ścieżki klucza**: Ścieżka klucza to określony plik, źródło danych ODBC lub klucz rejestru, który autor pakietu określa jako krytyczny dla danego składnika.

## Bibliografia

* [Instalator Windows — z Wikipedii](https://en.wikipedia.org/wiki/Windows_Installer)


