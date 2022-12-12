{
  "date" : "2019-12-10",
  "keywords" :["XLM", "plik", "rozszerzenie", "format pliku", "Plik makr Microsoft Excel", "Arkusz kalkulacyjny"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby dowiedzieć się, co to jest plik makr XLM i interfejsy API, które mogą tworzyć i otwierać pliki XLM.",
  "title" :"Co to jest plik XLM?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Czym jest plik XLM?

XLM, dla programu Excel Macro, to rodzaj plików arkuszy kalkulacyjnych, które służą do przechowywania makr. Z punktu widzenia aplikacji makro to zestaw instrukcji służących do automatyzacji procesów. Makro służy do rejestrowania powtarzających się kroków w formacie pliku [XLS](/pl/spreadsheet/xls/) i ułatwia wykonywanie czynności poprzez ponowne uruchomienie makra. Makra są programowane przy użyciu Visual Basic for Applications (VBA) firmy Microsoft z poziomu skoroszytu programu Excel przy użyciu edytora Visual Basic i można je uruchamiać/debugować bezpośrednio z tego miejsca.

## Krótka historia ##

Microsoft Excel wspierał programowanie makr od pierwszego publicznego uruchomienia. Funkcje makr pozostały takie same w kolejnych wersjach programu Excel z rozszerzeniem o nowe funkcje. XLM był domyślnym językiem makr dla programów Excel do wersji Excel 4.0. Excel 5.0 domyślnie nagrywał makra w VBA, ale w wersji 5.0 nagrywanie XLM było nadal dozwolone jako opcja. Po wersji 5.0 ta opcja została wycofana. Wszystkie wersje programu Excel, w tym Excel 2010, umożliwiają uruchamianie makr XLM, chociaż firma Microsoft odradza ich używanie.

## Nagrywanie makra w formacie XLM ##

Program Excel zapewnia łatwe w użyciu kroki rejestrowania makra. Do pracy z makrami wymagane jest zainstalowanie narzędzi programistycznych. Gdy nagrywanie makra jest w toku, rejestrowane jest każde działanie użytkownika, które ma zostać odtworzone później. Nagrywanie makr w rzeczywistości obejmuje wszystkie kroki, które użytkownik wykonuje po rozpoczęciu nagrywania. Tak więc, jeśli po rozpoczęciu nagrywania makra pogrubisz zawartość komórki, zmienisz kursywę i ustawisz jej wyrównanie, wszystkie te polecenia zostaną zarejestrowane. Do każdego zarejestrowanego makra można również przypisać skrót do szybkiego odtwarzania w późniejszym czasie. Rejestrowanie makr generuje kod VBA w postaci makra, który można edytować za pomocą edytora Visual Basic (VBE).

## Model obiektowy programu Excel ##

Makra używają w tym celu procedur VBA i stosują się do [modelu obiektowego programu Excel](https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model). Ten model identyfikuje obiekty arkusza kalkulacyjnego do interakcji z arkuszem kalkulacyjnym za pomocą zdefiniowanych przez użytkownika pasków narzędzi poleceń, pasków poleceń lub okien komunikatów. Na przykład dostęp do właściwości skoroszytu jest udzielany za pomocą obiektu Workbook. Podobnie w modelu istnieje obiekt Worksheet do programistycznej pracy z arkuszami skoroszytu.

## Makra i bezpieczeństwo ##

VBA umożliwia dostęp do wszystkich obszarów aplikacji, a także systemu plików, a także może być niebezpieczny. Budzi to obawy podczas udostępniania skoroszytu komuś, kto może uruchomić plik na swoim końcu. Oznacza to, że Microsoft Excel ostrzega przed otwarciem takiego pliku. Makra mogą być certyfikowane podpisem cyfrowym, aby inni użytkownicy mogli zweryfikować, czy są one godne zaufania. Dzięki temu makra można włączyć po weryfikacji ich źródła.

## Bibliografia ##

* [[MS-XLS] — struktura binarnego formatu pliku programu Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Programowanie makr](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

