{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Dowiedz się o formacie plików VHDX i interfejsach API, które mogą tworzyć i otwierać pliki VHDX.",
  "title" :"Format pliku VHDX - Co to jest plik VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Czym jest plik VHDX?

Plik VHDX to plik obrazu dysku w formacie pliku Virtual Hard Disk v2. Zawiera cały system operacyjny, który można załadować i używać jak każdą normalną maszynę do testowania oprogramowania lub uruchamiania oprogramowania wymagającego określonego systemu operacyjnego. VHDX, mimo że jest pełnym obrazem dysku, jest przechowywany w jednym pliku. Oprogramowanie maszyny wirtualnej, takie jak Parallels Desktop, Windows Virtual Machine i Virtual Box, może ładować i otwierać obraz dysku.

Plik VHDX można przekonwertować na [VHD](/pl/disc-and-media/vhd/) za pomocą Hyper-V Manager lub na [VDI](/pl/disc-and-media/vdi/) za pomocą VirtualBox.

## Format pliku VHDX — więcej informacji

Szczegóły formatu plików VHDX są w pełni udokumentowane i dostępne online jako [Specyfikacja formatu plików VHDX](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) w dokumentacji firmy Microsoft. Jest to rozszerzenie formatu VHD i zawiera rozszerzone możliwości. Format pliku VHDX zapewnia dodatkowe funkcje, które są dostępne w warstwach plików wirtualnego dysku twardego i wirtualnego dysku twardego. Jest bardziej zoptymalizowany i daje lepsze wyniki w zakresie konfiguracji i możliwości sprzętu pamięci masowej. Pliki VHDX można otwierać

### Wsparcie dla wirtualnych dysków twardych w VHDX

Obsługuje trzy typy wirtualnych dysków twardych.

1. **Fixed Virtual Hard Disk** — Wirtualny dysk twardy z przydzielonym stałym rozmiarem danych. Rozmiar wirtualnego dysku twardego nie zmienia się wraz z dodawaniem lub usuwaniem danych.

1. **Dynamiczny wirtualny dysk twardy** — Wirtualny dysk twardy z dynamicznym rozmiarem dysku. Jego rozmiar jest w każdej chwili tak duży, jak rzeczywiste dane do niego zapisane i metadane. Jego rozmiar pliku dynamicznie rośnie w miarę dodawania lub usuwania danych.

1. **Różnicowanie wirtualnego dysku twardego** — reprezentuje bieżący wirtualny dysk twardy jako zestaw zmodyfikowanych bloków w porównaniu z nadrzędnym plikiem wirtualnego dysku twardego.

## Bibliografia

* [Specyfikacje formatu plików VHDX](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD – z Wikipedii](https://en.wikipedia.org/wiki/VHD_(file_format))

