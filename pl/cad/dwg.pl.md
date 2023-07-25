{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Format pliku", "CAD", "Otwórz", "Utwórz" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików DWG i interfejsy API, które mogą tworzyć i otwierać pliki DWG.",
  "title" :"Format Pliku DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik DWG?

Pliki z rozszerzeniem DWG reprezentują zastrzeżone pliki binarne używane do przechowywania danych projektowych 2D i 3D. Podobnie jak DXF, które są plikami ASCII, DWG reprezentuje binarny format plików dla rysunków CAD (projektowanie wspomagane komputerowo). Zawiera obraz wektorowy i metadane do reprezentacji zawartości plików CAD. Dostępne są bezpłatne przeglądarki do przeglądania plików DWG w systemie operacyjnym Windows, takie jak bezpłatna DWG TrueView firmy Autodesk. Istnieją również inne aplikacje firm trzecich, które obsługują pobieranie plików DWG. Pliki DWG zawierają informacje utworzone przez użytkownika i obejmują:

* Projekty
* Dane geometryczne
* Mapy i zdjęcia

Ten format jest powszechnie używany przez architektów, inżynierów i projektantów do różnych celów projektowych.

## Krótka historia ##

Format pliku DWG ewoluował od czasu jego oficjalnego wprowadzenia w 1982 roku. Poniżej przedstawiono krótki przegląd wydarzeń z przeszłości z perspektywy historii.

**1982:** Firma Autodesk uzyskała licencję na format pliku DWG , który został opracowany przez Mike'a Riddle'a w 1970 r. jako podstawa programu AutoCAD.

**1998:** Wraz z wydaniem programu AutoCAD R14.01 firma Autodesk dodała weryfikację plików za pomocą funkcji o nazwie DWGCHECK, która osadzała zaszyfrowaną sumę kontrolną i kod produktu, zwany znakiem wodnym firmy Autodesk, w plikach DWG tworzonych przez program.

**2006:** Firma Autodesk zmodyfikowała program AutoCAD 2007, dodając „technologię TrustedDWG” w celu osadzenia ciągu tekstowego „Autodesk DWG. Ten plik jest zaufanym plikiem DWG, który został ostatnio zapisany przez aplikację firmy Autodesk lub aplikację licencjonowaną przez firmę Autodesk” w plikach DWG. Miało to na celu pomóc użytkownikom oprogramowania Autodesk upewnić się, że te pliki zostały utworzone przez aplikację Autodesk lub RealDWG, co zdecydowanie powinno pomóc w zmniejszeniu ryzyka niezgodności.

## Struktura plików ##

DWG jest jednym z powszechnie używanych formatów plików w wielu aplikacjach i ma solidną strukturę plików. Ponieważ DWG jest formatem pliku binarnego, nie jest czytelny dla człowieka, jak zwykły format pliku ASCII [DXF](/pl/cad/dxf/). Pliki DWG zwykle zawierają informacje o współrzędnych obrazu i wszelkich powiązanych z nim metadanych. Pełne [specyfikacje](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) formatu plików DWG są dostępne do pobrania przez OpenDesign. Struktura plików w formacie DWG jest podsumowana w następujący sposób.

**Nagłówek**: Nagłówek pliku składa się ze zmiennych nagłówka DWG i informacji o cyklicznej kontroli nadmiarowej (CRC), która jest używana do wykrywania błędów. Każda podsekcja jest wyspecjalizowanym wektorem, w którym różne długości bitów są używane do reprezentowania różnych etykiet. Na przykład pierwsze 6 bitów zmiennej DWG Header oznacza ciąg wersji.

**Definicje klas:** Plik DWG może zawierać wiele klas w zależności od określonego celu pliku .dwg. Informacje, takie jak rozmiar metadanych klasy obszaru danych klasy, numer klasy i suma kontrolna oprócz innych.

**Szablon**: jest opcjonalny iw przypadku wersji R15 i R15 ta sekcja znajduje się poniżej sekcji Wolne miejsce na obiekt.

**Dopełnienie**: metadane są sufiksowane i postfiksowane o określoną liczbę bajtów, co sprawia, że starsze wersje oprogramowania AutoCAD są zgodne z nowym formatem plików DWG.

**Dane obrazu**: metadane tej sekcji zależą od określonego typu pliku .dwg. Dla użytkowników R14 i R15 ta sekcja jest opcjonalna.

**Dane obiektu**: Dane obiektu składają się z pełnej listy jednostek tabeli, wpisów słownika itp. odpowiadających istniejącej liście obiektów.

**Mapa obiektów**: Lokalizacja każdego obiektu w pliku jest określona w tej sekcji pliku. Większość metadanych w tej sekcji to uchwyty plików, które odgrywają rolę w identyfikacji i ponownym renderowaniu obiektu.

**Object Free Space**: Ta sekcja jest opcjonalna dla wszystkich użytkowników

**Drugi nagłówek**: Duplikat sekcji nagłówka pliku pod koniec pliku DWG

## Bibliografia ##

* [Specyfikacje formatu plików DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Specyfikacja pliku DWG](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG – z Wikipedii](https://en.wikipedia.org/wiki/.dwg)

