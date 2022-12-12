{
  "date" : "2019-12-10",
  "keywords" :["XLSB", "plik", "rozszerzenie", "format pliku", "Binarny plik arkusza kalkulacyjnego programu Excel" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby wiedzieć, co to jest plik XLSB i interfejsy API, które mogą je tworzyć i otwierać.",
  "title" :"Co to jest plik XLSB?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Czym jest plik XLSB?

Format pliku XLSB określa format pliku binarnego programu Excel, który jest zbiorem rekordów i struktur określających zawartość skoroszytu programu Excel. Treść może zawierać nieustrukturyzowane lub częściowo ustrukturyzowane tabele liczb, tekst lub zarówno liczby, jak i tekst, formuły, połączenia danych zewnętrznych, wykresy i obrazy. W przeciwieństwie do [XLSX](/pl/spreadsheet/xlsx/) (opartego na formacie pliku Open XML), XLSB reprezentuje binarny plik skoroszytu programu Excel. Pliki XLSB można szybciej odczytywać i zapisywać, co czyni je przydatnymi do pracy z dużymi plikami. XLSB jest rzadko używany do przechowywania skoroszytów, ponieważ XLSX (a wcześniej [XLS](/pl/spreadsheet/xls/)) to najczęściej wybierane przez użytkowników formaty plików do zapisywania skoroszytów. Można go otworzyć za pomocą pakietu Microsoft Office 2007 i nowszych.

## Specyfikacje formatu pliku XLSB ##

Specyfikacje formatu plików dla formatu plików XLSB zostały upublicznione w 2008 roku jako wersja 1.0. Od tego czasu specyfikacje były kilkakrotnie aktualizowane, a najnowsza wersja specyfikacji (wersja 10.0) została opublikowana w kwietniu 2018 r. Specyfikacje są udostępniane publicznie przez firmę Microsoft jako [[MS-XLSB] — specyfikacje formatu binarnego programu Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) i powinien być konsultowany przez każdego, kto chce czytać lub zapisywać pliki w formacie XLSB.

## Struktura pliku XLSB ##

Plik XLSB to pakiet składający się z kolekcji części. Te części zawierają informacje o zawartości skoroszytu, w tym dane skoroszytu i strukturę pakietu. Niektóre części zawierają informacje przechowywane za pomocą rekordów binarnych, niektóre jako XML, podczas gdy inne zawierają informacje przechowywane jako binarny strumień bajtów. Każdy rekord binarny zawiera zero lub więcej pól strukturalnych zawierających dane ze skoroszytu.

#### Pakiet ####

Pakiet XLSB to archiwum [ZIP](/pl/compression/zip/), które musi zawierać dokładnie jedną część skoroszytu. Ta część musi być celem relacji w tej części relacji pakietowej. Część skoroszytu jest częścią początkową w dokumencie XLSB.

#### Część ####

Część to strumień bajtów z powiązanym typem zawartości, który określa naturę i typ zawartości przechowywanej w części. Niektóre części przechowują informacje w formacie binarnym, podczas gdy inne przechowują informacje w formacie XML. Sekcja [wyliczenie części](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) dokumentu specyfikacji zawiera listę prawidłowych części, typów zawartości oraz wymaganych/opcjonalnych relacji między wszystkie części w pakiecie.

#### Relacja ####

Zasób źródłowy i docelowy są połączone relacją. Związek może być:

**Relacja pakietu:** gdzie celem jest część, a źródłem jest pakiet jako całość

**Relacja między częściami:** gdzie celem jest część, a źródłem jest część pakietu

**Jawna relacja:** gdzie odwołanie do zasobu pochodzi z zawartości części źródłowej przez odwołanie do wartości atrybutu ID elementu relacji

**relacja niejawna** to relacja, która nie jest jawna

**Relacja wewnętrzna:** gdzie cel jest częścią pakietu

**Związek zewnętrzny:** gdzie celem jest zasób zewnętrzny, którego nie ma w pakiecie

#### Nagrywać ####

Rekord jest podstawowym blokiem konstrukcyjnym używanym do przechowywania informacji o funkcjach w skoroszycie. Każdy rekord binarny jest sekwencją bajtów o zmiennej długości. Rekord binarny składa się z trzech elementów:

* typ rekordu
* rozmiar rekordu i
* dane rekordu, które są specyficzne dla tego typu rekordu.

**Typ rekordu:** Typ rekordu pokazuje typ rekordu określony przez rekord. Określa również strukturę danych rekordowych specyficzną dla tego rekordu. Prawidłowe typy rekordów są wymienione w sekcji [Wyliczanie rekordów](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) dokumentu specyfikacji. Typ rekordu musi wynosić jeden lub dwa bajty i musi być większy lub równy 128 i mniejszy niż 16384.

**Rozmiar rekordu:** Rozmiar rekordu określa liczbę bajtów, która określa całkowity rozmiar danych rekordu. Ta wartość MUSI wynosić od jednego do czterech bajtów. Ta wartość MUSI być jednym bajtem, jeśli wysoki bit w młodszym bajcie jest równy 0; w przeciwnym razie ta wartość MUSI być większa niż jeden bajt. Jeśli liczba bajtów jest większa niż jeden bajt, wysoki bit w każdym kolejnym bajcie określa, czy używany jest dodatkowy bajt. Jeśli starszy bit drugiego bajtu jest równy 1, to ta wartość MUSI wykorzystywać dodatkowy trzeci bajt. Jeśli starszy bit trzeciego bajtu jest równy 1, to ta wartość MUSI wykorzystywać dodatkowy czwarty bajt. Wysoki bit czwartego bajtu MUSI zostać zignorowany. Wartość składa się z siedmiu młodszych bitów każdego bajtu łącznie. Młodsze, najmniej znaczące bity są zawarte w pierwszym bajcie, a każdy kolejny bajt zawiera bity wyższego rzędu niż poprzedni bajt.

**Dane rekordu:** Składnik danych rekordu zawiera pola odpowiadające określonemu typowi rekordu i obejmuje pozostałą część rekordu. Kolejność i struktura pól dla danego typu rekordu na liście Wyliczanie rekordów jest określona w odpowiedniej sekcji dla tego typu rekordu w Rekordach. Całkowity rozmiar komponentu danych rekordu MUSI być równy rozmiarowi rekordu. Pola w komponencie danych rekordu mogą zawierać proste wartości, tablice wartości, struktury kilku pól, tablice pól i tablice struktur.

#### Przykład rekordu XLSB ####

Poniższy typ i rozmiar rekordu określają rekord **BrtCommentText** o rozmiarze 200 bajtów:

11111101 00000100 11001000 00000001 [Pola zapisu]

Pierwszy bajt to 11111101, określający niską wartość 125 i że typ rekordu wymaga drugiego bajtu. Drugi bajt to 00000100, określający wysoką wartość 4 * 128, co odpowiada 512. Wartość typu rekordu to 125 + 512 lub 637, co odpowiada typowi rekordu **BrtCommentText**. Następny bajt to 11001000, określający niską wartość 72 i że rozmiar rekordu wymaga drugiego bajtu. Drugi bajt to 00000001, określający wyższą wartość 1 * 128, a rozmiar rekordu nie wymaga dodatkowego bajtu. Rozmiar rekordu to 72 + 128 lub 200, co określa całkowity rozmiar w bajtach składnika danych rekordu. Pola w komponencie danych rekordu są określone przez **BrtCommentText**.

## Bibliografia ##

* [[MS-XLSB] — binarny format pliku programu Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

