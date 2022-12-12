{
  "date" : "2019-12-16",
  "keywords" :["XLS", "plik", "rozszerzenie", "format pliku", "Excel", "Arkusz kalkulacyjny" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby dowiedzieć się, co to jest plik XLS i interfejsy API, które mogą je tworzyć i otwierać.",
  "title" :"Co to jest format pliku XLS? Dowiedz się od ekspertów od formatów plików!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Czym jest plik XLS?

Pliki z rozszerzeniem XLS reprezentują format binarny programu Excel. Takie pliki mogą być tworzone przez program Microsoft Excel, a także inne podobne programy do obsługi arkuszy kalkulacyjnych, takie jak OpenOffice Calc lub Apple Numbers. Plik zapisany przez program Excel jest znany jako skoroszyt, w którym każdy skoroszyt może zawierać jeden lub więcej arkuszy roboczych. Dane są przechowywane i wyświetlane użytkownikom w postaci tabeli w arkuszu i mogą obejmować wartości liczbowe, dane tekstowe, formuły, zewnętrzne połączenia danych, obrazy i wykresy. Aplikacje takie jak Microsoft Excel umożliwiają eksportowanie danych skoroszytu do kilku różnych formatów, w tym [PDF](/pl/pdf/), [CSV](/pl/spreadsheet/csv/), [XLSX](/pl/spreadsheet/xlsx/), [TXT](/pl/ edytor tekstu/txt/), [HTML](/pl/web/html/), [XPS](/pl/page-description-language/xps/) i kilka innych. Format pliku XLS został zastąpiony bardziej otwartym i ustrukturyzowanym formatem, XLSX, wraz z wydaniem programu Microsoft Excel 2007. Najnowsze wersje nadal zapewniają obsługę tworzenia i odczytywania plików XLS, chociaż XLSX jest obecnie pierwszym wyborem.

## Krótka historia

XLS został stworzony przez firmę Microsoft do użytku z programem Microsoft Excel i jest również znany jako Binary Interchange File Format (BIFF). Ten typ pliku został wprowadzony po raz pierwszy, czyniąc go częścią programu Excel dla systemu Windows w 1987 r. Specyfikacje formatu plików XLS zostały upublicznione po raz pierwszy w czerwcu 2008 r. jako wersja 1. Następnie specyfikacje były stale aktualizowane i dostępna jest najnowsza wersja jest z sierpnia 2018 r. i jest oznaczony jako wersja 8.0. Krótka historia różnych wersji formatu pliku XLS jest następująca:

* Wersja 7.0 (wydana wraz z pakietem Office 95): ta wersja programu Excel była najbardziej niezawodna i najszybsza spośród wszystkich wersji, a przepisywanie strumieni wewnętrznych zostało zaktualizowane do 32 bitów.
* Wersja 8 (wydana wraz z pakietem Office 97): VBA został wprowadzony jako język standardowy i po raz pierwszy w tej wersji uwzględniono usunięte etykiety języka naturalnego. Po raz pierwszy wprowadził również asystenta biurowego ze spinaczem do papieru.
* Wersja 9 (wydana wraz z pakietem Office 2000): W wersji 9 wprowadzono tylko niewielkie zmiany, w których asystent biurowy spinacza mógł jednocześnie trzymać wiele obiektów, co wcześniej nie było możliwe.
* Wersja 10 (wydana z pakietem Office XP): Ta wersja nie zawiera żadnych zauważalnych ulepszeń.
* Wersja 11 (wydana wraz z pakietem Office 2003): Główną aktualizacją w wersji 11 programu Excel 2003 było wprowadzenie nowych tabel.

## Specyfikacje formatu plików XLS ##

Dane są uporządkowane w pliku XLS jako strumienie binarne w postaci pliku złożonego, jak opisano w [MS-CFB]. Dane są przechowywane w pliku złożonym przy użyciu magazynów, strumieni i strumieni podrzędnych, które zawierają informacje o zawartości i strukturze skoroszytu, w tym dane skoroszytu, takie jak definicje arkuszy. Każdy strumień lub podstrumień zawiera serię rekordów binarnych. Każdy rekord binarny zawiera zero lub więcej pól strukturalnych zawierających dane ze skoroszytu. Ta sekcja zawiera krótkie omówienie struktury plików XLS, ale szczegółowe specyfikacje formatu plików można znaleźć w [Specyfikacjach tworzenia plików XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) dokument firmy Microsoft.

#### Strumień i podstrumień ####

Skoroszyt jest reprezentowany przez strumień skoroszytu. Każdy arkusz w skoroszycie jest reprezentowany przez strumienie podrzędne. Ponadto strumień podrzędny arkusza wykresu, strumień podrzędny arkusza makr lub strumień podrzędny arkusza dialogowego, który następuje po globalnym strumieniu podrzędnym. Każdy strumień binarny lub podstrumień zawierający dane ze skoroszytu MUSI być zapisany jako seria rekordów binarnych.

#### Nagrywać ####

Informacje o funkcjach w skoroszycie są przechowywane jako rekord będący sekwencją bajtów o zmiennej długości. Rekord binarny składa się z następujących trzech elementów:

**Typ rekordu:** Typ rekordu to dwubajtowa liczba całkowita bez znaku, która określa, jaki typ informacji jest określony w rekordzie oraz w jaki sposób struktura danych rekordu jest uporządkowana i ustrukturyzowana. Wartości typu rekordu MUSZĄ być wartościami z wyliczenia rekordu (sekcja 2.3) lub rekord MUSI wykorzystywać przyszłą architekturę rekordu (sekcja 2.1.6).

**Rozmiar rekordu**: Rozmiar rekordu to dwubajtowa liczba całkowita bez znaku, która określa liczbę bajtów określających całkowity rozmiar danych rekordu. Rozmiar rekordu MUSI być większy lub równy 0 i MUSI być mniejszy lub równy 8224.

**Dane rekordu:** Składnik danych rekordu zawiera pola odpowiadające określonemu typowi rekordu i obejmuje pozostałą część rekordu. Kolejność i struktura pól dla danego typu rekordu jest określona w odpowiedniej sekcji dla tego typu rekordu. Rozmiar komponentu danych rekordu MUSI być równy rozmiarowi rekordu. Pola w komponencie danych rekordu mogą zawierać proste wartości, tablice wartości, struktury kilku pól, tablice pól i tablice struktur.

#### Tabela komórek ####

Komórki to podstawowe bloki skoroszytu, które przechowują zawartość skoroszytu, taką jak tekst, formuły i dane liczbowe. Komórki przechowują zapis przechowywanych danych za pośrednictwem struktury danych zwanej tabelą komórek. Sama Tabela komórek jest przechowywana w sekwencji rekordów zgodnej z regułami CELLTABLE określonymi w dokumencie specyfikacji. Składa się z szeregu bloków rzędowych, w których rzędy są ułożone w bloki rzędowe. Każdy blok wierszy zawiera wiersze od pierwszego wiersza zawierającego dane do ostatniego wiersza zawierającego dane.

Formatowanie danych lub wierszy jest zapisywane w rekordzie wiersza dla każdego bloku wierszy. Każda komórka zawierająca dane lub pojedyncze formatowanie komórki jest reprezentowana przez rekord. Formatowanie skojarzone z komórką może pochodzić z formatowania poszczególnych komórek, formatowania wierszy, formatowania kolumn lub domyślnego formatu komórki. Kolejność pierwszeństwa formatowania to formatowanie poszczególnych komórek z najwyższym priorytetem, następnie formatowanie wierszy, następnie formatowanie kolumn, a następnie domyślny format komórek. Komórki, które nie zawierają danych i nie zawierają indywidualnego formatowania, nie są zapisywane.

#### Formuły ####

Formuła to sekwencja wartości, odwołań do komórek, nazw, funkcji lub operatorów w komórce, które razem tworzą nową wartość. Formuły są przechowywane w tokenizowanej reprezentacji znanej jako „przeanalizowane wyrażenia”. Przeanalizowane wyrażenie jest konwertowane na formułę tekstową w czasie wykonywania w celu wyświetlania i edytowania przez użytkownika. Formuły komórek są określane przez rekord Formuła. Formuły tablicowe są określone przez rekord Array. Wspólne formuły są określone przez rekord ShrFmla.

#### Wykresy ####

Arkusz wykresu określa wykres, grafikę przedstawiającą dane lub relacje między zestawami danych w formie wizualnej, a także pamięć podręczną danych wykresu, brak lokalnej kopii danych używanych w danych wykresu lub łącza do zewnętrznych źródła danych są uszkodzone. Wykres określa grupy z jedną lub dwiema osiami, zestaw osi, względem których wykreślane są dane wykresu, oraz zestaw serii, linii trendu i słupka błędów określonych na wykresie. Każda grupa osi określa od jednej do czterech grup wykresów, które określają typ wizualizacji używanej do wyświetlania danych. Każda seria, linia trendu i słupek błędu określają grupę wykresów, z którą są powiązane.

#### Metadane ####

Metadane to dodatkowe dane powiązane z określoną komórką lub jej zawartością. Metadane są rejestrowane w BIFF8 wyłącznie do celów przyszłej rozszerzalności.

#### Tabele przestawne ####

Tabela przestawna to mechanizm podsumowujący dane źródłowe w celu uzyskania przeglądu dystrybucji tych danych. W tabeli przestawnej odpowiednie kolumny danych źródłowych stają się polami, których można użyć do podsumowania danych. Gdy dane źródłowe tabeli przestawnej są danymi źródłowymi OLAP, hierarchie OLAP i niektóre inne jednostki OLAP stają się polami w tabeli przestawnej.
Tabela przestawna składa się z dwóch głównych części: pamięci podręcznej przestawnej i widoku tabeli przestawnej. Może istnieć wiele widoków tabeli przestawnej opartych na pojedynczej pamięci przestawnej innej niż OLAP.

#### Style ####

W tym omówieniu opisano sposób określania informacji o formatowaniu i ochronie komórek w arkuszu (1). Formatowanie komórki składa się z kilku zestawów właściwości:

* Właściwości czcionki (pogrubienie, kursywa, kolor czcionki, rozmiar czcionki itp.)
* Właściwości wypełnienia (kolor pierwszego planu, kolor tła, wzór, gradient itp.)
* Właściwości wyrównania (wyrównanie do lewej, do środka, do prawej itp.)
* Właściwości obramowania (lewe, prawe, górne, dolne, grube lub cienkie, kolor itp.)
* Właściwości formatowania liczb (data, godzina, liczba miejsc dziesiętnych itp.)
* Właściwości ochrony (zablokowane, ukryte itp.)

Te właściwości jako całość opisują sposób wyświetlania i drukowania określonej komórki.

## Bibliografia ##

* [[MS-XLS] — struktura binarnego formatu pliku programu Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Binarny format pliku złożonego](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

