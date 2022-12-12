{
  "date" : "2019-12-10",
  "keywords" :["CSV", "plik", "rozszerzenie", "format pliku", "Wartości oddzielone przecinkami", "Arkusz kalkulacyjny"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku CSV i interfejsy API, które mogą tworzyć i otwierać pliki CSV.",
  "title" :"Format Pliku CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co to jest plik CSV?

Pliki z rozszerzeniem .csv (Comma Separated Values) reprezentują zwykłe pliki tekstowe, które zawierają rekordy danych z wartościami oddzielonymi przecinkami. Każda linia w pliku CSV to nowy rekord ze zbioru rekordów zawartych w pliku. Takie pliki są generowane, gdy zamierzony jest transfer danych z jednego systemu pamięci masowej do drugiego. Ponieważ wszystkie aplikacje potrafią rozpoznawać rekordy oddzielone przecinkiem, import takich plików danych do bazy danych odbywa się w bardzo wygodny sposób. Prawie wszystkie aplikacje do obsługi arkuszy kalkulacyjnych, takie jak Microsoft Excel lub OpenOffice Calc, mogą importować pliki CSV bez większego wysiłku. Dane importowane z takich plików są uporządkowane w komórkach arkusza kalkulacyjnego w celu przedstawienia ich użytkownikowi.

## Krótka historia ##

Poniżej znajduje się kilka krótkich faktów na temat pochodzenia i historii formatu plików CSV.

* 1972 - Kompilator IBM Fortran (rozszerzony poziom H) wspiera je pod OS/360

* 1978 - Wejście/wyjście kierowane na listę było obsługiwane przez FORTRAN 77, który używał przecinków i spacji jako ograniczników

* 2005 — CSV został znormalizowany za pomocą [RFC4180](https://tools.ietf.org/html/rfc4180) jako typ zawartości MIME.

* 2013 - braki RFC4180 zostały usunięte przez rekomendację W3C

* 2015 - W3C stworzyło pierwsze szkice rekomendacji dla standardów metadanych CSV, które zaczęły jako rekomendacje w grudniu 2015

## Konwertuj pliki CSV ##

Pliki CSV można konwertować do kilku różnych formatów plików za pomocą aplikacji, które mogą otwierać te pliki. Na przykład program Microsoft Excel może importować dane z pliku w formacie CSV i zapisywać je w plikach XLS, [XLSX](/pl/spreadsheet/xlsx/), [PDF](/pl/pdf/), [TXT](/pl/word-processing/txt/) , XML i [HTML](/pl/web/html/). Podobnie inne usługi stacjonarne i internetowe zapewniają możliwość eksportowania plików CSV do HTML, ODS i [RTF](/pl/word-processing/rtf/).

## Format pliku CSV ##

Wiadomo, że format pliku CSV jest określony w [RFC4180](https://tools.ietf.org/html/rfc4180). Definiuje każdy plik jako zgodny z CSV, jeśli:

* Każdy rekord znajduje się w osobnym wierszu oddzielonym znakiem końca wiersza (CRLF). Na przykład:
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* Ostatni rekord w pliku może mieć koniec wiersza lub nie. Na przykład:
* aaa, bbb, ccc CRLF
* zzz,rrrr,xxx
* Może istnieć opcjonalna linia nagłówka pojawiająca się jako pierwsza linia pliku w tym samym formacie, co normalne linie rekordu. Nagłówek ten będzie zawierał nazwy odpowiadające polom w pliku i powinien zawierać taką samą liczbę pól jak rekordy w pozostałej części pliku (obecność lub brak linii nagłówka należy wskazać za pomocą opcjonalnego parametru „header” tego pliku typu MIME). Na przykład:
* nazwa_pola,nazwa_pola,nazwa_pola CRLF
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* W nagłówku i każdym rekordzie może znajdować się jedno lub więcej pól oddzielonych przecinkami. Każda linia powinna zawierać taką samą liczbę pól w całym pliku. Pomieszczenia są uważane za część pola i nie należy ich ignorować. Po ostatnim polu rekordu nie może występować przecinek. Na przykład:
* aaa, bbb, ccc
* Każde pole może być ujęte w podwójny cudzysłów lub nie (jednakże niektóre programy, takie jak Microsoft Excel, w ogóle nie używają podwójnych cudzysłowów). Jeśli pola nie są ujęte w podwójne cudzysłowy, podwójne cudzysłowy mogą nie pojawiać się wewnątrz pól. Na przykład:\
* „aaa”, „bbb”, „ccc” CRLF
* zzz,rrrr,xxx
* Pola zawierające podziały wierszy (CRLF), podwójne cudzysłowy i przecinki należy ująć w cudzysłowy. Na przykład:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,rrrr,xxx
* Jeśli podwójne cudzysłowy są używane do ujmowania pól, wówczas podwójny cudzysłów występujący wewnątrz pola musi być poprzedzony innym podwójnym cudzysłowem. Na przykład:
* "aaa","b""bb","ccc"

Jednak w świetle współczesnego użycia ogranicznik nie ogranicza się tylko do przecinka i może również być średnikiem, tabulatorem lub spacjami. Aplikacje, takie jak Microsoft Excel, udostępniają opcję określenia znaku separatora podczas importowania rekordów z pliku CSV.

## Bibliografia

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV – Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

