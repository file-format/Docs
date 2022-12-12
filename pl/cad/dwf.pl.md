{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Format pliku", "Otwórz", "Odczyt", "Utwórz", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku DWF i interfejsy API, które mogą tworzyć i otwierać pliki DWF.",
  "title" :"Format Pliku DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik DWF?

Design Web Format (DWF) reprezentuje rysunki 2D/3D w skompresowanym formacie do przeglądania, przeglądania lub drukowania plików projektowych. Zawiera grafikę i tekst jako część danych projektowych i zmniejsza rozmiar pliku ze względu na jego skompresowany format. Zmniejszony rozmiar pliku sprawia, że dystrybucja i komunikacja bogatych danych projektowych jest wydajna. DWF nie wymaga od odbiorcy wiedzy o użyciu oprogramowania CAD, które stworzyło oryginalny rysunek. Zawartość pliku w formacie DWF może być prosta i obejmować tylko jeden arkusz lub na tyle złożona, że zawiera czcionki, kolory i obrazy.

## Krótka historia ##

Firma Autodesk wprowadziła format plików DWF w 1995 roku jako część wtyczki WHIP do Netscape Navigation. Format ewoluował z formatu tylko 2D, aby zawierać treści 3D wraz z upływem czasu. Wiele aplikacji innych firm również korzysta z tego formatu.

## Format pliku DWF ##

DWF to otwarty, bezpieczny format zaprojektowany specjalnie do udostępniania bogatych danych projektowych. Jest niezależny od oryginalnego oprogramowania użytkowego, sprzętu i systemu operacyjnego użytych do utworzenia tych danych projektowych. Dzięki temu członkowie zespołu, którzy nie używają aplikacji CAD, mogą uczestniczyć w cyfrowych procesach poprzez przeglądanie projektów budynków, GIS lub produktów. Archiwum plików DWF składa się z kilku plików XML i plików binarnych spakowanych razem w skompresowanym archiwum utworzonym przy użyciu kompresji [ZIP](/pl/compression/zip/). Możesz zmienić nazwę rozszerzenia pliku DWF na ZIP i wyświetlić zawartość pliku. Pakiet DWF może zawierać wiele rodzajów danych projektowych, takich jak grafika 2D, grafika 3D, metadane pakietu i sekcji oraz inne pliki zasobów.

**Pliki metadanych DWF** – pliki XML, które zawierają informacje dotyczące metadanych i struktury (autor, tytuł, czas utworzenia, zależności sekcji, kolejność sekcji, opisy plików zasobów, role, typy MIME itp.) oraz dotyczące sekcji (strona informacje, metadane projektowe itp.). Metadane strukturalne służą do tworzenia obiektów logicznych (kolekcji plików reprezentujących część lub stronę itp.).

**Pliki zasobów** – pliki multimedialne lub inne pliki treści, do których odniesienia znajdują się w metadanych pakietu/sekcji i zazwyczaj są prezentacjami danych projektowych w różnych formatach (ZGL, W2D, [JPG](/pl/image/jpeg/), [PNG] (/pl/image/png/), AVI, XML, [TXT](/pl/przetwarzanie tekstu/txt/), [DOC](/pl/przetwarzanie tekstu/doc/) itp.)

### Szczegóły formatu pliku ###

Pliki DWF są podzielone na trzy główne sekcje, jak pokazano poniżej.

* Nagłówek identyfikacji pliku
* Blok danych pliku
* Zwiastun zakończenia pliku

#### Nagłówek identyfikatora pliku ####

Nagłówek identyfikatora pliku umożliwia identyfikację plików DWF przez aplikacje. Określa również, która wersja specyfikacji DWF została użyta do zakodowania pliku. Jest to 12-bajtowy nagłówek, który jest ułożony w następujący sposób:


|Bajt|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Znak|(|D|W|F|(spacja)|V|0|0|.|3|0|)

Oto podsumowanie tej tabeli:

* Pierwsze sześć bajtów nagłówka zawsze reprezentuje znaki ASCII "(DWF V"
* Kolejne 5 bajtów zawiera informacje o numerze wersji np. "00.30" wraz z wartością wersji głównej i pomocniczej formatu

Aplikacje tworzące plik DWF powinny określać najniższy możliwy numer wersji, jaki musi obsługiwać aplikacja czytająca, aby poprawnie korzystać z danych.

#### Blok danych pliku ####

Blok danych pliku rozpoczyna się od 13. bajtu pliku DWF i jest serią par kodu operacji i operandu, jak w poniższej tabeli.

|Pole 1|Pole 2|Pole 3|Pole 4|Pole 5|Pole 5
--- | --- |--- | --- |--- | --- |
|kod operacji|operand|kod operacji|operand|kod operacji|operand

Plik DWF może zawierać pary opcode-operand w postaci czytelnego kodu ASCII, jak również kodu binarnego lub kombinacji obu tych elementów. Wszystkie operacje DWF mają czytelną postać kodu operacji/argumentu operacji ASCII, a większość operacji ma również zakodowaną binarną postać kodu operacji/argumentu operacji. Kody operacji są jednobajtowe, co pozwala na ponad 200 operacji. Rozszerzony ASCII i rozszerzony plik binarny to przypadki wyjątkowe. Wartości Opcodes mogą mieścić się w zakresie od 0-255 z pewnymi wyjątkami. Z wyjątkiem dwóch specjalnych typów kodów operacyjnych rozszerzonego ASCII i rozszerzonego binarnego, czytnik plików musi wiedzieć, jak obliczyć długość operandu.

##### Zakazane Opcodes #####

Reprezentacje ASCII dla następujących elementów nie mogą być używane jako kody operacji:

Następujące reprezentacje ASCII nie mogą być używane jako kody operacyjne:

* Spacja (0x20)
* Zakładka (0x09)
* Łącznik (0x2D)
* Cyfry ASCII 0-9 (0x30 - 0x39)
* Powrót karetki (0x0D)
* Przesunięcie wiersza (0x0A)
* Pojedynczy cudzysłów (0x27)
* Podwójny cudzysłów (0x22)
* Okres (0x2E)
* Nawiasy (0x28 i 0x29)
* Nawiasy klamrowe (0x7B i 0x7D)
* Nawiasy kwadratowe (0x5B i 0x5D)
* Ukośnik wsteczny (0x5C)

#### Zwiastun zakończenia pliku ####

Zwiastun zakończenia pliku dla DWF jest po prostu specjalnym kodem operacji wskazującym koniec pliku. Niektóre aplikacje mogą przechowywać dane inne niż DWF po opkodzie zakończenia. Zwiastun jest pokazany poniżej:


|Bajt|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Znak|(|E|n|d|0|f|D|W|F|)

## Bibliografia ##

* [DWF – z Wikipedii](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Format danych WHIP](http://paulbourke.net/dataformats/whip/)
* [http://blogs.msdn.com/opc/archive/2009/05/18/adventures-in-packaging-episode-1.aspx](http://blogs.msdn.com/opc/archive/2009 /05/18/adventures-in-packaging-episode-1.aspx)

