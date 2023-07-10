{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku EDB — plik bazy danych poczty Exchange",
  "description":"Poznaj format pliku EDB i interfejsy API, które mogą tworzyć i otwierać pliki EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Czym jest plik EDB?

Plik z rozszerzeniem .edb to baza danych skrzynek pocztowych utworzona przez Microsoft Exchange Server do przechowywania danych związanych z pocztą. EDB, baza danych programu Exchange, przechowuje komunikaty w toku i inne niż SMTP. EDB są również znane jako pliki bazy danych Extensible Storage Engine (ESE) i przechowują pliki przy użyciu struktury b-drzewa. Będąc plikami przechowywania, pliki EDB można konwertować na inne formaty plików przechowywania poczty, takie jak [PST](/pl/email/pst/) i [OST](/pl/email/ost/).

## Format pliku EDB

Nie ma dostępnych oficjalnych/otwartych specyfikacji formatu plików EDB, do których można się odwoływać. Poczyniono pewne postępy w zakresie inżynierii wstecznej formatu pliku, co skutkowało częściowym dekodowaniem specyfikacji. Zgodnie z nimi plik EDB składa się z:
* Nagłówek pliku — zawiera informacje o nagłówku pliku bazy danych
* Strony o stałym rozmiarze - Zawiera bazę danych składającą się z tabel i indeksów

### Nagłówek pliku bazy danych
Nagłówek pliku bazy danych znajduje się na pierwszej stronie bazy danych i ma co najmniej 668 bajtów. Nagłówek pliku zawiera „Wersję formatu pliku” i „Typ pliku” oprócz innych pól.

#### Typy plików
|Typ|Opis
---|---|
|0| Baza danych|
|1| Transmisja strumieniowa|

`Uwaga:` Identyfikatory tych typów nie są znane.

#### Wersja formatu pliku
Oryginalny format EDB powstał w kwietniu 1997 roku i od tego czasu ewoluował w celu wprowadzenia zmian.

|Data wersji|Wersja|Rewizja|opis
---|---|---|---|
|Kwiecień 1997| 0x00000620|0x00000000| Oryginalny system operacyjny w formacie Beta.|
|Maj 1997 |0x00000620|0x00000001| Dodaj kolumny w katalogu do indeksowania warunkowego i OLD.|
|Czerwiec 1997|0x00000620|0x00000002|Dodaj flagę fLocalizedText w IDB.|
|Październik 1997|0x00000620|0x00000003|Dodaj SPLIT_BUFFER do stron głównych drzewa przestrzeni.|
|Jan 1998|0x00000620|0x00000002|Przywróć wersję, aby ESE97 zachował kompatybilność w przód.|
||0x00000620|0x00000003|Dodaj nowe oznaczone kolumny do katalogu ("CallbackData" i "CallbackDependencies").|
|Maj 1998|0x00000620|0x00000004|Obsługa bardzo długich wartości (SLV): signSLV, fSLVEistnieje w dbheader.|
|Maj 1998|0x00000620|0x00000005|Nowe drzewo przestrzeni SLV.|
|Październik 1998|0x00000620|0x00000006|Mapa przestrzeni SLV.|
|Grudzień 1998|0x00000620|0x00000007|4-bajtowy IDXSEG.|
|Styczeń 1999|0x00000620|0x00000008|Nowy format kolumny szablonu.|
|Czerwiec 1999|0x00000620|0x00000009|Posortowane kolumny szablonu. Używany w Windows XP SP3|
||0x00000620|0x0000000b|Zawiera nagłówek strony z sumą kontrolną ECC używaną w Exchange|
||0x00000620|0x0000000c|Używany w systemie Windows Vista (SP0)|
||0x00000620|0x00000011|Obsługa stron 2 KiB, 16 KiB i 32 KiB.Rozszerzony nagłówek strony z dodatkowymi sumami kontrolnymi ECC.Kompresja kolumn.Wskazówki dotyczące spacji.Używany w Windows 7 (SP0)|
|Maj 1999|0x00000623|0x00000000|Nowy menedżer przestrzeni.|

### Pliki bazy danych

Plik bazy danych EDB zawiera schemat dla wszystkich tabel w bazie danych. Ponadto zawiera również rekordy dla wszystkich tabel bazy danych oraz indeksy dla tych tabel. Jego lokalizacja jest określana przez następujące identyfikatory.

* Baza danych JetCreate
* JetCreateDatabase2
* Baza danych JetAttach
* JetAttachDatabase2

Na ich podstawie stan bazy danych można ocenić w następujący sposób.

|Wartość|Identyfikator|Opis
---|---|---|
|1|JET_dbstateJustCreated|Baza danych została właśnie utworzona.|
|2|JET_dbstateDirtyShutdown|Baza danych wymaga twardego lub miękkiego odzyskiwania, aby stała się użyteczna lub przenośna. Nie należy próbować przenosić baz danych w tym stanie.|
|3|JET_dbstateCleanShutdown|Baza danych jest czysta. Bazę danych można dołączyć bez żadnych plików dziennika.|
|4|JET_dbstateBeingConverted|Baza danych jest aktualizowana.|
|5|JET_dbstateForceDetachInternal|Ta wartość jest wprowadzana w WindowsXP|
 

## Bibliografia
* [Specyfikacja pliku bazy danych Extensible Storage Engine (ESE) (EDB)](https://github.com/libyal/libesedb/tree/main/documentation)

