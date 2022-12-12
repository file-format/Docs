{
  "date" : "2020-11-11",
  "keywords" :["ACCDB", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików ACCDB i interfejsy API, które mogą tworzyć i otwierać pliki ACCDB.",
  "title" :"Format Pliku ACCDB - Plik Bazy Danych Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Czym jest plik ACCDB?

Plik z rozszerzeniem .accdb to plik bazy danych programu Microsoft Access 2007, który przechowuje dane użytkowników w tabelach. Wspiera przechowywanie
niestandardowe formularze, zapytania SQL i inne dane. Pliki ACCDB zastąpiły pliki [MDB](/pl/database/mdb/) po tym, jak Microsoft przeszedł na strukturę plików opartą na XML. Pliki ACCDB nadal można konwertować na MDB ze starą kompatybilnością. Jednak ACCDB są obecnie powszechnie używanym formatem plików bazy danych programu Access. Microsoft wspierał również dodatkowe funkcje w formacie ACCDB, takie jak możliwość przechowywania załączników, danych binarnych i obsługa pól wielowartościowych.

## Format pliku ACCDB

Podobnie jak MDB, nie ma dostępnych publicznych specyfikacji formatu pliku ACCDB. Firma Microsoft obsługuje programowy dostęp do tych plików za pośrednictwem standardu Open Database Connectivity (ODBC) i języka Visual Basic for Applications (VBA).

### Wgląd

Zrzut szesnastkowy prostego pliku ACCDB sugeruje, że istnieją ogólne podobieństwa w strukturze do najnowszych wersji poprzedniej rodziny formatów MDB. Oba formaty plików używają stałych rozmiarów stron wynoszących 4096 bajtów. Innym podobieństwem między ACCDB i MDB jest forma magicznej liczby, która zawiera ciąg „Standard ACE DB” dla ACCDB. Wersja lub kod zgodności znajduje się w tej samej lokalizacji w obu formatach. Narzędzia mdb | Plik HACKING stwierdza, że „Offset 0x14 zawiera wersję Jet tej bazy danych”, a nieoficjalny przewodnik MDB jest zgodny. Informacje zawarte w tych źródłach, w połączeniu z wpisem w Wikipedii dotyczącym [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), sugerują, że wartość 0x02 oznacza ACE 12 (Access 2007), a 0x03 wskazuje ACE 14 (dostęp 2010). Jednak minimalna baza danych utworzona w programie Access 2010 i podobna baza utworzona w programie Access 2016 mają w tej lokalizacji 0x02. Minimalna baza danych utworzona w programie Access 2016, ale definiująca kolumnę z nowo wprowadzonym typem danych „large integer”, miała wartość 0x05. W plikach ACCDB ten wskaźnik wydaje się odzwierciedlać zgodność pliku, a nie wersję silnika ACE użytego do jego utworzenia.

## Bibliografia

* [Format pliku programu Access](https://support.microsoft.com/en-us/office/ Which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Specyfikacje programu Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Aparat bazy danych Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Którego formatu pliku programu Access powinienem użyć?](https://support.microsoft.com/en-us/office/ Which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)

