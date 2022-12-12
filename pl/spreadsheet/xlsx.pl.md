{
  "date" : "2019-12-10",
  "keywords" :["XLSX", "plik", "rozszerzenie", "format pliku", "Excel", "Arkusz kalkulacyjny" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się, co to jest plik XLSX i interfejsy API, które mogą tworzyć i otwierać pliki XLSX.",
  "title" :"Format pliku XLSX - Co to jest plik XLSX?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Czym jest plik XLSX?

**XLSX** to dobrze znany format dokumentów programu Microsoft Excel, który został wprowadzony przez firmę Microsoft wraz z wydaniem pakietu Microsoft Office 2007. Oparty na strukturze zorganizowanej zgodnie z konwencjami Open Packaging, jak opisano w [Część 2] (https://www. .ecma-international.org/publications/standards/Ecma-376.htm) standardu OOXML ECMA-376, nowy format to pakiet ZIP zawierający pewną liczbę plików XML. Podstawową strukturę i pliki można sprawdzić, po prostu rozpakowując plik .xlsx.

## Krótka historia formatu pliku XLSX

Format pliku XLSX został wprowadzony w 2007 roku i wykorzystuje standard Open XML zaadaptowany przez firmę Microsoft w 2000 roku. Przed XLSX powszechnie używanym formatem pliku był [XLS](/pl/arkusz kalkulacyjny/xls/), który był czysto binarnym formatem pliku. Nowy typ pliku ma dodatkowe zalety związane z małymi rozmiarami plików, mniejszymi zmianami uszkodzeń i dobrze sformatowaną reprezentacją obrazów. To było na początku 2000 roku, kiedy Microsoft zdecydował się na zmianę, aby dostosować się do standardu **Office Open XML**. Do 2007 roku ten nowy format plików stał się częścią pakietu Office 2007 i jest również stosowany w nowych wersjach pakietu Microsoft Office.

## Specyfikacje formatu plików XLSX

Oficjalna [specyfikacja formatu plików XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) jest dostępna online w firmie Microsoft. Aby zobaczyć, co znajduje się w pliku XLSX, po prostu zmień jego nazwę na plik [ZIP](/pl/compression/zip/), zmieniając jego rozszerzenie, a następnie rozpakuj go, aby wyświetlić pliki składowe tego skoroszytu programu Excel. Pusty skoroszyt po wyodrębnieniu do swoich plików zawiera następujące składowe pliki i foldery.

### [Typy_zawartości].xml ###

Jest to jedyny plik znaleziony na poziomie podstawowym podczas rozpakowywania pliku ZIP. Zawiera listę typów zawartości dla części w pakiecie. Wszystkie odniesienia do plików XML zawartych w pakiecie znajdują się w tym pliku XML.

### \_rels (folder) ###

Jest to folder Relationships zawierający pojedynczy plik XML przechowujący relacje na poziomie pakietu. Linki do kluczowych części plików Xlsx są zawarte w tym pliku jako identyfikatory URI. Te identyfikatory URI identyfikują typ relacji każdej kluczowej części z pakietem. Obejmuje to związek z głównym dokumentem biurowym znajdującym się jako xl/workbook.xml oraz innymi częściami w docProps jako właściwości podstawowe i rozszerzone.

### docProps ###

Ten folder zawiera ogólne właściwości dokumentu. Obejmują one zestaw podstawowych właściwości, zestaw rozszerzonych lub specyficznych dla aplikacji właściwości oraz miniaturowy podgląd dokumentu. Pusty skoroszyt zawiera dwa pliki w tym folderze, a mianowicie app.xml i core.xml. Plik core.xml zawiera informacje takie jak autor, data utworzenia i zapisania oraz modyfikacji. Plik App.xml zawiera informacje o zawartości pliku.

### xl (folder) ###

Jest to główny folder zawierający wszystkie szczegóły dotyczące zawartości skoroszytu. Domyślnie ma następujące foldery:

* \_rels
* motyw
* karty pracy

oraz następujące pliki xml:

* style.xml
* skoroszyt.xml

## Przykład formatu XLSX ##


Dla każdego arkusza programu Excel zawartego w skoroszycie istnieje jeden plik XML. Te pliki XML można znaleźć w folderze xl/worksheets. Wszystkie informacje zawarte w arkuszu są zorganizowane w różnych sekcjach w pliku XML. Przyjrzyjmy się przykładowemu arkuszowi ze skoroszytu, który jest pokazany na poniższej ilustracji.

{{< figure src="../XLSX file format.png" alt="Format pliku XLSX" >}}

Jak widać, ten arkusz zawiera zawartość komórek od A1 do B2 oraz obraz. Ponadto komórka G13 jest obecnie aktywną komórką w arkuszu. Przyjrzyjmy się teraz plikowi xl/worksheets/sheet1.xml, aby zobaczyć, jak te informacje są reprezentowane w pliku XML. Zawartość tego pliku XML jest pokazana poniżej.

{{< figure src="../XLSX File Format Details.png" alt="Format pliku XPS" >}}

1. Karta ma zastosowany kolor motywu. Jest wymieniony w pliku XML z tagiem<tabColor> podążając za identyfikatorem motywu.
1. Wartość tabSelected jest ustawiona na 1, co oznacza, że jest to wybrany arkusz
1. Jak widać na pierwszym obrazku powyżej, komórka G13 w arkuszu jest aktywną komórką, o której również wspomniano w pliku XML.
1. Zakładka sheetData reprezentuje dane zawarte w arkuszu. Można jednak zauważyć, że w tej sekcji nie ma nigdzie oryginalnej zawartości arkusza. Dzieje się tak, ponieważ tekst jest pośrednio odwoływany z arkusza XML „sharedStrings”. To powiązanie zapewnia, że każdy tekst jest zapisywany tylko raz i można do niego ponownie się odwoływać w celu zaoszczędzenia miejsca.
1. Obraz, jak widać, odwołuje się do identyfikatora odniesienia „rId2”

## Przyczynić się

Chcesz podzielić się czymś na temat formatów plików XLSX lub arkuszy kalkulacyjnych? Możesz opublikować swoje ustalenia w sekcji [Wiadomości dotyczące formatu pliku arkusza kalkulacyjnego](https://news.fileformat.com/t/Spreadsheet).

## Bibliografia

* [[MS-XLSX] — format pliku XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

