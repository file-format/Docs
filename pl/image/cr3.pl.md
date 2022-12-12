{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku CR3 — plik obrazu Canon Raw 3",
  "description":"Poznaj format pliku CR3 i interfejsy API, które mogą tworzyć i otwierać pliki CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Czym jest plik CR3?

Plik CR3 to format pliku obrazu Canon RAW tworzony przez wybrane aparaty cyfrowe firmy Canon. Został wprowadzony przez firmę Canon w celu zastąpienia formatu pliku CR2 i jest używany przez niektóre urządzenia cyfrowe firmy Canon. Pliki CR3 przechowują oryginalne nieprzetworzone bezstratne dane obrazu przechwycone przez aparat. Wykorzystanie tych surowych obrazów zapewnia wysoką jakość obrazów i daje fotografom dużo miejsca na edycję. Oprócz głównych danych obrazu pliki CR3 przechowują również informacje o metadanych obrazu.

## Format pliku CR3

Pliki CR3 są zapisywane na dysku jako pliki binarne w formacie ISO Base Media File Format (ISO/IEC 14496-12) i zawierają również niestandardowe [znaczniki firmy Canon] (https://exiftool.org/TagNames/Canon.html#uuid). Zawiera również [kodek Canon „crx”](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), który jest mieszanką JPEG-LS (Rice-Golomb + RLE kodowanie) i JPEG-2000 (LeGall 5/3 DWT + kwantyfikacja).

## Niestandardowe znaczniki CR3

Pliki CR3 zawierają niestandardowe tagi do różnych celów. Niektóre z tych tagów są następujące.

|Identyfikator znacznika| Nazwa znacznika| Zapisywalne |Wartości / Notatki|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Tagi Canon CCTP|
|'CMT1' |IFD0| - |--> Etykiety EXIF|
|'CMT2' |ExifIFD| - |--> Etykiety EXIF|
|'CMT3' |MakerNoteCanon| - |--> Znaczniki Canon|
|'CMT4' |Informacje GPS| - |--> Znaczniki GPS|
|'CNCV' |Wersja kompresora| nie| |
|'CNOP' |CanonCNOP| - |--> Tagi Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Znaczniki Canon CNTH|
|'THMB' |Obraz miniatury| nie| |

## Bibliografia

* [Format pliku CR2] (http://lclevy.free.fr/cr2/)
* [Tagi Canon](https://exiftool.org/TagNames/Canon.html#uuid)

