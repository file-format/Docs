{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "JSON", "Plik archiwum"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - format pliku archiwum HTTP",
  "description" :"Twój przewodnik po formacie pliku, aby dowiedzieć się, co to jest plik HAR i interfejsy API, które mogą tworzyć i otwierać plik HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Czym jest plik HAR?

Plik z rozszerzeniem .har (HTTP Archive) to plik archiwum HTTP, który przechowuje dane sesji przesyłane przez wiele przeglądarek (takich jak Chrome, Safari, IE, Firefox itp.) w formacie [JSON](/pl/web/json/) w formacie pliku. Dane przesyłane przez Internet między serwerem a klientem (w tym przypadku przeglądarką użytkownika) zawierają nagłówki żądań i odpowiedzi HTTP, które są przechowywane w pliku HAR. Ponadto zawiera szczegółowe informacje o danych dotyczących wydajności stron internetowych ładowanych w przeglądarce. Pliki HAR można otwierać w dowolnym edytorze tekstu, takim jak Notatnik w systemie operacyjnym Microsoft Windows i TextEdit w systemie Apple MacOS.

## Format pliku HAR — więcej informacji

Pliki HAR przechowują informacje o sesji w zwykłym pliku tekstowym przy użyciu popularnego formatu JSON. Specyfikacje formatu plików HAR zostały opracowane przez Web Performance Group of the World Web Consortium (W3C), ale nie mogły zostać opublikowane. Jednak z powodzeniem zdefiniował format archiwalny dla transakcji HTTP.

Oprócz monitorowania przesyłania informacji o żądaniach i odpowiedziach, pliki HAR są używane przez programistów do rejestrowania wydajności przeglądarki internetowej pod względem szybkości ładowania strony, czasu ładowania treści, załadowanej treści, zapytań wykonanych w celu uzyskania odpowiedzi z przeglądarki i wielu innych .

## Dlaczego warto używać plików HAR?

Pliki HAR mogą być pomocne w poprawie wydajności witryny internetowej poprzez ocenę długiego czasu ładowania, czasu renderowania strony i czasu odpowiedzi. Pliki HAR można analizować w celu znalezienia takich problemów i rozwiązania wszelkich problemów z witryną w celu poprawy wydajności.

## Jak wygenerować plik HAR?

Jak więc wygenerować plik HAR? Cóż, zależy to od typu przeglądarki używanej do generowania pliku HAR. W tym przewodniku wymieniamy kroki dla przeglądarki Google Chrome. Metody generowania plików HAR przy użyciu Safari, Firefox itp. można łatwo wyszukać w Internecie i zastosować.

### Kroki, aby wygenerować plik HAR za pomocą przeglądarki Google Chrome

Następujące kroki można wykonać na stronie internetowej, na której występują problemy.

1. Otwórz stronę internetową w Google Chrome, na której wystąpił problem.
1. Otwórz narzędzie deweloperskie (zbadaj element).
1. Przejdź w lewą stronę panelu, aby rozpocząć nagrywanie pliku. W tej sekcji znajduje się mały okrągły czerwony przycisk.
1. Kliknij ikonę „Wyczyść”, aby usunąć wszelkie zapisy dziennika przechowywane w przeglądarce.
1. Aby zapisać żądaną zawartość, jak pokazano powyżej, kliknij prawym przyciskiem myszy i kliknij „Zapisz jako plik HAR”

## Bibliografia

* [Format pliku HAR – Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))

