{
  "date" : "2021-08-10",
  "keywords" :[ "plik .ovf", "format pliku", "co to jest plik .ovf", "plik", "rozszerzenie pliku"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Dowiedz się, co to jest format pliku .ovf i interfejsy API, które mogą tworzyć i otwierać pliki OVF.",
  "title" :"Format pliku OVF - Otwórz plik wirtualizacji",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Czym jest plik OVF?

Plik OVF to plik tekstowy zawierający informacje o pakowaniu i dystrybucji oprogramowania działającego na maszynie wirtualnej. Jest sformatowany zgodnie z [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf), który opisuje wszystkie wymagania (takie jak bezpieczeństwo, przenośność, wydajność i możliwości rozbudowy) dotyczące uruchamiania aplikacji na maszynach wirtualnych. Międzynarodowa Organizacja Normalizacyjna (ISO) przyjęła OVF jako normę ISO 17203.

## Krótka historia formatu plików OVF

Format pliku OVF został wprowadzony przez DMTF (Distributed Management Task Force), który tworzy otwarte standardy zarządzania. Jest niezależny od konkretnego hiperwizora lub architektury zestawu instrukcji. Pakiet OVF zawiera jeden lub więcej systemów wirtualnych, z których każdy można zainstalować na maszynie wirtualnej.

## Format pliku OVF — więcej informacji

Pakiet OVF składa się z wielu plików umieszczonych w jednym katalogu. Wśród nich znajduje się dokładnie jeden plik deskryptora OVF (z rozszerzeniem .ovf), który jest przechowywany w formacie pliku [XML](/pl/web/xml/). Opisuje spakowane informacje o maszynie wirtualnej i metadane dotyczące pakietu OVF, takie jak:

* Nazwa
* Wymagania sprzętowe
* odniesienia do innych plików w pakiecie OVF i
* Opisy czytelne dla człowieka

Inne pliki, które można znaleźć w pakiecie OVF, to jeden lub więcej obrazów dysków oraz opcjonalnie pliki certyfikatów i inne pliki pomocnicze.

## Bibliografia

* [Otwarty format wirtualizacji - DMTF](https://www.dmtf.org/standards/ovf)
* [Specyfikacje formatu plików OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

