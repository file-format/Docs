{
  "date" : "2021-03-08",
  "keywords" :["RB", "Nuvo Media's Rocket eBook device", "plik", "rozszerzenie", "format", "eBook"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku RB dla urządzenia Rocket eBook firmy Nuvo Media i interfejsach API, które mogą tworzyć i otwierać pliki RB.",
  "title" :"RB - Rocket eBook File",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Czym jest plik RB?

Plik z rozszerzeniem .rb zawiera zawartość eBooka Rocket. eBook Rocket jest w rzeczywistości urządzeniem wyprodukowanym przez Nuvo Media; wypuścili to urządzenie w 1998 roku. Chociaż eBook Rocket może wyświetlać obrazy, ale tylko w trybie czarno-białym. Ma ekran o rozdzielczości 106 dpi lub 480 x 320 pikseli na ekranie dotykowym 4,5 x 3 cale. Rocket eBook łączy się z komputerem za pośrednictwem portu szeregowego, aby pobierać eBooki w formacie pliku RB. Pliki RB mogą korzystać z DRM, ale ta technologia nie jest używana w nowoczesnych eBookach. Plik RB zwykle zawiera plik HTML z obrazami i plik pseudo-OPF ze wszystkimi metadanymi (.info).

## Specyfikacja techniczna formatu pliku RB ##

Magiczna liczba (w systemie szesnastkowym) pojawia się w pierwszych 4 bajtach pliku: B0 0C B0 0C.

Wygląda na to, że następne dwa bajty to numer wersji, na przykład „02 00”, co oznacza wersję główną 2 i wersję pomocniczą 0.

Następne cztery bajty zawierają tekst „NUVO”, po którym następują 4 bajty 00h.

Następne 4 bajty to data utworzenia książki, zakodowana jako int16. To stawia nas w przesunięciu 0Eh. Stara wersja ORocketLibrary zakodowała pełną wartość roku (tj. 1999 to „CF 07”, 2000 to „D0 07”). W najnowszej wersji tm_year jest zapisywane dosłownie, tj. 100 oznacza rok 2000 („64 00”). Po roku następuje int8 reprezentujący względny numer miesiąca 1 i int8 reprezentujący dzień miesiąca.

Kolejne 6 bajtów to 00h. Mogą one być zarezerwowane do ustawiania czasu.

Bezwzględne przesunięcie „Spisu treści” jest zawarte w int32 w przesunięciu 18h.

Po tym następuje int32 zawierający długość pliku .rb. Służy do określenia, czy pliki są kompletne, czy nie.

Cały ten fragment bajtów (od 20h do 128h) wydaje się być potrzebny tylko tytułowi, który jest zaszyfrowany. W tytułach niezaszyfrowanych są one zawsze zerowe.

W większości przypadków następuje spis treści (przy przesunięciu 128). Rozpoczyna się liczbą int32 liczby wpisów „stron” (sekcji pliku .rb) w ToC. Każdy wpis składa się z nazwy (dopełnionej zerami do 32 bajtów), po której następują 3 liczby typu int32: długość segmentu danych, pozycja w pliku .rb i flaga dla tego wpisu. Na dzień dzisiejszy znane wartości to: 1 (zaszyfrowane), 2 (strona informacyjna) i 8 (deflowane). W razie potrzeby wszystkie nazwy są dostosowywane, aby zapewnić, że wszystkie są niepowtarzalne.

## Bibliografia

* [Czytnik elektroniczny — przez MobileRead](https://en.wikipedia.org/wiki/Czytnik elektroniczny)

