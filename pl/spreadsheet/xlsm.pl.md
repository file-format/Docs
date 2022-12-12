{
  "date" : "2019-12-10",
  "keywords" :["XLSM", "plik", "rozszerzenie", "format pliku", "Makra programu Excel", "Otwórz" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby wiedzieć, co to jest plik XLSM i interfejsy API, które mogą je tworzyć i otwierać.",
  "title" :"Co to jest plik XLSM?",
  "linktitle" : "XLSM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Czym jest plik XLSM?

Pliki z rozszerzeniem XLSM to rodzaj plików Arkusz kalkulacyjny obsługujący Makra. Z punktu widzenia aplikacji makro to zestaw instrukcji służących do automatyzacji procesów. Makro służy do rejestrowania powtarzających się czynności i ułatwia wykonywanie czynności poprzez ponowne uruchomienie makra. Makra są programowane przy użyciu języka Visual Basic for Applications (VBA) firmy Microsoft z poziomu skoroszytu programu Excel przy użyciu edytora Visual Basic i można je uruchamiać/debugować bezpośrednio z tego miejsca.

Pliki XLSM są podobne do formatów plików XLM, ale są oparte na formacie Open XML wprowadzonym w pakiecie Microsoft Office 2007. Innymi słowy, XLSM to pliki [XLSX](/pl/spreadsheet/xlsx/), ale z obsługą makr. Domyślnie sam program Excel udostępnia kilka makr do wspólnego użytku. Można jednak również nagrywać własne makra z wymaganymi funkcjami.

## XLSM — nagrywanie makra ##

Program Excel zapewnia łatwe w użyciu kroki rejestrowania makra. Do pracy z makrami wymagane jest zainstalowanie narzędzi programistycznych. Gdy nagrywanie makra jest w toku, rejestrowane jest każde działanie użytkownika, które ma zostać odtworzone później. Nagrywanie makr w rzeczywistości obejmuje wszystkie kroki, które użytkownik wykonuje po rozpoczęciu nagrywania. Tak więc, jeśli po rozpoczęciu nagrywania makra pogrubisz zawartość komórki, zmienisz kursywę i ustawisz jej wyrównanie, wszystkie te polecenia zostaną zarejestrowane. Do każdego zarejestrowanego makra można również przypisać skrót do szybkiego odtwarzania w późniejszym czasie. Rejestrowanie makr generuje kod VBA w postaci makra, który można edytować za pomocą edytora Visual Basic (VBE).

## Bibliografia ##

* [Format pliku MS-XLSX](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

