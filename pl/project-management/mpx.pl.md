{
  "date" : "2019-10-11",
  "keywords" :[ "plik mpx", "format pliku mpx", "co to jest plik mpx", "plik", "przykład mpx", "rozszerzenie pliku mpx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX — format pliku programu Microsoft Project Exchange",
  "description":"Poznaj format plików MPX i interfejsy API, które mogą tworzyć i otwierać pliki MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Czym jest plik MPX? ##

Plik z rozszerzeniem .mpx to format pliku programu Microsoft Exchange. Format pliku MPX został opracowany przez firmę Microsoft Project (MSP) w celu ułatwienia wymiany informacji o projekcie między MSP a innymi aplikacjami obsługującymi format pliku MPX, w tym Primavera Project Planner, Sciforma i Timerline Precision Estimating. Korzystając z plików MPX, możesz przenosić wszelkiego rodzaju informacje z projektu do innego systemu, takie jak szczegółowe informacje o przydziale zasobów, informacje z kalendarza lub informacje z okna dialogowego Informacje o projekcie.

Program Microsoft Project 4.0 wprowadził obsługę tworzenia i odczytywania formatów plików MPX, które nadal były używane w programie Microsoft Project 98. Jednak obsługa tworzenia plików MPX została wycofana z wydania programu Microsoft Project 2000, a wersje do programu Microsoft Project 2010 obsługują tylko odczyt MPX. Format pliku MPX nie jest obsługiwany w wersjach późniejszych niż MSP 2010.

## Format pliku MPX ##

W tej sekcji podano przegląd specyfikacji plików MPX. Pełne specyfikacje można znaleźć w tej [Bazie wiedzy](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) artykuł i można się do niego odnieść w celu uzyskania szczegółowych informacji.

### Rekordy ###

Zapis pliku MPX zawiera informacje dotyczące projektu. Istnieją różne typy rekordów, w których każdy rekord ma swoją własną kolejność. Każdy typ rekordu jest identyfikowany przez jego numer rekordu. W przypadku pliku MPX konieczne jest, aby zawierał typ rekordu Utworzenie pliku. Inne rodzaje ewidencji nie są obowiązkowe. W poniższej tabeli przedstawiono wszystkie typy rekordów, ich numery rekordów oraz liczbę rekordów, które każdy typ może zawierać w pliku MPX. Włączanie rekordów do pliku MPX musi być zgodne z kolejnością w tabeli, z komentarzami wstawianymi w dowolnym miejscu.

|Nazwa rekordu|Numer rekordu|Maksymalna liczba rekordów
---|---|---|
|Tworzenie pliku (wymagane)|brak|1
|Ustawienia waluty|10|1
|Ustawienia domyślne|11|1
|Ustawienia daty i godziny|12|1
|Definicja kalendarza bazowego|20|250
|Podstawowe godziny kalendarzowe|25| 7 na rekord definicji kalendarza podstawowego
|Wyjątek kalendarza bazowego|26| 250 na rekord definicji kalendarza podstawowego
|Nagłówek projektu|30|1
|Definicja tabeli zasobów tekstowych|140|1- (Możesz też użyć rekordu Definicja tabeli zasobów liczbowych)
|Definicja tabeli zasobów numerycznych|41|1
|Zasoby|50|9999
|Uwagi dotyczące zasobów|51| 1 na rekord zasobu
|Definicja kalendarza zasobów|55| 1 na rekord zasobu
|Godziny w kalendarzu zasobów|56| 7 na kalendarz zasobów
|Wyjątek kalendarza zasobów| 57|250 na kalendarz zasobów
|Tekstowa definicja tabeli zadań|60|1 (Możesz też użyć rekordu Numeryczna definicja tabeli zadań)
|Definicja numerycznej tabeli zadań|61|1
|Zadanie|70|9
|Notatki do zadań|71| 1 na rekord zadania
|Zadanie cykliczne|72| 1 na rekord zadania
|Przydział zasobów|75| 100 na rekord zadania
|Pola grupy roboczej przydziału|76| 1 na rekord Przydziału
|Nazwy projektów|80|500
|Łącza klienckie DDE i OLE|81|500
|Komentarze|0|bez ograniczeń

### Struktura plików ###

Plik MPX składa się z wyżej wymienionych rekordów, które są ułożone w określony sposób w pliku. Szczegóły dotyczące tych typów rekordów omówiono w następujący sposób:

**Rekord utworzenia pliku (FCR):** Jest to obowiązkowy zapis, którego celem jest identyfikacja:

* Format pliku (MPX)
* Znak separatora listy używany w pliku
* Program i numer wersji użyty do utworzenia pliku
* Numer wersji formatu pliku MPX użytego w pliku
* Strona kodowa użyta do utworzenia pliku

Musi to być pierwszy rekord w pliku. Podczas eksportowania z programu Microsoft Project znak separatora listy jest określany w elemencie Ustawienia regionalne w Panelu sterowania systemu Windows. Rekord FCR zawiera następujące pola:

* MPX, po którym bezpośrednio następuje znak separatora listy
* Nazwa/identyfikator programu
* Numer wersji pliku
* Strona kodowa (850, 437, MAC, ANSI)

Na przykład rekord może zawierać informacje **MPX, Microsoft Project, 3.0**, które określają, że w tym pliku MPX jako separatora listy używany jest przecinek. Wersja formatu MPX używana w pliku jest eksportowana z programu Microsoft Project w wersji 3.0.

**Ustawienia waluty** Ten rekord o numerze 10 określa ustawienia opcji walutowych w oknie dialogowym Opcje. Jeśli ten rekord nie jest uwzględniony, używane są bieżące ustawienia w oknie dialogowym Opcje. Separatory tysięcy i dziesiętnych są określone w elemencie Ustawienia regionalne w Panelu sterowania systemu Windows.
Pola zawarte w tym rekordzie to:

* Symbol waluty
* Pozycja symbolu (0 # po, 1 # przed, 2 # po ze spacją, 3 # przed ze spacją)
* Cyfry waluty (0,1,2)
* Separator tysięcy
* Separator liczb dziesiętnych

**Przykład:** 10,$,1,2,",",.
Ten przykład określa, że wartości walutowe mają przed sobą znak dolara ($), że dwie cyfry są umieszczane po przecinku, że przecinek jest używany do oddzielania tysięcy, a kropka jest używana jako kropka dziesiętna. Ponieważ znak separatora listy jest zawarty w polu Separator tysięcy, pole jest otoczone cudzysłowami.

**Ustawienia domyślne:** Ten rekord, o numerze 11, określa ustawienia opcji domyślnych w oknie dialogowym Opcje. Jeśli czas trwania nie jest określony, należy ustawić domyślną jednostkę czasu trwania, aby obliczenia jednostek czasu trwania były prawidłowe. Jeśli ten rekord nie jest uwzględniony, używane są bieżące ustawienia w oknie dialogowym Opcje.
Pola zawarte w tym rekordzie to:

* Domyślne jednostki czasu trwania (0 # minut, 1 # godzin, 2 # dni, 3 # tygodni)
* Domyślny typ czasu trwania (0 # nie naprawiono, 1 # naprawiono)
* Domyślne jednostki pracy (0 # minut, 1 # godzin, 2 # dni, 3 # tygodni)
* Domyślne godziny/dzień
* Domyślne godziny/tydzień
* Domyślna stawka standardowa
* Domyślna stawka za nadgodziny
* Aktualizacja statusu zadania aktualizuje status zasobu (0 # nie, 1 # tak)
* Podziel zadania w toku (0 # nie, 1 # tak)

**Ustawienia daty i godziny:** Ten rekord, o numerze rekordu 12, określa ustawienia opcji daty i godziny w oknie dialogowym Opcje oraz opcji Format daty tekstu paskowego w oknie dialogowym Układ. Jeśli ten rekord nie jest uwzględniony, używane są bieżące ustawienia w oknie dialogowym Opcje.
\\Pola zawarte w tym rekordzie to:

* Kolejność dat (0 # miesiąc/dzień/rok, 1 # dzień/miesiąc/rok, 2 # rok/miesiąc/dzień)
* Format czasu (0 # 12 godzin, 1 # 24 godziny)
* Czas domyślny (liczba minut po północy)
* Separator daty
* Separator czasu
* 0:00 do 11:59 Tekst
* 12:00 do 23:59 Tekst
* Format daty (0 -14)*
* Format daty tekstu słupkowego (0 -194)*

**Definicja kalendarza bazowego:** Rekordy te, posiadające numer rekordu 20, definiują kalendarze bazowe oraz ich robocze i wolne dni tygodnia. W przypadku braku wpisu w danym dniu stosowane są ustawienia domyślne. Domyślne ustawienia to od poniedziałku do piątku dla dni roboczych oraz sobota i niedziela dla dni wolnych od pracy. W tym rekordzie pole Nazwa jest wymagane. Dla każdego z dni wpis 0 oznacza, że dzień jest dniem wolnym od pracy, a wpis 1 oznacza, że dzień jest dniem roboczym.
Pola zawarte w tym rekordzie to:

* Nazwa
* Niedziela
* Poniedziałek
* Wtorek
* Środa
* Czwartek
* Piątek
* Sobota

**Podstawowe godziny kalendarzowe:** Rekordy te, posiadające numer rekordu 25, określają godziny pracy dla dni tygodnia, jeśli różnią się one od ustawień domyślnych. Domyślne godziny pracy to od 8:00 do 12:00 i od 13:00 do 17:00. Każdy rekord Godziny kalendarza podstawowego odnosi się do poprzedniego rekordu Definicja kalendarza podstawowego. Po każdym rekordzie definicji kalendarza podstawowego może występować maksymalnie siedem takich rekordów.

* Dzień tygodnia (1 - 7, gdzie 1 # niedziela i 7 # sobota)
* Od czasu 1
* Do czasu 1
* Od czasu 2
* Do czasu 2
* Od czasu 3
* Do czasu 3

**Wyjątek kalendarza podstawowego:** Rekordy te, mające numer rekordu 26, określają wyjątki od dni i godzin określonych w poprzednich dwóch typach rekordów. Po każdym rekordzie definicji kalendarza podstawowego może znajdować się do 250 takich rekordów. Zapisy te muszą być wymienione w porządku chronologicznym. Jeśli wyjątek dotyczy jednego dnia, pole Do daty można pozostawić puste. Jeśli nie podano żadnych godzin, używane są godziny domyślne od 8:00 do 12:00 i od 13:00 do 17:00.
Pola zawarte w tym rekordzie to:

* Od daty
* Spotykać się z kimś
* Niepracujący/Pracujący (0 # niedziałający, 1 # pracujący)
* Od czasu 1
* Do czasu 1
* Od czasu 2
* Do czasu 2
* Od czasu 3
* Do czasu 3

**Nagłówek projektu:** Ten rekord o wartości rekordu 30 ustawia globalne pola projektu, takie jak data rozpoczęcia projektu i data zakończenia projektu. Pola w tym rekordzie odpowiadają informacjom w oknach dialogowych Informacje o projekcie i Statystyki.
Pola i karty zawarte w tym rekordzie to:

* Zakładka Projekt
* Firma
* Menedżer
* Kalendarz (standard używany, jeśli nie ma wpisu)
* Data rozpoczęcia (to pole lub następne pole jest obliczane dla importowanego pliku, w zależności od ustawienia Zaplanuj od)
* Data zakończenia
* Zaplanuj od (0 # start, 1 # koniec)
* Bieżąca data*
* Uwagi
* Koszt
* Koszt bazowy
* Aktualna cena
* Praca
* Praca podstawowa
* Rzeczywista praca
* Praca
* Czas trwania*
*Czas trwania linii bazowej*
* Rzeczywisty czas trwania
* Procent ukończenia
* Początek linii bazowej
* Wykończenie linii bazowej
* Rzeczywisty początek
* Rzeczywiste wykończenie
* Rozpocznij wariancję
* Wariancja wykończenia
* Temat
* Autor
* Słowa kluczowe

**Definicja tabeli zasobów tekstowych**: Ten rekord zawiera listę pól zasobów, w kolejności, które są importowane lub eksportowane. W przypadku importowanych plików nazwy muszą być zgodne z nazwami pól używanymi w programie Microsoft Project. W przypadku eksportowanych plików ten rekord pochodzi z tabeli eksportu zasobów. Należy użyć tego rekordu lub rekordu definicji tabeli zasobów numerycznych. Podczas eksportowania z programu Microsoft Project uwzględniane są oba te rekordy.

**Definicja tablicy zasobów liczbowych:** Ten rekord zawiera liczby, a nie nazwy, w kolejności, w której pola zasobów są importowane lub eksportowane. Jest to alternatywna metoda identyfikowania pól zasobów zawartych w każdym rekordzie zasobu i jest przydatna podczas definiowania pliku MPX utworzonego przez produkt w języku obcym.

**Zasób:** te rekordy zawierają informacje o każdym importowanym lub eksportowanym zasobie. Każdy rekord zasobu opisuje jeden zasób. Podczas importowania informacji uwzględnione pola są definiowane przez rekord Definicja tabeli zasobów tekstowych lub rekord Definicja tabeli zasobów liczbowych. Podczas eksportowania informacji uwzględniane są pola wymienione w tabeli Eksport zasobów.

**Uwagi dotyczące zasobu:** Te rekordy zawierają uwagi dotyczące bezpośrednio poprzedzającego rekordu zasobu. W przypadku nowej linii w notatce używany jest znak ASCII 127. Jeśli uwaga zawiera znak separatora listy, należy ją ująć w cudzysłowy.

**Definicja kalendarza zasobów:** Te rekordy definiują dni robocze dla zasobu określonego w bezpośrednio poprzedzającym rekordzie zasobu. W przypadku plików importowanych, jeśli w polu Nazwa kalendarza podstawowego nie ma wpisu, używana jest opcja Standard. Brak wpisu dla określonego dnia oznacza, że dzień jest ustawiony jako domyślny (2). Jeśli nie ma żadnych rekordów definicji kalendarza zasobów, standardowy jest używany jako kalendarz bazowy dla zasobu, a domyślnie używane są dni. Dla każdego dnia wpis 0 wskazuje, że dzień jest dniem wolnym od pracy, 1 wskazuje, że dzień jest dniem roboczym, a 2 określa, że używana jest wartość domyślna.

**Godziny kalendarza zasobu:** te rekordy definiują godziny pracy zasobu, które różnią się od kalendarza bazowego używanego przez zasób. Rekordy te dotyczą rekordu Definicja kalendarza zasobów bezpośrednio poprzedzającego ten rekord. Po każdym rekordzie definicji kalendarza zasobów można śledzić maksymalnie siedem takich rekordów.

**Wyjątek kalendarza zasobów:** Te rekordy definiują wyjątki od dni i godzin określonych w poprzednich dwóch typach rekordów. Do 250 takich rekordów może następować po każdym rekordzie definicji kalendarza zasobów. Zapisy te muszą być wymienione w porządku chronologicznym. Jeśli wyjątek dotyczy tylko jednego dnia, pole Do dnia można pozostawić puste. Jeśli nie podano żadnych godzin, używane są godziny domyślne od 8:00 do 12:00 i od 13:00 do 17:00.

**Definicja tabeli zadań tekstowych:** Ten rekord zawiera listę pól zadań, które są importowane lub eksportowane w kolejności. W przypadku importowanych plików nazwy muszą być zgodne z nazwami pól używanymi w programie Microsoft Project. Jeśli plik jest eksportowany, ten rekord pochodzi z zadania Eksportuj tabelę. Podczas eksportowania z programu Microsoft Project uwzględniane są oba te rekordy. Pola obliczane przez program Microsoft Project, takie jak Zaplanowane rozpoczęcie i Zaplanowane zakończenie, są ignorowane po zaimportowaniu. Jeśli masz ustalone daty rozpoczęcia lub zakończenia zadania, użyj pól Typ ograniczenia i Data ograniczenia.

**Definicja numerycznej tabeli zadań:** Używając liczb zamiast nazw, ten rekord zawiera listę pól zadań, które są importowane lub eksportowane w kolejności. Jest to alternatywna metoda identyfikowania pól zadań zawartych w każdym rekordzie Zadania i jest przydatna podczas definiowania pliku MPX utworzonego przez produkt w języku obcym.

**Zadanie:** Te rekordy zawierają informacje o każdym importowanym lub eksportowanym zadaniu. Każdy rekord zadania opisuje jedno zadanie. Podczas importowania informacji uwzględnione pola są definiowane przez rekord Definicja tabeli zadań tekstowych lub rekord Definicja liczbowej tabeli zadań. Podczas eksportowania informacji uwzględniane są pola wymienione w tabeli eksportu zadania.

**Notatki do zadania:** Te rekordy zawierają uwagi dotyczące bezpośrednio poprzedzającego rekordu zadania. Użyj znaku ASCII 127, aby wskazać nową linię w notatce. Jeśli uwaga zawiera znak separatora listy, należy ją ująć w cudzysłowy.

**Przydział zasobów**: te rekordy zawierają informacje o zasobach przypisanych do zadania, które zostało zdefiniowane w poprzednim rekordzie zadania. Jeśli scalasz pliki i chcesz zachować informacje o przydziale zasobów, musisz dołączyć te informacje do pliku MPX. W przypadku scalenia wszystkie istniejące przypisania do scalonych zadań zostaną usunięte. Jeśli scalasz pliki na podstawie unikalnych identyfikatorów, zasoby są przydzielane przy użyciu unikatowych identyfikatorów zasobów, a nie identyfikatorów.

**Pola grupy roboczej przydziału zasobów:** Te rekordy zawierają informacje przechowywane z każdym przydziałem dla funkcji grupy roboczej programu Microsoft Project 4.0 i 4.1. Jeśli korzystasz z funkcji grupy roboczej, musisz dołączyć ten rekord, aby upewnić się, że żadne informacje nie zostaną utracone.

**Nazwy projektów:** Te rekordy zawierają listę wszystkich nazw łączy DDE przechowywanych w projekcie.

**Łącza klienta DDE i OLE:** Te rekordy zawierają listę łączy DDE do projektu.

**Komentarze:** Rekordy te mogą służyć do dodawania komentarzy do pliku i mogą pojawiać się w dowolnym miejscu w pliku. Każdy rekord komentarzy musi zaczynać się od „0”.

## Problemy z otwarciem pliku MPX ##

Oto lista typowych problemów, które mogą wystąpić i spowodować nieprawidłowe działanie formatu MPX:

* Brak oprogramowania pomocniczego
* Uszkodzony plik
* Zainfekowany plik z powodu wirusa
* Brak prawa dostępu w systemie do otwierania plików
* Przestarzały dysk w twoim systemie
* Zmieniono nazwę rozszerzenia pliku

## Bibliografia ##

* [MPX — Baza wiedzy firmy Microsoft](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

