{
"data": "2023-02-02",
  "keywords": [
"plik aplikacji",
"co to jest plik aplikacji",
"plik",
"jak otworzyć plik aplikacji",
"rozszerzenie pliku aplikacji",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Dowiedz się więcej o formacie pliku aplikacji i interfejsach API, które umożliwiają tworzenie i otwieranie plików aplikacji.",
"title": "Format pliku aplikacji - pakiet aplikacji macOS",
"tytuł łącza": "APLIKACJA",
  "menu": {
    "docs": {
      "identifier": "executable-app",
      "parent": "executable"
}
},
"lastmod": "2023-02-02"
}

## Co to jest plik APP?

Plik .app w systemie macOS to specjalny typ katalogu, który zawiera wszystkie pliki niezbędne do uruchomienia określonej aplikacji, w tym kod wykonywalny, zasoby i metadane. Rozszerzenie .app sygnalizuje systemowi operacyjnemu, że ten katalog powinien być traktowany jako pojedyncza jednostka, a nie zbiór oddzielnych plików i że można go uruchomić bezpośrednio z Findera lub Docka.

Finder to domyślna aplikacja do zarządzania plikami w systemie macOS. Umożliwia przeglądanie i organizowanie plików i katalogów na komputerze. Dock to funkcja systemu macOS zapewniająca szybki dostęp do często używanych aplikacji i dokumentów. Zarówno Finder, jak i Dock umożliwiają uruchamianie aplikacji poprzez kliknięcie ich plików .app, co spowoduje otwarcie odpowiedniego pakietu aplikacji. Po uruchomieniu aplikacji uruchamiany jest kod wykonywalny zawarty w pakiecie .app, dzięki czemu aplikacja staje się dostępna do użytku. Plik .app reprezentuje aplikację w systemie plików i umożliwia użytkownikowi uzyskanie dostępu do aplikacji oraz jej uruchomienie.

Po kliknięciu prawym przyciskiem myszy pliku .app w Finderze w systemie macOS i wybraniu opcji "Pokaż zawartość pakietu" zobaczysz wewnętrzną strukturę pakietu aplikacji. Jest to przydatne, jeśli chcesz uzyskać dostęp do zasobów lub plików używanych przez aplikację lub jeśli chcesz sprawdzić zawartość aplikacji w celu rozwiązywania problemów. Zawartość pakietu pliku .app zazwyczaj obejmuje katalogi z zasobami, takimi jak obrazy i dźwięki, a także kod wykonywalny aplikacji. Eksplorując zawartość pliku .app, możesz uzyskać głębszy wgląd w sposób, w jaki aplikacja jest zbudowana i co robi.

## Jak otworzyć plik APP?

Aby otworzyć plik .app w systemie macOS, po prostu kliknij dwukrotnie plik w Finderze. Spowoduje to uruchomienie aplikacji zawartej w pakiecie .app. Jeżeli aplikacja jest zainstalowana w Twoim systemie i została skojarzona z plikiem typu .app, dwukrotne kliknięcie pliku powinno uruchomić aplikację automatycznie. Jeśli aplikacja nie jest skojarzona z typem pliku .app, może być konieczne kliknięcie pliku prawym przyciskiem myszy i wybranie opcji "Otwórz za pomocą", aby wybrać odpowiednią aplikację do otwarcia.

Możesz otworzyć plik .app na terminalu w systemie macOS, używając polecenia "otwórz". Aby to zrobić, przejdź do katalogu, w którym znajduje się plik .app, za pomocą polecenia "cd", a następnie uruchom następujące polecenie:

```
open <AppName>.app 
```

Gdzie<AppName> to nazwa aplikacji, którą chcesz uruchomić. Spowoduje to uruchomienie aplikacji tak, jakbyś kliknął ją dwukrotnie w Finderze. Polecenie "otwórz" to narzędzie ogólnego przeznaczenia, którego można używać do otwierania wielu różnych typów plików, w tym aplikacji, dokumentów i katalogów. Użycie polecenia "otwórz" w pliku .app powoduje uruchomienie aplikacji zawartej w pakiecie.

## Bibliografia
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
