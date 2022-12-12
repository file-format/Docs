{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "rozszerzenie", "plik", "format", "system", "plik TMP", "dokumenty TMP", "pliki TMP", "plik tymczasowy", "aplikacja", "programy" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Tymczasowy Format Pliku",
  "description":"Poznaj format pliku TMP i interfejsy API, które mogą tworzyć i otwierać pliki TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Czym jest plik TMP? ##

Plik TMP odnosi się do przejściowej kopii zapasowej, pamięci masowej lub innego systemu plików generowanego przez oprogramowanie. Czasami jest tworzony jako niewidoczny plik i często jest niszczony po zamknięciu programu. Pliki TMP mogą być również używane do tymczasowego przechowywania informacji podczas tworzenia nowego pliku.

## Format pliku TMP ##

Plik TMP zazwyczaj składa się z nieprzetworzonych danych, które są wykorzystywane jako faza procesu konwersji materiału z jednego stylu na inny. Microsoft Word i Apple Safari to dwie aplikacje, które mogą tworzyć i używać formatu plików TMP.

Wygenerowane dokumenty TMP powinny teoretycznie być automatycznie usuwane po zamknięciu programu lub wyłączeniu maszyny. W praktyce nie zawsze tak jest. W rezultacie podczas przeglądania dokumentów programu można natknąć się na pliki przejściowe, które nie są aktywnie używane przez system ani żadne inne oprogramowanie.

### Pamięć pomocnicza ###

Pamięć wirtualna jest używana w systemach operacyjnych, jednak programy, które wykorzystują ogromne ilości informacji, mogą wymagać tworzenia tymczasowych dokumentów.

### Komunikacja między procesami ###

Większość systemów operacyjnych zapewnia prymitywy do przekazywania danych między programami, takimi jak potoki, gniazda lub pamięć główna, ale najprostszą metodą jest przesłanie plików do pliku tymczasowego i powiadomienie aplikacji odbierającej o lokalizacji pliku tymczasowego.


## Specyfikacja techniczna ##

Uzyskanie wyróżniających się tymczasowych nazw dokumentów jest zwykle zapewniane przez systemy operacyjne i programy.
Pliki tymczasowe można bezpiecznie generować w systemach POSIX przy użyciu funkcji bibliotecznych mkstemp lub tmpfile. Niektóre systemy zawierają poprzednią aplikację mktemp POSIX (odkąd jej nie ma). Pliki te zwykle znajdują się w zwykłym katalogu tymczasowym na platformach Unix w /TMP lub %TEMP% (jest to specyficzne dla logowania) na komputerach z systemem Windows.

Po zatrzymaniu programu lub zamknięciu dokumentu plik przejściowy wygenerowany za pomocą pliku tmp jest automatycznie usuwany. GetTempFileName (Windows) lub tmpnam (POSIX) może służyć do tworzenia tymczasowej nazwy pliku, która będzie działać dłużej niż program, który ją utworzył.

## Odniesienie ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
