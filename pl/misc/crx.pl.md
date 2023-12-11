{
"data": "2023-06-08",
  "keywords": [
"plik crx",
"co to jest plik crx",
"jak zainstalować plik crx w Google Chrome",
"jak otworzyć plik crx",
"co zawiera plik crx",
"jaki jest format pliku crx",
"plik",
"rozszerzenie pliku crx",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku CRX - rozszerzenie Google Chrome",
  "description":"Dowiedz się o formacie CRX i interfejsach API, które umożliwiają tworzenie i otwieranie plików CRX.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"lastmod": "2023-06-08"
}

## Czym jest plik CRX?

Format pliku CRX jest powiązany z rozszerzeniami przeglądarki Google Chrome. Plik CRX to zasadniczo skompresowany pakiet zawierający niezbędne pliki i metadane do zainstalowania i uruchomienia rozszerzenia w przeglądarce Google Chrome. Poprawia funkcjonalność lub wygląd przeglądarki internetowej, udostępniając dodatkową funkcję lub motyw.

Po pobraniu i zainstalowaniu pliku CRX w przeglądarce Google Chrome przeglądarka weryfikuje integralność rozszerzenia za pomocą klucza publicznego i podpisu. Jeśli weryfikacja przebiegnie pomyślnie, Chrome wyodrębni zawartość pliku CRX i zainstaluje rozszerzenie, udostępniając je do użytku. Użytkownicy mogą zarządzać swoimi rozszerzeniami za pośrednictwem strony Rozszerzenia Chrome, która umożliwia włączanie, wyłączanie lub usuwanie zainstalowanych rozszerzeń.

## Jak zainstalować plik CRX w przeglądarce Google Chrome?

Aby zainstalować plik CRX w przeglądarce Google Chrome, możesz wykonać następujące kroki:

1. Otwórz przeglądarkę Chrome.
2. Wpisz "chrome://extensions" w pasku adresu i naciśnij Enter.
3. Włącz przełącznik "Tryb programisty" znajdujący się w prawym górnym rogu strony Rozszerzenia.
4. Kliknij przycisk "Załaduj rozpakowany".
5. Zlokalizuj i wybierz folder zawierający wyodrębnioną zawartość pliku CRX (lub po prostu wybierz sam plik CRX).
6. Kliknij "Otwórz", aby zainstalować rozszerzenie.

## Co zawiera plik CRX?

Plik CRX zawiera niezbędne pliki i metadane wymagane dla rozszerzenia Google Chrome. Oto zestawienie typowej zawartości pliku CRX:

- **Plik manifestu (manifest.json):** Ten plik jest plikiem w formacie JSON, który zawiera informacje o rozszerzeniu, takie jak jego nazwa, wersja, opis, uprawnienia i skrypty w tle. Definiuje strukturę i zachowanie rozszerzenia.
- **Pliki JavaScript:** Pliki te zawierają kod definiujący funkcjonalność rozszerzenia. Mogą zawierać skrypty do obsługi zdarzeń, modyfikowania stron internetowych lub interakcji z interfejsami API przeglądarki Chrome.
- **Pliki HTML, CSS i obrazy:** Rozszerzenia często zawierają elementy interfejsu użytkownika, takie jak wyskakujące okienka lub strony opcji. Pliki HTML definiują strukturę tych interfejsów, natomiast pliki CSS kontrolują ich wygląd. Pliki obrazów służą do tworzenia ikon lub innych zasobów graficznych.
- **Opcjonalne pliki zasobów:** Rozszerzenia mogą zawierać dodatkowe zasoby, takie jak pliki lokalizacyjne obsługujące wiele języków. Pliki te zawierają tłumaczenia tekstu używanego w interfejsie użytkownika rozszerzenia.
- **Skrypty działające w tle:** Jeśli rozszerzenie ma procesy działające w tle lub skrypty działające niezależnie od aktywnej strony internetowej, skrypty te zostaną uwzględnione w pliku CRX.
- **Skrypty treści:** Skrypty treści to skrypty, które można wstrzykiwać na strony internetowe w celu modyfikowania ich zachowania lub interakcji z ich treścią. Jeśli rozszerzenie korzysta ze skryptów treści, niezbędne pliki dla tych skryptów będą obecne w pliku CRX.
- **Inne zasoby:** W zależności od konkretnych wymagań rozszerzenia mogą zostać dołączone dodatkowe pliki, takie jak pliki audio lub wideo, czcionki lub pliki danych.

Format pliku CRX to zasadniczo skompresowany pakiet zawierający wszystkie te pliki i foldery w uporządkowany sposób. Kiedy plik CRX jest zainstalowany w przeglądarce Google Chrome, przeglądarka wyodrębnia zawartość i umieszcza ją w odpowiednich lokalizacjach, umożliwiając załadowanie i uruchomienie rozszerzenia w przeglądarce.

## Jaki jest format pliku CRX?

Format pliku CRX to specyficzny format pakowania i dystrybucji rozszerzeń przeglądarki Google Chrome. Zasadniczo jest to skompresowane archiwum ZIP z innym rozszerzeniem pliku. Podstawowa struktura pliku CRX jest następująca:

- **Podpis pliku:** Pierwsze 4 bajty pliku zawierają magiczną liczbę "Cr24" (w formacie szesnastkowym: 43 72 32 34), która służy jako podpis identyfikujący plik jako plik CRX.
- **Numer wersji:** Kolejne 4 bajty reprezentują numer wersji formatu CRX.
- **Długość klucza publicznego:** Kolejne 4 bajty wskazują długość zakodowanego klucza publicznego używanego do weryfikacji podpisu rozszerzenia.
- **Długość podpisu:** Kolejne 4 bajty określają długość podpisu rozszerzenia.
- **Klucz publiczny:** Ta sekcja zawiera zakodowany klucz publiczny używany do weryfikacji integralności rozszerzenia.
- **Podpis:** Ta sekcja zawiera sygnaturę rozszerzenia, która jest generowana poprzez podpisanie zawartości rozszerzenia kluczem prywatnym odpowiadającym wspomnianemu powyżej kluczowi publicznemu.
- **Archiwum ZIP:** Pozostałe bajty pliku CRX stanowią skompresowane archiwum ZIP. To archiwum zawiera wszystkie niezbędne pliki i foldery rozszerzeń, w tym plik manifestu, pliki JavaScript, pliki HTML, pliki CSS, obrazy i wszelkie inne zasoby.

## Bibliografia
* [Specyfikacja formatu CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

