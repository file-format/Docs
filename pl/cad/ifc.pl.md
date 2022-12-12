{
  "date" : "2020-03-16",
  "keywords" :[ "Plik IFC", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku IFC i interfejsy API, które mogą tworzyć i otwierać pliki IFC.",
  "title" :"Format Pliku IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik IFC?

Pliki z rozszerzeniem IFC odnoszą się do formatu plików Industry Foundation Classes (IFC), który ustanawia międzynarodowe standardy importowania i eksportowania obiektów budowlanych oraz ich właściwości. Ten format pliku zapewnia współdziałanie różnych aplikacji. Specyfikacje dla tego formatu plików są opracowywane i utrzymywane przez buildingSMART International jako jej standard danych. Ostatecznym celem formatu plików IFC jest poprawa komunikacji, produktywności, czasu dostawy i jakości w całym cyklu życia budynku.

Dzięki ustalonym standardom dla typowych obiektów w budownictwie zmniejsza utratę informacji podczas transmisji z jednej aplikacji do drugiej. IFC może przechowywać dane dotyczące geometrii, obliczeń, ilości, zarządzania obiektami, wyceny itp. Dla wielu różnych zawodów (architekci, elektrycy, HVAC, konstrukcyjni, terenowi itp.).

## Krótka historia ##

Inicjatywa IFC została podjęta w 1994 roku przez Autodesk w celu wspierania zintegrowanego rozwoju aplikacji i obejmowała takie firmy jak Honeywell, Butler Manufacturing i AT&T. W 1995 roku członkostwo zostało otwarte dla każdego, a nazwa została zmieniona na International Alliance for Interoperability. Intencją organizacji non-profit było opublikowanie klasy Industry Foundation Class (IFC) jako modelu produktu AEC. W 2005 roku nazwa została ponownie zmieniona i teraz buildSMART ją utrzymuje.

## Format pliku IFC ##

Format pliku IFC przeszedł kilka zmian w przeszłości, aby osiągnąć specyfikację formatu pliku v4. Od czasu do czasu pojawiało się kilka drobnych zmian, które zostały włączone do specyfikacji jako dodatki. Poniżej znajduje się lista różnych wersji specyfikacji plików, które zostały upublicznione w przeszłości.

* IFC4 Dodaj2 (2016) IFC4 Dodaj1 (2015)
* IFC4 (marzec 2013) ifcXML2x3 (czerwiec 2007)
* IFC2x3 (luty 2006) ifcXML2 dla IFC2x2 add1 (RC2)
* IFC2x2 Dodatek 1 (lipiec 2004)ifcXML2 dla IFC2x2 (RC1)
* IFC 2x2IFC 2x Dodatek 1ifcXML1 dla IFC2x i
* IFC2x Dodatek 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Najnowsze wersje specyfikacji formatu plików IFC są zawsze dostępne na stronie internetowej buildingSMART, a programiści powinni zapoznać się z nimi w przypadku każdego rodzaju aplikacji, które planują opracować. W chwili pisania tego artykułu specyfikacje wersji 4 są najnowszymi dostępnymi online.

### Formaty plików danych IFC ###

Format pliku IFF obsługuje wymianę danych między aplikacjami przy użyciu różnych formatów wymienionych poniżej:

**IFC:** Jest to domyślny format wymiany IFC i wykorzystuje fizyczną strukturę plików STEP zgodnie z normą ISO 10303-21. Ten format pliku ma rozszerzenie pliku .ifc i jest najczęściej używanym formatem IFC.

**IFC-XML:** Jest to plik IFC w formacie XML, który może być generowany bezpośrednio przez aplikację wysyłającą zgodnie ze strukturą ISO 10303-28, zwaną także STEP-XML. Format pliku IFC-XML jest uważany za odpowiedni do współdziałania narzędzi XML. W porównaniu z formatem pliku IFC, format IFC-XML jest o 300-400% większy.

**IFC-ZIP:** Jest to skompresowana [ZIP](/pl/compression/zip/) wersja IFC lub IFC-XML, w której jeden z tych plików znajduje się w głównym katalogu archiwum zip. Ten format kompresuje plik .ifc o 60-80%, a plik .ifc XML o 90-95%.

### Architektura IFC ###

Specyfikacja IFC zawiera terminy, koncepcje i elementy specyfikacji danych, które pochodzą z zastosowania w dyscyplinach, branżach i zawodach sektora budowlanego i zarządzania obiektami. Terminy i pojęcia wykorzystują proste angielskie słowa, pozycje danych w specyfikacji danych są zgodne z konwencją nazewnictwa.

nazwy elementów danych dla typów, podmiotów, reguł i funkcji zaczynają się od przedrostka „Ifc” i są kontynuowane przez angielskie słowa w konwencji nazewnictwa CamelCase (bez podkreślenia, pierwsza litera w słowie wielkimi literami); nazwy atrybutów w jednostce są zgodne z konwencją nazewnictwa CamelCase bez przedrostka; definicje zestawów właściwości, które są częścią tego standardu, zaczynają się od przedrostka „Pset_” i kontynuują angielskimi słowami w konwencji nazewnictwa CamelCase; definicje zestawów ilości, które są częścią tego standardu, zaczynają się od przedrostka „Qto_” i kontynuują angielskimi słowami w konwencji nazewnictwa CamelCase.

Architektura schematu danych IFC definiuje cztery warstwy pojęciowe, każdy indywidualny schemat jest przypisany do dokładnie jednej warstwy pojęciowej.

**Warstwa zasobów** — najniższa warstwa obejmuje wszystkie indywidualne schematy zawierające definicje zasobów, definicje te nie zawierają globalnie unikalnego identyfikatora i nie mogą być używane niezależnie od definicji zadeklarowanej w warstwie wyższej;

**Warstwa rdzenia** — następna warstwa obejmuje schemat jądra i schematy rozszerzeń rdzenia, zawierające najbardziej ogólne definicje jednostek, wszystkie jednostki zdefiniowane w warstwie rdzenia lub wyższej posiadają globalnie unikalny identyfikator i opcjonalnie informacje o właścicielu i historii;

**Warstwa interoperacyjności** — następna warstwa obejmuje schematy zawierające definicje jednostek, które są specyficzne dla ogólnej specjalizacji produktu, procesu lub zasobów używanej w kilku dyscyplinach. Definicje te są zwykle wykorzystywane do wymiany między domenami i udostępniania informacji konstrukcyjnych;

**Warstwa domenowa** — najwyższa warstwa zawiera schematy zawierające definicje jednostek, które są specjalizacjami produktów, procesów lub zasobów specyficznych dla określonej dziedziny, definicje te są zwykle wykorzystywane do wymiany informacji wewnątrz domeny.

## Bibliografia ##

* [Industry Foundation Classes – Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

