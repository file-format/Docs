{
  "date" : "2019-10-11",
  "keywords" :[ "3DS", "plik", "format", "typ pliku", "rozszerzenie", "co to jest plik 3DS?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie plików 3DS i interfejsach API, które mogą otwierać i tworzyć pliki 3DS.",
  "title" :"Format Pliku 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik 3DS?

Plik z rozszerzeniem .3ds reprezentuje format pliku siatki 3D Sudio (DOS) używany przez Autodesk 3D Studio. Autodesk 3D Studio działa na rynku formatów plików 3D od lat 90. XX wieku, a teraz ewoluowało w 3D Studio MAX do pracy z modelowaniem, animacją i renderowaniem 3D. Plik 3DS zawiera dane do reprezentacji 3D scen i obrazów i jest jednym z popularnych formatów plików do importu i eksportu danych 3D. Uwzględnia informacje, takie jak lokalizacje kamer, dane siatki, informacje o oświetleniu, konfiguracje rzutni, dane grupy wygładzania, odniesienia do map bitowych i atrybuty, aby utworzyć wierzchołki i wielokąty do renderowania sceny.

## Format pliku 3DS — więcej informacji
U podstaw 3DS jest binarnym formatem pliku, który ma predefiniowaną strukturę przechowywania i wyszukiwania danych. Format pliku binarnego umożliwia szybsze formatowanie plików 3DS w porównaniu z formatami plików tekstowych. Dane w pliku 3DS są przechowywane w postaci porcji.

### Fragment 3DS

Każdy fragment w pliku 3DS to blok danych, który zawiera identyfikator, długość bloku dla lokalizacji następnego bloku i same dane. Identyfikator fragmentu pozwala czytnikom formatów plików 3DS pomijać bloki, których nie rozpoznają. Pomaga również w rozszerzaniu formatu. Każdy fragment przechowuje informacje związane z kształtami, oświetleniem i przeglądaniem informacji, które razem renderują scenę. Kawałki są ułożone w hierarchiczną strukturę w pliku 3DS i przypominają drzewo XML Document Object w reprezentacji.

**Identyfikator fragmentu:** pierwsze dwa bajty fragmentu reprezentują identyfikator fragmentu, który pozwala czytnikowi plików zdecydować, czy wziąć go pod uwagę podczas odczytu, czy pominąć.

**Długość fragmentu:** Po identyfikatorze fragmentu następuje 4-bajtowa liczba całkowita (w little-endian), która oznacza długość fragmentu. Długość ta obejmuje również długość danych, długość ich podbloków i 6-bajtowy nagłówek.

**Ładunek:** Po długości porcji następują rzeczywiste bajty danych dla porcji, po których następują jej podkawałki w tej samej hierarchicznej strukturze, którą można rozszerzyć do kilku poziomów.

### Struktura kawałka

Hierarchiczna struktura prostej porcji jest przedstawiona poniżej:

**Kawałek**

|początek|koniec|rozmiar|nazwa
--- | --- | --- | ---
|0|1|2|Identyfikator fragmentu
|2|5|4|Następny fragment

Kawałki mają narzuconą hierarchię, która jest identyfikowana przez ich identyfikator. Plik 3ds ma identyfikator podstawowej porcji 4D4Dh. Jest to zawsze pierwsza część pliku. W podstawowej części znajdują się główne części.

**Główne kawałki**

|identyfikator|opis
--- | ---
|3D3D|Początek danych siatki obiektu.
|B000|Początek danych klatki kluczowej.

Wskaźnik Next Chunk po bloku ID wskazuje następny fragment główny.
Bezpośrednio po porcji głównej znajduje się kolejna porcja. Może to być dowolny inny typ fragmentu dozwolony w jego głównym zakresie fragmentów.
Dla opisu siatki (3D3D) mogą to być dowolne wielokrotności.

**Podkawałki 3D3D — blok siatki**


|identyfikator|opis
--- | ---
|1100|nieznane
|1200|Kolor tła.
|1201|nieznane
|1300|nieznane
|1400|nieznane
|1420|nieznane
|1450|nieznane
|1500|nieznane
|2100|Blok kolorów otoczenia
|2200|mgła?
|2201|mgła?
|2210|mgła?
|2300|nieznane
|3000|nieznane
|4000|Blok obiektu
|7001|nieznane
|AFFF|nieznane

**Podfragmenty 4000 - blok opisu obiektu**
Pierwszym elementem Subchunk 4000 jest ciąg ASCIIZ nazwy obiektu.
Pamiętaj, że obiektem może być siatka, światło lub kamera.

|identyfikator|opis
--- | ---
|4010|nieznane
|4012|cień?
|4100|Trójkątny obiekt wielokątny
|4600|Światło
|4700|Aparat

## Bibliografia

* [Formaty plików geometrii — Autodesk](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)
* [3DS – z Wikipedii](https://en.wikipedia.org/wiki/.3ds)
