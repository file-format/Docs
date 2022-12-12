{
  "date" : "2019-10-11",
  "keywords" :[ "plik rar", "format pliku rar", "co to jest plik rar", "plik", "przykład rar", "rozszerzenie pliku rar", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Co to jest rozszerzenie pliku RAR i interfejsy API, które mogą tworzyć i otwierać pliki RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik RAR?

Pliki z rozszerzeniem .rar to pliki archiwalne, które są tworzone w celu przechowywania informacji w postaci skompresowanej lub normalnej. RAR, co oznacza format pliku Roshal ARchive, to zastrzeżony format pliku stworzony przez Eugene'a Roshala w 1995 roku, który był rosyjskim inżynierem oprogramowania. Format służy do archiwizowania plików różnymi metodami, w tym różnymi technikami kompresji. Dostępnych jest kilka aplikacji dla systemów Windows, Linux i MacOS do wyodrębniania plików RAR. Oprogramowanie WinRAR firmy RARLab to narzędzie do archiwizacji plików typu shareware (bezpłatne przez 40 dni) dla platformy Microsoft Windows; oprogramowanie zostało przeportowane na Linuksa (tylko jako ekstraktor) przez tego samego autora, Eugene'a Roshala.

## Historia wersji formatu pliku RAR

* v1.3 (oryginalna, bez podpisu „Rar!”)
* v1.5
* v2.0 - wydana z WinRAR 2.0 i Rar dla MS-DOS 2.0
* v2.9 - wydany w WinRAR w wersji 3.00
* v5.0 — obsługiwane przez WinRAR 5.0 i nowsze

## Kluczowe cechy formatu RAR

RAR działa w terenie od dłuższego czasu i jest jednym z ulubionych formatów plików do archiwizacji. Kluczowe cechy formatu RAR to:

**`Wysoki współczynnik kompresji:`** Lepszy w porównaniu z [ZIP](/pl/compression/zip/), porównywalny z formatem 7z i zipx.

**`Silne szyfrowanie plików z założenia:`** Zaszyfrowane archiwa RAR4 opierają się na szyfrowaniu AES-128, podczas gdy zaszyfrowane archiwa RAR5 opierają się na szyfrowaniu AES-256 z ulepszonym planowaniem kluczy

**`Zaawansowana korekcja błędów i możliwości odzyskiwania danych:`** opcjonalne zapisy odzyskiwania podczas tworzenia archiwum

**`Rozmiar pliku:`** Minimalnie 20 bajtów i maksymalnie 2^63 bajty (8 eksabajtów całkowitego rozmiaru archiwum)

**`Wielotomowe archiwa RAR:`** Możliwość podzielenia dużych archiwów na kilka mniejszych plików w celu ułatwienia przesyłania przez sieć. W takim przypadku rozszerzenia plików są zwiększane o 1, aby reprezentować podzielone woluminy

## Format pliku RAR

Pełne specyfikacje formatu RAR nie są publicznie dostępne i dlatego nie można sformułować szczegółowych informacji na temat formatu w zwięzły sposób.

### Ogólny układ archiwum

Ogólny układ formatu pliku RAR wprowadzonego w wersji 5.0 jest następujący:

|Format pliku
---|
|Moduł samorozpakowujący (opcjonalnie)
|Podpis RAR 5.0
|Nagłówek szyfrowania archiwum (opcjonalnie)
|Główny nagłówek archiwum
|Nagłówek usługi komentarzy archiwum (opcjonalnie)
Nagłówek pliku 1
|Nagłówki usług (NTFS ACL, strumienie itp.) dla poprzedniego pliku (opcjonalnie)
|...
|N nagłówka pliku
|Nagłówki usług (NTFS ACL, strumienie itp.) dla poprzedniego pliku (opcjonalnie)
|Rekord odzyskiwania (opcjonalnie)
|Koniec nagłówka archiwum

Informacje o każdej sekcji pliku RAR wymienionej powyżej można znaleźć w dokumencie [Specyfikacja formatu plików RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### Samorozpakowujące się archiwa RAR

Jeśli sam plik RAR jest samorozpakowujący się, informacja o samorozpakowaniu znajduje się na początku pliku przed sygnaturą archiwum. Jego rozmiar i zawartość nie są określone.

#### Podpis RAR 5.0

Sygnatura RAR to 8-bajtowy nagłówek, który składa się z następującej magicznej liczby:

0x 52 61 72 21 1A 07 00

gdzie

0x6152 — HEAD_CRC

0x72 — TYP_GŁOWY

0x1A21 - HEAD_FLAGS

0x0007 — ROZMIAR_GŁÓWKI

## Bibliografia

* [Format archiwum RAR 5.0] (https://www.rarlab.com/technote.htm)
* [RAR – z Wikipedii](https://en.wikipedia.org/wiki/RAR_(file_format))

