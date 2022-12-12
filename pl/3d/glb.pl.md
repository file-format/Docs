{
  "date" : "2019-12-03",
  "keywords" :[ "GLB", "plik", "format", "typ pliku", "rozszerzenie", "co to jest plik GLB?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Dowiedz się o formacie pliku GLB i interfejsach API, które mogą otwierać i tworzyć pliki GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Czym jest plik GLB?

GLB to binarna reprezentacja formatu plików modeli 3D zapisanych w formacie transmisji GL ([glTF](/pl/3d/gltf/)). Informacje o modelach 3D, takie jak hierarchia węzłów, kamery, materiały, animacje i siatki w formacie binarnym. Ten format binarny przechowuje zasób glTF (JSON, .bin i obrazy) w binarnym obiekcie blob. Pozwala to również uniknąć problemu zwiększania rozmiaru pliku, który ma miejsce w przypadku glTF. Format plików GLB zapewnia niewielkie rozmiary plików, szybkie ładowanie, pełną reprezentację sceny 3D i rozszerzalność w celu dalszego rozwoju. Format wykorzystuje model/gltf-binary jako typ MIME.

## Format pliku GLB — więcej informacji

Metody dostarczania treści używane przez glTF skutkują dodatkowym przetwarzaniem w celu dekodowania danych binarnych zakodowanych w standardzie base-64, a także zwiększają rozmiar pliku o 33%. Te metody dostarczania, które przyczyniły się do powstania formatu pliku GLB, obejmują:

* glTF JSON wskazuje na zewnętrzne dane binarne (geometria, klatki kluczowe, skórki) i obrazy.
* glTF JSON osadza dane binarne zakodowane w base64 i obrazy wbudowane przy użyciu identyfikatorów URI danych.

GLB jako format kontenera został wprowadzony jako format pliku binarnego do reprezentacji zasobu glTF w binarnym obiekcie blob, aby uniknąć problemów powodowanych przez glTF. Format pliku GLB [specyfikacje] (https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification) powinien być skierowany do każdej implementacji czytnika/zapisu tego samego do tworzenia aplikacji .

## Struktura plików GLB

Format pliku GLB jest oparty na little endian, a jego struktura pokazuje, że zawiera:

* 12-bajtowa preambuła, zatytułowana nagłówek.
* Jeden lub więcej fragmentów zawierających zawartość JSON i dane binarne.

#### Nagłówek GLB

Nagłówek formatu pliku GLB składa się z trzech 4-bajtowych wpisów:

* uint32 magic - magic równa się 0x46546C67. Jest to ciąg ASCII glTF i może być używany do identyfikacji danych jako binarny glTF
* wersja uint32 — wskazuje wersję formatu kontenera Binary glTF
* długość uin32 - całkowita długość binarnego glTF, w tym nagłówka i wszystkich fragmentów w bajtach

#### Kawałki

Każda porcja w pliku GLB ma następującą strukturę:

|uint32|uint32|ubyte[]
---|---|---|
|Długość kawałka|Typ kawałka|Dane kawałka

* `chunkLength` - długość chunkData w bajtach
* `chunkType` - wskazuje wskazuje typ porcji
* `chunkData` - binarny ładunek porcji

gdzie typy porcji to:

|# |Typ fragmentu|ASCII|Opis|Wystąpienia
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Ustrukturyzowana zawartość JSON|1
|2.|0x004E4942|BIN|Bufor binarny|0 lub 1

Początek i koniec każdego fragmentu muszą być wyrównane do 4-bajtowej granicy i w tym celu należy zastosować dopełnienie.

##### Strukturalna zawartość JSON

Powinien to być pierwszy fragment zasobu Binary glTF i umożliwia implementacji stopniowe pobieranie zasobów z kolejnych fragmentów. Zapewnia to również możliwość odczytu tylko wybranego podzbioru zasobów z binarnego zasobu glTF, takiego jak najgrubszy poziom szczegółowości siatki. Aby spełnić wymagania dotyczące wyrównania, ta porcja musi być uzupełniona końcowymi znakami spacji (0x20).

##### Bufor binarny #####

Ten fragment zawiera binarny ładunek dla geometrii, klatek kluczowych animacji, skórek i obrazów. Powinien to być drugi fragment zasobu Binary glTF i musi być uzupełniony końcowymi zerami (0x00), aby spełnić wymagania wyrównania.

## Bibliografia ##

* [Specyfikacje formatu plików GLB — Khronos](/pl/3D/GLTF/)

