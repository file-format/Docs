{
  "date" : "2021-06-24",
  "keywords" :["plik nietoperza", "co to jest plik nietoperza", "plik", "przykład pliku nietoperza", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku BAT i interfejsy API, które mogą tworzyć i otwierać pliki BAT.",
  "title" :"BAT - Format pliku wsadowego",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Czym jest plik BAT?
Plik BAT jest znany jako plik wsadowy uruchamiany z systemem DOS i wszystkimi wersjami systemu Windows pod cmd.exe. Składa się z szeregu poleceń wiersza w postaci zwykłego tekstu, które mają być wykonywane przez interpreter wiersza poleceń w celu wykonania różnych zadań, takich jak uruchamianie narzędzi konserwacyjnych w systemie Windows lub uruchamianie typowych programów. Plik wsadowy może zawierać dowolne polecenie, które interpreter może zaakceptować interaktywnie i wykorzystywać strukturę kodu, która umożliwia warunkowe rozgałęzianie i zapętlanie, zgodnie z zapisem w pliku wsadowym.
## Format pliku BAT
Format pliku BAT to po prostu skrypt włączony do automatyzacji sekwencji poleceń, które mają charakter powtarzalny. Termin „partia” jest używany do przetwarzania wsadowego. Można to uznać za „wykonanie nieinteraktywne”. Dlatego plik wsadowy może nie przetwarzać partii wielu danych. W starym Dyskowym systemie operacyjnym (DOS) plik wsadowy był uruchamiany w interfejsie wiersza poleceń, wpisując nazwę pliku i rozszerzenie .bat. Wcześniejszy system operacyjny oparty na interfejsie graficznym firmy Microsoft, taki jak Microsoft Windows, był zależny od systemu DOS. Użytkownicy musieli używać systemu DOS do wykonywania typowych operacji, takich jak naprawa, optymalizacja lub ponowna instalacja systemu Windows. Później Microsoft wprowadził system Windows NT, który nie był zależny od systemu operacyjnego DOS. Dlatego pliki wsadowe można uruchamiać za pomocą wiersza polecenia lub **cmd.exe** we współczesnych systemach operacyjnych firmy Microsoft.
### Parametry pliku wsadowego
Wiersz polecenia obsługuje wiele zmiennych specjalnych, takich jak **%0, %1 do %9**, które odwołują się do nazwy i ścieżki zadania wsadowego oraz dziewięciu parametrów wywołania z poziomu zadania wsadowego. Nieistniejące parametry są zastępowane łańcuchem o zerowej długości. Chociaż można ich używać podobnie jak zmiennych środowiskowych, ale nie są one zapisywane w środowisku. Microsoft i IBM określają te zmienne jako parametry zastępcze, podczas gdy Novell, Digital Research i Caldera wprowadziły dla nich termin zmienne zastępcze.

Oto kilka przydatnych poleceń pliku wsadowego:
| Polecenie | Opis |
------|------------|
| VER | To polecenie wsadowe pokazuje używaną wersję systemu MS-DOS. |
|SPOŁECZNE| Jest to polecenie wsadowe, które kojarzy rozszerzenie z typem pliku (FTYPE), wyświetla istniejące powiązania lub usuwa powiązanie. |
|CD| To polecenie wsadowe pomaga w dokonywaniu zmian w innym katalogu lub wyświetla bieżący katalog. |
|CLS| To polecenie wsadowe czyści ekran. |
|KOPIUJ| To polecenie wsadowe służy do kopiowania plików z jednej lokalizacji do drugiej. |
|DEL| To polecenie wsadowe usuwa pliki, a nie katalogi. |
|KIER| To polecenie wsadowe wyświetla zawartość katalogu. |
|DATA| To polecenie wsadowe pomaga znaleźć datę systemową. |
|ECHO| To polecenie wsadowe wyświetla komunikaty lub włącza lub wyłącza powtarzanie poleceń. |
|WYJŚCIE| To polecenie wsadowe powoduje wyjście z konsoli DOS. |
|MD| To polecenie wsadowe tworzy nowy katalog w bieżącej lokalizacji. |
|PRZESUŃ| To polecenie wsadowe przenosi pliki lub katalogi między katalogami. |
|ŚCIEŻKA| To polecenie wsadowe wyświetla lub ustawia zmienną ścieżki. |
|PAUZA| To polecenie wsadowe monituje użytkownika i czeka na wprowadzenie wiersza danych wejściowych. |
|POMOC| To polecenie wsadowe może służyć do zmiany lub zresetowania monitu cmd.exe. |
|RD| To polecenie wsadowe usuwa katalogi, ale katalogi muszą być puste, zanim będzie można je usunąć. |
|REN| Zmienia nazwy plików i katalogów |
|REM| To polecenie wsadowe jest używane do uwag w plikach wsadowych, uniemożliwiając wykonanie treści uwagi. |
|START| To polecenie wsadowe uruchamia program w nowym oknie lub otwiera dokument. |
|CZAS| To polecenie wsadowe ustawia lub wyświetla czas. |
|TYP| To polecenie wsadowe drukuje zawartość pliku lub plików na wyjściu. |
|TOM| To polecenie wsadowe wyświetla etykiety woluminów. |
|ATRYB| Wyświetla lub ustawia atrybuty plików w bieżącym katalogu |
|CHKDSK| To polecenie wsadowe sprawdza dysk pod kątem problemów. |
|WYBÓR| To polecenie wsadowe udostępnia użytkownikowi listę opcji. |
|CMD| To polecenie wsadowe wywołuje inne wystąpienie wiersza polecenia. |
|KOMP| To polecenie wsadowe porównuje 2 pliki na podstawie rozmiaru pliku. |
|KONWERTOWAĆ| To polecenie wsadowe konwertuje wolumin z systemu plików FAT16 lub FAT32 na system plików NTFS. |
|ZAPYTAJ O STEROWNIKI| To polecenie wsadowe pokazuje wszystkie zainstalowane sterowniki urządzeń i ich właściwości. |
|ROZWIŃ| To polecenie wsadowe wyodrębnia pliki ze skompresowanych plików .cab cabinet. |
|ZNAJDŹ| To polecenie wsadowe wyszukuje ciąg znaków w plikach lub danych wejściowych, wyświetlając pasujące wiersze. |
|FORMATUJ| To polecenie wsadowe formatuje dysk w celu użycia systemu plików obsługiwanego przez system Windows, takiego jak FAT, FAT32 lub NTFS, zastępując w ten sposób poprzednią zawartość dysku. |
|POMOC| To polecenie wsadowe wyświetla listę poleceń dostarczonych przez system Windows. |
|IPKONFIG| To polecenie wsadowe wyświetla konfigurację adresu IP systemu Windows. Pokazuje konfigurację według połączenia i nazwę tego połączenia. |
|ETYKIETA| To polecenie wsadowe dodaje, ustawia lub usuwa etykietę dysku. |
|WIĘCEJ| To polecenie wsadowe wyświetla zawartość pliku lub plików, jeden ekran na raz. |
|NETTO| Zapewnia różne usługi sieciowe, w zależności od użytego polecenia. |
|PING| To polecenie wsadowe wysyła pakiety „echo” ICMP/IP przez sieć na wyznaczony adres. |
|WYŁĄCZENIE| To polecenie wsadowe wyłącza komputer lub wylogowuje bieżącego użytkownika. |
|SORTUJ| To polecenie wsadowe pobiera dane wejściowe z pliku źródłowego i sortuje jego zawartość alfabetycznie, od A do Z lub od Z do A. Wypisuje dane wyjściowe na konsoli. |
|PODSTAW| To polecenie wsadowe przypisuje literę dysku do folderu lokalnego, wyświetla bieżące przypisania lub usuwa przypisanie. |
|INFORMACJE O SYSTEMIE| To polecenie wsadowe pokazuje konfigurację komputera i jego systemu operacyjnego. |
|ZAKRYCIE ZADANIA| To polecenie wsadowe kończy jedno lub więcej zadań. |
|LISTA ZADAŃ| To polecenie wsadowe wyświetla listę zadań, w tym nazwę zadania i identyfikator procesu (PID). |
|XKOPIUJ| To polecenie wsadowe kopiuje pliki i katalogi w bardziej zaawansowany sposób. |
|DRZEWO| To polecenie wsadowe wyświetla drzewo wszystkich podkatalogów bieżącego katalogu na dowolnym poziomie rekurencji lub głębokości. |
|FC |To polecenie wsadowe wyświetla rzeczywiste różnice między dwoma plikami. |
|DISKPART |To polecenie wsadowe pokazuje i konfiguruje właściwości partycji dysku. |
|TYTUŁ |To polecenie wsadowe ustawia tytuł wyświetlany w oknie konsoli. |
|USTAW | Wyświetla listę zmiennych środowiskowych w bieżącym systemie. |

## Przykład pliku BAT
Skrypty wsadowe są zwykle zapisywane jako proste pliki tekstowe; zawierające polecenia, które są wykonywane w sekwencji. Pliki te są zapisywane z rozszerzeniem .bat; rozpoznawane i wykonywane przy użyciu oprogramowania **Interpretator poleceń**. To oprogramowanie jest natywnie dostępne w systemie Microsoft Windows pod nazwą **cmd.exe**.

Oto przykładowy skrypt wsadowy, który usuwa wszystkie pliki w bieżącym katalogu:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Bibliografia

* [Skrypt wsadowy — skrócony przewodnik](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Plik wsadowy - autorstwa Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

