{
  "date" : "2020-03-16",
  "keywords" :[ "Plik DXF", "Format pliku", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików DXF i interfejsy API, które mogą tworzyć i otwierać pliki DXF.",
  "title" :"Format Pliku DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik DXF?

DXF, Drawing Interchange Format lub Drawing Exchange Format, jest oznakowaną reprezentacją danych pliku rysunku programu AutoCAD. Każdy element w pliku ma przedrostek liczby całkowitej zwany kodem grupy. Ten kod grupy faktycznie reprezentuje element następujący po nim i wskazuje znaczenie elementu danych dla danego typu obiektu. DXF umożliwia reprezentację prawie wszystkich informacji określonych przez użytkownika w pliku rysunku.

Format pliku DXF został opracowany przez firmę Autodesk jako format pliku danych CAD w celu zapewnienia współdziałania danych między programem AutoCAD a innymi aplikacjami. W ten sposób dane mogą być importowane z innych formatów do DXF do AutoCAD zgodnie ze specyfikacjami interoperacyjności formatu DXF.

## Krótka historia ##


Historia formatu plików DXF sięga 1982 roku, kiedy to został wprowadzony jako część programu AutoCAD 1.0. Początkowe wersje programu AutoCAD obsługują tylko format plików ASCII DXF. Wraz z wydaniem 10 programu AutoCAD (i nowszych wersji) w 1988 r. w programie AutoCAD wprowadzono obsługę zarówno formatu ASCII, jak i binarnego formatu plików DXF. Na wcześniejszych etapach Autodesk nie udostępniał żadnych specyfikacji formatu plików, przez co poprawny import plików DXF nie był łatwy. Jednak firma Autodesk publikuje teraz specyfikacje DXF i jest dostępna dla ogółu społeczeństwa.

## Specyfikacje formatu plików ##

Format pliku DXF wykorzystuje kod grupy i pary wartości do uporządkowania zawartości w sekcje. Każda sekcja składa się z rekordów, gdzie każdy rekord składa się z kodu grupy i elementu danych. Każdy kod grupy i wartość znajdują się w osobnej linii w pliku DXF. Każda sekcja zaczyna się od kodu grupy 0, po którym następuje ciąg SECTION. Po nim następuje kod grupy 2 i łańcuch wskazujący nazwę sekcji (na przykład SECTION1). Każda sekcja składa się z kodów grup i wartości, które definiują jej elementy. Sekcja kończy się cyfrą 0, po której następuje ciąg ENDSEC.

Format pliku DXF uwzględnia obiekty różniące się od jednostek. Obiekty nie mają tutaj reprezentacji graficznej, ale jednostki ją mają. W związku z tym wpisy w DXF są określane jako obiekty graficzne, podczas gdy obiekty obiekty są określane jako obiekty niegraficzne. Sekcje BLOCK i ENTITIES pliku DXF zawierają jednostki, a użycie kodów grup w tych dwóch sekcjach jest identyczne. Koniec encji jest wskazywany przez następną grupę 0, która rozpoczyna następną encję lub wskazuje koniec sekcji.

### Struktura plików ###

Sekcje w pliku DXF są ułożone w następującej kolejności:

|Sekcja|Opis podstawowy
---|---|
|Nagłówek|Ta sekcja zawiera ogólne informacje o rysunku. To jest jak funkcja Ustawienia w telefonie, która zawiera różne zmienne powiązane z rysunkiem i skojarzonymi z nim wartościami. Na przykład sekcja Nagłówek określi, z której wersji AutoCAD korzysta plik DXF (zmienna $ACADVER) lub jednostka używana do pomiaru kątów w pliku (zmienna $AUNITS)
|Klasy|Sekcja KLASY zawiera informacje o klasach zdefiniowanych przez aplikację, których instancje pojawiają się w sekcjach BLOCKS, ENTITIES i OBJECTS bazy danych.
|Tabele|Ta sekcja zawiera definicje kilku różnych tabel, z których każda zawiera pewną liczbę różnych wpisów symboli. Na przykład [typ linii](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) (LTYPE) określa wzór kresek, kropek, tekstu i symboli w pliku DXF oraz sposób ich skalowania. Oto pełna lista tabel znalezionych w tej sekcji:<ul><li> Tabela identyfikatorów aplikacji (APPID).</li><li> Tabela rekordów blokowych (BLOCK_RECORD).</li><li> Tabela stylów wymiarowania (WYMSTYP).</li><li> Tabela warstw (WARSTWA).</li><li> Tabela rodzajów linii (LTYPE).</li><li> Tabela stylów tekstu (STYLE).</li><li> Tabela układu współrzędnych użytkownika (LUW).</li><li> Wyświetl (WIDOK) tabelę</li><li> Tabela konfiguracji rzutni (VPORT).</li></ul>
|Bloki|Ta sekcja zawiera obiekty graficzne i elementy rysunku, które składają się na każde odniesienie do bloku na rysunku.
|Elementy|Ta sekcja zawiera rzeczywiste dane obiektów i elementy graficzne rysunku. Może to obejmować surowe dane — na przykład okrąg jest definiowany przez jego grubość, punkt środkowy, promień i kierunek wyciągnięcia.
|Obiekty|Tutaj znajdziesz niegraficzne części rysunku. Na przykład tutaj przechowywane są słowniki programu AutoCAD.

## Bibliografia ##

* [Specyfikacje plików DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF z Wikipedii](https://en.wikipedia.org/wiki/AutoCAD_DXF)

