{
  "date" : "2020-08-20",
  "keywords" :[ "plik eot", "format pliku eot", "co to jest plik eot", "plik", "przykład eot", "rozszerzenie pliku eot", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT — format pliku czcionek TrueType",
  "description":"Dowiedz się o formacie plików EOT i interfejsach API do tworzenia i otwierania plików EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Czym jest plik EOT?

Plik z rozszerzeniem .eot to czcionka OpenType osadzona w dokumencie. Są one najczęściej używane w plikach internetowych, takich jak strony internetowe. Został stworzony przez firmę Microsoft i jest obsługiwany przez produkty firmy Microsoft, w tym plik prezentacji programu PowerPoint [.pps](/pl/presentation/pps). Plik nie ma podstawowego zastosowania i jest rodzajem dokumentu towarzyszącego głównemu dokumentowi lub stronie internetowej. Podobnie jak czcionki OTF, EOT obsługuje zarówno kontury Postscript, jak i TrueType dla glifów. Pliki EOT mają mniejszy rozmiar z tego powodu, że są kompresowane przy użyciu kompresji LZ. EOT używa narzędzia firmy Microsoft do tworzenia czcionki z istniejących czcionek TTF/OTF.

## Krótka historia

Czcionka EOT została zgłoszona do W3C w 2007 roku jako część CSS3, ale ze względu na wymagania dotyczące trwałej instalacji w systemie zdalnym stała się powodem jej odrzucenia. Został ponownie przesłany w marcu 2008 roku, ale ostatecznie W3C wybrało [Web Font Format](/pl/font/woff/) (WOFF), który został wówczas ustandaryzowany.

## Format pliku EOT

Szczegóły formatu pliku EOT można znaleźć na [stronie przesyłania W3](https://www.w3.org/Submission/EOT/#FileFormat) i omówiono strukturę używaną przez ten format czcionki. EOT składa się z pojedynczej struktury EMBEDDEDFONT, która zapewnia wystarczającą ilość podstawowych informacji o nazwie czcionki i obsługiwanych znakach. Pakowanie tych informacji pozwala agentom użytkownika uniknąć rozpakowywania, dekompresji lub instalowania czcionki, jeśli jest ona już obecna na komputerze.

### Struktura EMBEDDEDFONT
Struktura EMBEDDEDFONT została poddana trzem rewizjom, z dodaniem dodatkowych danych na końcu struktury przy każdej rewizji. Ostatnia wersja struktury EMBEDDEDFONT jest przedstawiona poniżej.

|Typ danych|Nazwa wpisu|Opis|
---|---|---|
|unsigned long|EOTSize|Całkowita długość struktury w bajtach (łącznie z łańcuchem i danymi czcionki)|
|unsigned long|FontDataSize|Długość czcionki OpenType (FontData) w bajtach|
|unsigned long|Wersja|Numer wersji tego formatu - 0x00020002|
|unsigned long|Flagi|Przetwarzanie flag|
|byte[10]|FontPANOSE|Wartość PANOSE dla tej czcionki — zobacz http://www.microsoft.com/typography/otspec/os2.htm#pan|
|bajt|Zestaw znaków|W systemie Windows pochodzi z TEXTMETRIC.tmCharSet. Ta wartość określa zestaw znaków czcionki. DEFAULT_CHARSET (0x01) oznacza brak preferencji. — Zobacz https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|bajt|Kursywa|Jeśli bit kursywy jest ustawiony w OS/2.fsSelection, wartość będzie równa 0x01 — patrz http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Waga|Wartość wagi tej czcionki — zobacz http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Flagi typu, które dostarczają informacji o uprawnieniach osadzania — zobacz http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Magiczny numer dla pliku EOT - 0x504C. Służy do sprawdzania uszkodzeń danych.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bity 0-31) — patrz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bity 32-63) — patrz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bity 64-95) — patrz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bity 96-127) — patrz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bity 0-31) — patrz http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bity 32-63) — patrz http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment — zobacz https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Zarezerwowany1|Zarezerwowany - musi wynosić 0|
|unsigned long|Zarezerwowany2|Zarezerwowany - musi wynosić 0|
|unsigned long|Zarezerwowany3|Zarezerwowany - musi wynosić 0|
|unsigned long|Zarezerwowany4|Zarezerwowany - musi wynosić 0|
|unsigned short|Wypełnienie1|Wypełnienie, aby zachować długie wyrównanie. Wartość wypełnienia musi być zawsze ustawiona na 0x0000.|
|unsigned short|FamilyNameSize|Liczba bajtów używanych przez tablicę FamilyName|
|bajt|NazwaRodziny[RozmiarNazwyRodziny]|Tablica znaków UTF-16 o długości bajtów RozmiarNazwyRodziny. To jest ciąg rodziny czcionek w języku angielskim znaleziony w tabeli nazw czcionki (identyfikator nazwy = 1) — patrz https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Dopełnienie2|Wartość dopełnienia musi być zawsze ustawiona na 0x0000.|
|unsigned short|StyleNameSize|Liczba bajtów używanych przez StyleName|
|byte|StyleName[StyleNameSize]|Tablica znaków UTF-16 o długości StyleNameSize bajtów. To jest łańcuch podrodziny czcionek w języku angielskim znaleziony w tabeli nazw czcionki (identyfikator nazwy = 2) — patrz https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Dopełnienie3|Wartość dopełnienia musi być zawsze ustawiona na 0x0000.|
|unsigned short|VersionNameSize|Liczba bajtów używanych przez VersionName|
|bajty|NazwaWersji[RozmiarNazwyWersji]|Tablica znaków UTF-16 o długości bajtówRozmiarNazwyWersji. To jest ciąg wersji języka angielskiego znaleziony w tabeli nazw czcionki (identyfikator nazwy = 5) — patrz https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Dopełnienie4|Wartość dopełnienia musi być zawsze ustawiona na 0x0000.|
|unsigned short|FullNameSize|Liczba bajtów używanych przez FullName|
|byte|FullName[FullNameSize]|Tablica znaków UTF-16 o długości FullNameSize bajtów. To jest ciąg pełnej nazwy w języku angielskim znaleziony w tabeli nazw czcionki (identyfikator nazwy = 4) — patrz https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Dopełnienie5|Wartość dopełnienia musi być zawsze ustawiona na 0x0000.|
|unsigned short|RootStringSize|Liczba bajtów używanych przez tablicę RootString|
|byte|RootString[RootStringSize]|Tablica znaków UTF-16 o długości bajtów RootStringSize.|
|unsigned long|RootStringCheckSum|RootString wartość sumy kontrolnej. Zobacz algorytm przetwarzania RootStringChecksum poniżej.|
|unsigned long|EUDCCodePage|Wartość strony kodowej potrzebna do obsługi czcionek EUDC.|
|unsigned short|Dopełnienie6|Wartość dopełnienia musi być zawsze ustawiona na 0x0000.|
|unsigned short|SignatureSize|Liczba bajtów używanych przez tablicę Signature. Obecnie zarezerwowane i powinno być ustawione na 0x0000.|
|bajt|Podpis[SignatureSize]|Obecnie zarezerwowane. Jeśli SignatureSize wynosi 0x0000, ta tablica nie ma długości.|
|unsigned long|EUDCFlags|Flagi przetwarzania dla czcionki EUDC. Typowe wartości to TTEMBED_XORENCRYPTDATA i TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Liczba bajtów używanych przez tablicę Signature.|
|bajt|EUDCFontData[EUDCFontSize]|Liczba bajtów użytych dla danych czcionki EUDC. Jeśli EUDCFontSize to 0x00000000, ta tablica nie ma długości.|
|byte|FontData[FontDataSize]|Dane czcionki dla tego pliku EOT. Dane mogą być skompresowane lub zaszyfrowane XOR, jak wskazują flagi przetwarzania.|

## Bibliografia

* [Format pliku EOT](https://www.w3.org/Submission/EOT/)
* [Osadzone OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Osadzanie czcionek](https://en.wikipedia.org/wiki/Font_embedding)

