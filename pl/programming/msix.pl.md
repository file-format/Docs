{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Co to jest plik MSIX?",
  "description":"Poznaj plik MSIX i interfejsy API, które mogą tworzyć i otwierać pliki MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Czym jest plik MIX?

Plik MSIX to format pakowania aplikacji systemu Windows, który jest używany do tworzenia i dystrybucji aplikacji w systemie Windows 10. Jest to nowoczesny format pliku pakietu w porównaniu z [APPX](/pl/programming/appx/) i MSI, które zostaną ostatecznie wycofane do tego nowego formatu pliku. Może być używany do wdrażania aplikacji Win32, WPF i Windows Forms. Pliki MSIX są niezawodne i służą do optymalizacji sieci i miejsca na dysku. Deweloperzy używają ich do dystrybucji programów wśród użytkowników końcowych za pośrednictwem Microsoft Store (wcześniej znanego jako Windows Store).

## Format pliku MSIX — więcej informacji

Pliki MSIX są skompresowane [ZIP](/pl/compression/zip/), a wszystkie pliki są zawarte w spakowanym pliku. Oprócz plików związanych z aplikacją plik MSIX zawiera pliki konfiguracyjne [.xml](/pl/web/xml/), które zawierają informacje związane z instalacją aplikacji.

## Co znajduje się w pakiecie MSIX?

Pakiet MSIX składa się z następujących plików.

* `AppxBlockMap.xml` — znany jako plik mapy bloków pakietu, jest to dokument XML zawierający listę plików aplikacji wraz z indeksami i skrótami kryptograficznymi dla każdego bloku danych przechowywanych w pakiecie.
* `AppxManifest.xml` — dokument XML zawierający informacje wymagane do wdrożenia, wyświetlenia i aktualizacji aplikacji MSIX. Te informacje obejmują tożsamość pakietu, zależności pakietu, wymagane możliwości, elementy wizualne i punkty rozszerzalności.
* `AppxSignature.p7x` — plik generowany podczas podpisywania pakietu. Wszystkie pakiety MSIX muszą zostać podpisane przed instalacją. Dzięki AppxBlockmap.xml platforma może zainstalować pakiet i zostać zweryfikowana.

## Bibliografia

* [Przegląd MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Utwórz pliki APPX za pomocą Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

