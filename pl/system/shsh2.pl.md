{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik SHSH2 - Format pliku obiektu BLOB SHSH iOS",
  "description":"Dowiedz się, co to jest plik SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Co to jest plik SHSH2?

Plik SHSH2, znany również jako obiekt blob SHSH lub ECID SHSH, to podpis cyfrowy używany przez firmę Apple do uwierzytelniania i weryfikowania aktualizacji oprogramowania sprzętowego dla urządzeń z systemem iOS, takich jak iPhone'y, iPady i iPody. Zawiera unikalny identyfikator urządzenia znany jako ECID (Exclusive Chip ID). Zawiera także informację o wersji oprogramowania zainstalowanego na urządzeniu.

## Format pliku SHSH2 — więcej informacji

Pliki SHSH2 są zapisywane na dysku w formacie binarnym, a szczegóły wewnętrznej struktury plików w tym formacie pliku nie są dostępne publicznie.

Po zainstalowaniu nowej wersji systemu iOS na urządzeniu Apple, takim jak iPhone, iPad lub Mac, generowany jest plik SHSH2. Ten plik SHSH2 jest wysyłany do serwerów Apple, które odczytują i weryfikują ten plik podpisu cyfrowego. Na podstawie tych informacji serwer zezwala lub uniemożliwia instalację.

To samo dzieje się, gdy żądana jest aktualizacja. Gdy użytkownik zażąda aktualizacji lub przywrócenia swojego urządzenia za pośrednictwem iTunes lub innego oprogramowania, serwery Apple sprawdzą, czy plik SHSH2 odpowiada numerowi ECID urządzenia i wersji oprogramowania sprzętowego, zanim umożliwią kontynuację aktualizacji.

## Bibliografia

* [SHSH Blob – według Wikipedii](https://en.wikipedia.org/wiki/SHSH_blob)
* [Oszczędzanie TSS](https://tsssaver.1conan.com/v2/)

