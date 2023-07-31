{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Układ Strony Raportu",
  "keywords" :[ "rpl", "Układ strony raportu", "XSD", "SQL Server", "raportowanie"],
  "description":"Poznaj format strumienia RPL, który jest wewnętrznym formatem binarnym używanym przez usługi Microsoft SQL Server Reporting Services podczas kontaktowania się z kontrolkami przeglądarki.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Czym jest plik RPL? ##

Format strumienia RPL (Report Page Layout) jest wewnętrznym formatem binarnym używanym przez usługi MS SQL Server Reporting Services podczas kontaktowania się z elementami sterującymi przeglądarki w celu ograniczenia części pracy związanej z renderowaniem z serwera do kontrolki przeglądarki klienta. Deweloperzy mogą tworzyć niestandardowych projektantów raportów za pomocą RPL, który generuje RPL, a także niestandardowe renderery raportów, które przetwarzają i wyświetlają plik RPL w celu wyświetlenia raportów.

## Struktury RPL

Strumień RPL zawiera strukturę strumienia, strukturę raportu, właściwości raportu i wyliczenia. Każda struktura zawiera:

- Definicja struktury.

- Gramatyka Augmented Backus-Naur Form (ABNF) dla struktury.

- Schemat bitowy struktury.

- Definicje wszystkich pól zawartych w strukturze.

Oto krótkie uwagi na temat niektórych struktur RPL:

### Struktura strumienia
Struktura strumienia składa się z serii rekordów. Rekord zawiera zero lub więcej pól strukturalnych zawierających układ raportu.

#### Strumień RPL
Strumień RPL musi zawierać tylko jeden rekord raportu, a strumień musi być serią rekordów binarnych, które zachowują hierarchię raportu.

#### Nagrywać
Rekord jest podstawowym budulcem służącym do przechowywania informacji o raporcie. Rekord składa się z sekwencji bajtów o różnej długości. Rekord składa się z dwóch elementów:
- Typ rekordu
- Dane rekordu, które są specyficzne dla tego typu rekordu.
Typ rekordu to jeden bajt, który określa, jaki typ informacji jest określony przez rekord oraz jak uporządkowana i ustrukturyzowana jest struktura danych rekordu dotyczących rekordu. Wartość rekordu zależy od typu danych charakterystycznych dla tego rekordu.

#### Proste struktury typów danych

W poniższej tabeli zdefiniowano typy danych w strumieniu RPL.

|Opis| formatuj|
---|---|
|Char|Reprezentuje 16-bitową (2-bajtową) wartość liczbową (porządkową).|
|Bajt|Reprezentuje 8-bitową (1-bajtową) liczbę całkowitą bez znaku.|
|Int16|Reprezentuje 16-bitową (2-bajtową) liczbę całkowitą ze znakiem.|
|Pojedynczy|Reprezentuje 32-bitową (4-bajtową) wartość zmiennoprzecinkową o pojedynczej precyzji.|
|Dziesiętny|Reprezentuje 128-bitowy (16-bajtowy) typ danych.|
|DateTime|Reprezentuje 64-bitowe (8-bajtowe) kodowanie wartości daty i godziny.|
|Int64|Reprezentuje 64-bitową (8-bajtową) liczbę całkowitą ze znakiem.|
|Int32|Reprezentuje 32-bitową (4-bajtową) liczbę całkowitą ze znakiem.|
|Float|Reprezentuje 32-bitową (4-bajtową) wartość zmiennoprzecinkową pojedynczej precyzji.|
|Boolean|Reprezentuje 8-bitową (1-bajtową) logiczną wartość typu Boolean. Prawidłowe wartości to prawda (1) i fałsz (0).|
|Long|Reprezentuje 64-bitową (8-bajtową) liczbę całkowitą ze znakiem.|
|String|Wszystkie wartości ciągu w protokole MUSZĄ być UNICODE UTF-16. Domyślnie wszystkie wartości typu String zaczynają się od liczby całkowitej, która określa długość łańcucha. Wartości łańcuchowe są reprezentowane w protokole jako tablica bajtów; liczba bajtów MUSI być równa liczbie znaków w łańcuchu pomnożonej przez dwa.|

### Struktury raportów
Struktury raportów zawierają definicje i rozmiary odpowiednich struktur i elementów.

Poniższa lista określa struktury raportów:

- Raport
- Wersja
- Właściwości raportu
- Przesunięcie elementu tablicy
- Zawartość strony
- Strona
- Właściwości strony
- Układ strony
- Sekcja
- Prosta sekcja
- Sekcja mieszana
- Właściwości sekcji
Element obszaru ciała
- Element nagłówka strony
- Element stopki strony
- Element ciała
- Właściwości elementu
- Właściwości elementu współdzielonego
- Użyj wspólnych właściwości elementu
-InlineSharedElementProperties
- Właściwości NonSharedElement
- Styl
-WspólneWłaściwościStyle
- NonSharedStyleProperties
- Informacje o działaniu
- ActionInfoContent
- Akcja
- ActionImageMapAreas
- ActionInfoWithMaps
- Dynamiczne dane obrazu
- Przesunięcia konsolidacji obrazu
- Zgłoś przedmiot
- Linia
- Obraz
- ImageDataProperties
-UżyjWłaściwościSharedImageData
-InlineSharedImageDataProperties
- NonSharedImageDataProperties
- Dane obrazu
- ImageMapAreas
- ImageMapArea
- Wykres
- Panel wskaźników
- Mapa
- Prostokąt
- Podraport
- RichTextBox
- Treść akapitu
- Uruchom tekst
- Ust
- RichTextBoxStructure
- Tablica
- Zawartość Tablix
- Struktura Tablix
- Pomiary Tablix
-Szerokości kolumn
- Informacje o kolumnie
-Wysokości wierszy
- Informacje o wierszu
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Pomiary
- Pomiar
-Koniec elementu raportu

### Nieruchomości
Poniżej znajduje się lista właściwości, których można użyć w strumieniu RPL:

- ID
- Liczba kolumn
— Odstępy między kolumnami
- Unikalna nazwa
- Nazwa
- Etykieta
- Zakładka
- Podpowiedź
- Przełącz element
- Opis
- Lokalizacja
- ConsumeContainerWhiteSpace (RPL 10.6)
- Język
- Czas egzekucji
- Autor
- Automatyczne odświeżanie
- Nazwa raportu
- Wysokość strony
- Szerokość strony
- Górny margines
- Margines lewy
- Margines prawy
- Margines dolny
- Kolumny
- Nazwa Strony (RPL 10.6)
- Pochylony
- Może rosnąć
- CanShrink
- Wartość
- Przełącz stan
- Sortuj
- stan sortowania
- Formuła
- IsToggleParent
- Kod typu
- Oryginalna wartość
- Jest proste
- Przesunięcie treści
- Nazwa strumienia
Rozmiar
- Połącz z dzieckiem
- Drukuj na pierwszej stronie
- Drukuj między sekcjami (RPL 10.4)
— FormattedValueExpressionBased
- Przetwarzane z błędem
- Typ MIME obrazu
- Nazwa obrazu
- Szerokość
- Wzrost
- Rozdzielczość w poziomie
- Rozdzielczość pionowa
- RawFormat
- Hiperłącze
- ZakładkaLink
- Identyfikator przeglądania szczegółowego
-Url przeglądania szczegółowego
- Kolor ramki
-ObramowanieKolorLewy
- Kolor obramowania w prawo
- Górny kolor obramowania
-ObramowanieKolorDół
- Styl obramowania
- BorderStyleLeft
- BorderStyleRight
- Górny styl obramowania
— Styl obramowania na dole
- Szerokość granicy
- Szerokość obramowania po lewej stronie
- Szerokość obramowania w prawo
— Górna szerokość obramowania
— Szerokość obramowania na dole
Wypełnienie w lewo
Wypełnienie w prawo
Wyściółka Top
Wyściółka na dole
- Styl czcionki
- Rodzina czcionek
- Rozmiar czcionki
- Grubość czcionki
- Sformatuj
- TekstDekoracja
- Wyrównanie tekstu
- Wyrównaj w pionie
- Kolor
- Wysokość linii
- Kierunek
- Tryb pisania
- UnicodeBiDi
- Zdjęcie w tle
- Kolor tła
- Powtarzanie tła
- Język Liczbowy
— Wariant liczbowy
- Kalendarz
-Wiersze nagłówków kolumn
- Kolumny nagłówków wierszy
- ColsBeforeRowHeader
— Kierunek układu
-Ścieżka definicji
- Poziom
- MemberCellIndex
-Przesunięcie elementu komórki
- ColSpan
- Rozpiętość wierszy
- DefIndeks
— Indeks kolumny
— Indeks wierszy
- Etykieta grupy
- Rekurencyjny poziom przełączania
— Styl listy
- Poziom listy
- Numer akapitu
- Prawe wcięcie
- Lewe wcięcie
- Wiszące wcięcie
- Przestrzeń przed
- Przestrzeń po
- Pierwsza linia
- Narzut
- ZawartośćTop
- Treść pozostała
-Szerokość treści
- Wysokość treści
- Państwo
- Stan elementu komórki
- Stan elementu członkowskiego

### Wyliczenia
Poniższa lista przedstawia wyliczenia, których można użyć w strumieniu RPL:

- Opcje sortowania
- Rozmiary
-Typ kształtu
- ImageRawFormat
- Style czcionek
-Waga czcionek
- TekstDekoracje
- Wyrównania tekstu
- Pionowe wyrównania
- Wskazówki
- Tryby pisania
- UnicodeBiDiTypes
- Kalendarze
- Style obramowania
-Typy powtarzania tła
- Listy stylów
- Style znaczników
- Kod typu
- Wartości stanu
- TablixMemberStateValues
- TablixMemberDefStateValues
-RPLSize





## Bibliografia ##

- [Format strumienia binarnego układu strony raportu (RPL)](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

