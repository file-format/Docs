{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "plik", "rozszerzenie", "format", "co to jest plik cda", "muzyka", "format pliku cda", "specyfikacja formatu pliku cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku CDA i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki CDA.",
  "title" :"CDA - plik skrótu ścieżki dźwiękowej CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Czym jest plik CDA?

Plik z rozszerzeniem .cda to mały plik pośredniczący generowany przez system Microsoft Windows dla każdej ścieżki audio na płycie audio CD. Pliki te zawierają typowe informacje, takie jak czasy utworów i skrót Windows, który umożliwia użytkownikom dostęp do określonych ścieżek audio. Pliki CDA nie są muzyką, ale wskazują plik muzyczny istniejący gdzieś w pamięci. Można powiedzieć, że jest to skrót do pliku audio znajdującego się na płycie CD.

## Format pliku CDA

Format pliku CDA służy do informowania komputera, który plik audio ma być odtwarzany na płycie CD. Tak więc pliki CDA stają się bezużyteczne oddzielone od płyty CD, którą reprezentują. Pliki CDA są powszechnie uważane za zasoby RIFF. W aktualnej wersji pliku .cda istnieje tylko jeden fragment o nazwie „CDDA” i zawierający tylko jeden blok danych o nazwie „FMT”. Ten blok ma długość 24 bajtów. Identyfikator utworzony przez system Windows jest używany przez napęd CD związany z systemami Windows 95 i Windows 98, a jego odtwarzacz nie może połączyć się z FreeDB ani CDDB. Aby mógł wyświetlać tytuł utworu oraz nazwisko wykonawcy, należy ręcznie wpisać te informacje w pliku cdplayer.ini.

### Organizacja pliku CDA

Poniższa tabela zawiera informacje o typowych offsetach:
| przesunięcie | długość | treść |
---|---|---|
| 0x00 | 4 | 4 znaki ASCII „RIFF” |
| 0x04 | 4 | rozmiar następującego fragmentu: zawsze 36 (44 - 8), na 4 bajtach (zamówienie Intela) |
| 0x08 | 4 | identyfikator porcji: 4 znaki ASCII "CDDA" |
| 0x0C | 4 | 3 znaki ASCII „fmt”, po których następuje spacja |
| 0x10 | 4 | długość fragmentu: zawsze 24, na 4 bajty (kolejność Intela) |
| 0x14 | 2 | wersja formatu CD, na 2 bajtach (zamówienie firmy Intel). W maju 2006 r. zawsze równe 1. |
| 0x016 | 2 | numer zakresu, na 2 bajtach (zamówienie Intela). Pierwszy utwór ma numer 1. |
| 0x18 | 4 | identyfikator obliczony przez system Windows dla cdplayer.exe. |
| 0x1c | 4 | przesunięcie zakresu, w liczbie klatek (zamówienie firmy Intel) |
| 0x20 | 4 | czas trwania utworu, całkowita liczba klatek (zamówienie Intel) |
| 0x24 | 1 | pozycja zakresu: ramki |
| 0x25 | 1 | pozycja zakresu: sekundy |
| 0x26 | 1 | pozycja zakresu: minuty |
| 0x27 | 1 | bajt zerowy (wartość binarna 0) |
| 0x28 | 1 | czas trwania utworu: klatki |
| 0x29 | 1 | czas trwania utworu: sekundy |
| 0x2a | 1 | czas trwania utworu: minuty |
| 0x2b | 1 | bajt zerowy (wartość binarna 0) |

## Bibliografia

* [plik .cda – z Wikipedii](https://en.wikipedia.org/wiki/.cda_file)

