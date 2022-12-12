{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby dowiedzieć się, co to jest plik _XLSX i interfejsy API, które mogą tworzyć i otwierać pliki _XLSX.",
  "title" :"Co to jest plik _XLSX?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Co to jest plik _XLSX?

Plik z rozszerzeniem .\_xlsx jest w rzeczywistości plikiem [XLSX](/pl/spreadsheet/xlsx/), którego nazwa została zmieniona przez inną aplikację. Może się to zdarzyć w niektórych przypadkach, gdy nazwa pliku zawiera rozszerzenie . na końcu nazwy pliku. Pliki \_XLSX można otwierać w programie Microsoft Excel podobnie jak pliki XLSX, ponownie zmieniając ich nazwę na rozszerzenie .xlsx.

## Format pliku _XLSX — więcej informacji

Pliki _XLSX nie różnią się niczym od plików XLSX i wykorzystują standard Open XML przyjęty przez firmę Microsoft w 2000 roku. Przed XLSX [XLS](/pl/spreadsheet/xls/) był podstawowym formatem pliku używanym do pracy z arkuszami kalkulacyjnymi programu Excel w celu zapisywania dokumentów w formacie binarnym. Ten nowy format plików oparty na XML ma zalety, takie jak małe rozmiary plików, odporność na uszkodzenia plików i dobrze sformatowana reprezentacja obrazów. Ten nowy format plików oparty na XML stał się częścią pakietu Office 2007 i jest również realizowany w nowych wersjach Microsoft.

## Specyfikacje formatu plików \_XLSX

Ponieważ plik \_XLSX jest plikiem o zmienionej nazwie XLSX, ma on takie same specyfikacje jak plik oryginalny. Jest to po prostu plik archiwum oparty na formacie pliku archiwalnego [ZIP](/pl/compression/zip/). Jeśli chcesz zobaczyć zawartość tego archiwum, po prostu zmień nazwę pliku na rozszerzenie .zip i rozpakuj go, aby wyświetlić pliki składowe tego skoroszytu programu Excel. Pusty skoroszyt po wyodrębnieniu do swoich plików zawiera następujące składowe pliki i foldery.

### [Typy_zawartości].xml

Jest to jedyny plik znaleziony na poziomie podstawowym podczas rozpakowywania pliku ZIP. Zawiera listę typów zawartości dla części w pakiecie. Wszystkie odniesienia do plików XML zawartych w pakiecie znajdują się w tym pliku XML.

### \_rels (folder)

Jest to folder Relationships zawierający pojedynczy plik XML przechowujący relacje na poziomie pakietu. Linki do kluczowych części plików Xlsx są zawarte w tym pliku jako identyfikatory URI. Te identyfikatory URI identyfikują typ relacji każdej kluczowej części z pakietem. Obejmuje to związek z głównym dokumentem biurowym znajdującym się jako xl/workbook.xml oraz innymi częściami w docProps jako właściwości podstawowe i rozszerzone.

### docProps

Ten folder zawiera ogólne właściwości dokumentu. Obejmują one zestaw podstawowych właściwości, zestaw rozszerzonych lub specyficznych dla aplikacji właściwości oraz miniaturowy podgląd dokumentu. Pusty skoroszyt zawiera dwa pliki w tym folderze, a mianowicie app.xml i core.xml. Plik core.xml zawiera informacje takie jak autor, data utworzenia i zapisania oraz modyfikacji. Plik App.xml zawiera informacje o zawartości pliku.

### xl (folder)

Jest to główny folder zawierający wszystkie szczegóły dotyczące zawartości skoroszytu. Domyślnie ma następujące foldery:

* \_rels
* motyw
* karty pracy

oraz następujące pliki xml:

* style.xml
* skoroszyt.xml

## Bibliografia

* [MS-XLSX — format pliku .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

