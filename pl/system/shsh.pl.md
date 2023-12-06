{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik SHSH - Format pliku SHSH Blob dla iPhone'a/iPoda Touch",
  "description":"Dowiedz się, co to jest plik SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Czym jest plik SHSH?

Plik SHSH, znany również jako Signature HaSH, to podpis cyfrowy używany przez firmę Apple do uwierzytelniania i weryfikowania aktualizacji oprogramowania sprzętowego dla urządzeń z systemem iOS, takich jak iPhone'y, iPady i iPody.

## Różnica między formatami plików SHSH i SHSH2

Podobnie jak plik SHSH2, plik SHSH zawiera unikalny identyfikator urządzenia zwany "ECID" (ekskluzywny identyfikator chipa), a także informacje o wersji oprogramowania zainstalowanego na urządzeniu. Jednak pliki SHSH były używane w starszych wersjach systemu iOS (przed iOS 10) i od tego czasu zostały zastąpione plikami SHSH2.

## Format pliku SHSH — więcej informacji

Pliki SHSH są zapisywane na dysku w formacie pliku binarnego. Szczegóły wewnętrznej struktury pliku tego formatu pliku nie są dostępne publicznie.

Pliki SHSH są ważne dla użytkowników, którzy chcą zaktualizować oprogramowanie swojego urządzenia do poprzedniej wersji, która nie jest już podpisana przez Apple. Zapisując pliki SHSH dla określonej wersji oprogramowania sprzętowego, gdy jest ona nadal podpisana przez Apple, użytkownicy mogą później użyć ich do ominięcia weryfikacji podpisu Apple i zainstalowania tej wersji oprogramowania na swoim urządzeniu. Proces ten jest również znany jako "jailbreaking".

## Bibliografia

* [SHSH Blob – według Wikipedii](https://en.wikipedia.org/wiki/SHSH_blob)
* [Oszczędzanie TSS](https://tsssaver.1conan.com/v2/)

