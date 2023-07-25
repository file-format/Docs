{
  "date" : "2019-12-12",
  "keywords" :["FBX", "plik", "rozszerzenie", "format", "Format pliku 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby wiedzieć, co to jest plik FBX i interfejsy API, które mogą je tworzyć i otwierać.",
  "title" :"FBX - format pliku FilmBox 3D",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik FBX?

FBX, FilmBox, to popularny format plików 3D, który został pierwotnie opracowany przez Kaydara dla MotionBuilder. Został przejęty przez Autodesk Inc w 2006 roku i jest obecnie jednym z głównych formatów wymiany 3D, używanym przez wiele narzędzi 3D. FBX jest dostępny zarówno w formacie binarnym, jak i ASCII. Format został ustanowiony w celu zapewnienia interoperacyjności między aplikacjami do tworzenia treści cyfrowych. Dostępnych jest wiele narzędzi do konwersji z/do formatu pliku FBX.

## Format pliku FBX — więcej informacji

FBX jest zastrzeżonym formatem, a specyfikacje dotyczące jego formatu plików binarnych nie są oficjalnie dostępne. Autodesk dostarcza C++ FBX SDK do odczytu, zapisu i konwersji do/z pliku FBX. Skrypt importu i eksportu Pythona dla FBX jest również dostępny w oprogramowaniu Blender, które nie korzysta z pakietu FBX SDK.

### Tekstowa struktura plików

Tekstowa struktura plików ma strukturę drzewa udokumentowaną z wyraźnie nazwanymi identyfikatorami. Składa się z zagnieżdżonej listy węzłów ułożonych w hierarchii, gdzie każdy węzeł ma:

* Identyfikator NodeType (nazwa klasy)
* Krotka powiązanych z nią właściwości, elementy krotki to zwykłe prymitywne typy danych: ##float, integer, string## itd.
* Lista zawierająca węzły w tym samym formacie (rekurencyjnie).

Można je przedstawić logicznie w następujący sposób:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Niektóre standardowe węzły są zdefiniowane jako niejawna lista, w której każdy element składa się z zagnieżdżonej listy. Każda aplikacja, która zamierza uzyskać dostęp do geometrii FBX, musi przeanalizować tę zawartość i nadać jej użyteczne znaczenie. Przykład tekstowego pliku FBX podano poniżej:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Struktura plików binarnych plików FBX

Jak wspomniano wcześniej, specyfikacje formatu plików FBX nie są publicznie dostępne dla FBX. Ponieważ Blender Foundation implementuje format pliku FBX bez korzystania z dostarczonego przez firmę pakietu SDK, niektóre szczegóły dotyczące formatu pliku binarnego są [dostępne](https://code.blender.org/2013/08/fbx-binary-file-format -specyfikacja/) w ramach jej realizacji.

Struktura plików binarnych jest zgodna z następującą kolejnością:

* Nagłówek
* Rekord obiektu
* Stopka

### Nagłówek FBX

Informacje nagłówka pliku składają się z 27 bajtów.

* Bajty 0 - 20: Kaydara FBX Binary \x00 (file-magic, z 2 spacjami na końcu, potem terminator NULL).
* Bajty 21 - 22: [0x1A, 0x00]## (nieznane, ale wszystkie obserwowane pliki pokazują te bajty).
* Bajty 23 - 26: unsigned int, numer wersji. 7300 dla wersji 7.3 na przykład.

### Rekord obiektu ###

Po nagłówku następuje rekord obiektu, który jest pełnym rekordem węzła z pustą nazwą i pustą listą właściwości. Rekurencyjnie zawiera całą formację pliku.

### Stopka ###

Sekcja stopki FBX znajduje się na końcu pliku, którego zawartość jest nieznana.

## Formaty nagrań ##

Rekordy w pliku FBX są podzielone na kategorie:

* Rekordy węzłów
* Rejestry nieruchomości

### Format rekordu węzła ###

Każdy format rekordu węzła ma nazwę i ma następujący układ pamięci.


|Rozmiar (bajty)|Typ daty|Nazwa
--- | ---|---|
|4|UInt32|Przesunięcie końca
|4|UInt32|LiczbaWłaściwości
|4|UInt32|ListaWłaściwościDł
|1|UInt8|NazwaDł
|NazwaDługość|znak|Nazwa
|?|?|Właściwość[n], gdzie n = 0:PropertyListLen
|Opcjonalne| |
|?|?|Lista zagnieżdżona
|13|uint8[]|Null-Record

gdzie:

* `EndOffset` to odległość od początku pliku do końca rekordu węzła (tj. pierwszego bajtu tego, co będzie następne). Można to wykorzystać do łatwego pomijania nieznanych lub niepotrzebnych rekordów.
* `NumProperties` to liczba właściwości w krotce wartości powiązanej z węzłem. Zagnieżdżona lista jako ostatni element nie jest liczona jako właściwość.
* `PropertyListLen` to długość listy właściwości. Jest to rozmiar wymagany do przechowywania właściwości ##NumProperties##, który zależy od typu danych właściwości.
* `NameLen` to długość nazwy obiektu w znakach. Jedynym przypadkiem, w którym jest to 0, wydaje się być lista najwyższego poziomu.
* `Nazwa` to nazwa obiektu. Nie ma zakończenia zerowego.
* `Właściwość[n]` jest n-tą właściwością. Aby uzyskać informacje na temat formatu, zobacz sekcję właściwość Format rekordu. Właściwości są zapisywane sekwencyjnie i bez dopełnienia.
* `NestedList` to zagnieżdżona lista, której obecność jest wskazywana przez NULL-rekord na samym końcu.

Istnienie wpisu na liście zagnieżdżonej można ustalić, sprawdzając, czy pozostały bajty do osiągnięcia wartości EndOffset. Jeśli tak, następny rekord obiektu powinien zostać odczytany bezpośrednio po ostatniej właściwości. Rekord obiektu następuje następnie po 13 bajtach zerowych, które następnie łączą się z EndOffset. Cel lub wymóg wpisu NULL nie jest znany i może wskazywać na jakąś funkcję formatu.

### Format rekordu właściwości ###

Rekord właściwości zawiera szczegółowe informacje o właściwościach, które są częścią Node. Rekord właściwości ma następujący układ pamięci:


|Rozmiar (bajty)|Typ danych|Nazwa
--- | --- | ---
|1|znak|Kod typu
|?|?|Dane

TypeCode reprezentują kody znaków, które są uporządkowane w grupach wymagających podobnej obsługi. TypeCodes można podzielić na następujące typy, a TypeCode może być jednym z kodów znaków wśród tych typów.

#### Typy pierwotne ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Dane w prymitywnym rekordzie typu skalarnego są dokładnie binarną reprezentacją wartości w kolejności bajtów little-endian.

#### Typy tablic ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Dane dla typu tablicy są bardziej złożone i mają następującą strukturę.


|Rozmiar (bajty)|Typ danych|Nazwa
--- | --- | ---
|4|Uint32|Długość tablicy
|4|Uint32|Kodowanie
|4|Uint32|Długość po skompresowaniu
|?|?|Spis treści

### Specjalne typy ###

Poniżej znajdują się kody typów specjalnych typów.

```
S: String
R: raw binary data
```

Oba te kody typów są reprezentowane w następujący sposób:


|Rozmiar (bajty)|Typ danych|Nazwa
--- | --- | ---
|4|Uw32|Długość
|Długość| |

Łańcuch nie jest zakończony zerem i może zawierać znaki \0 (jest to faktycznie używane w niektórych właściwościach FBX).

## Bibliografia ##

* [FBX — pakiet Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)
* [Specyfikacje formatu plików binarnych FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

