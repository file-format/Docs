{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku MKV",
  "keywords" :["mkv", "matroska wideo", "format mkv", "jak odtwarzać pliki mkv", "wideo", "plik", "format"],
  "description":"Poznaj format pliku MKV i interfejsy API, które mogą tworzyć i otwierać pliki MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Czym jest plik MKV? ##

MKV (Matroska Video) to kontener multimedialny podobny do formatu [MOV](/pl/video/mov/) i [AVI](/pl/video/avi/), ale obsługuje więcej niż jedną ścieżkę audio i napisy w tym samym pliku. Plik MKV to format kontenera multimedialnego Matroska używany do wideo. MKV jest oparty na Extensible Binary Meta Language i obsługuje kilka formatów kompresji wideo i audio. Główna różnica między MKV a innymi formatami wideo polega na tym, że MKV jest kontenerem, a nie kodekiem. Pliki MKV są zapisywane z rozszerzeniem .mkv. MKV może zawierać dźwięk, wideo i napisy w jednym pliku, nawet jeśli te elementy używają różnych typów kodowania. Na przykład możesz mieć plik MKV zawierający wideo H.264 i MP3 lub AAC dla dźwięku. MKV obsługuje również opisy, oceny, okładki, a nawet punkty rozdziałów. Istnieje kilka kluczowych funkcji, dzięki którym MKV jest przyszłościowy. Funkcje te obejmują:

- Wsparcie dla szybkiego wyszukiwania.
- Możliwość wyboru różnych strumieni audio i wideo.
- Wsparcie dla napisów (kodowane na stałe i programowane).
- Wsparcie dla metadanych, rozdziałów i menu.
- Możliwość przesyłania strumieniowego online.
- Możliwość odzyskiwania błędnych plików, które zapewniają możliwość odtwarzania uszkodzonych plików.

## Krótka historia ##

Plik MKV powstał w 2002 roku w Rosji. Głównym programistą był Lasse Kärkkäinen, który współpracował z założycielem Matroski, Steve'em Lhomme, oraz zespołem programistów. MKV został opracowany jako projekt o otwartych standardach, co oznacza, że jest open source i darmowy. Z biegiem czasu format był ulepszany i stał się podstawą formatu multimedialnego WebM w 2010 roku.

## Projekt Matroski ##

Matroska dodaje następujące ograniczenia do specyfikacji EBML.

- **DocType** **nagłówka EBML** musi mieć wartość „matroska”.
- **EBLMMaxIDLength** nagłówka **EBML** musi wynosić 4.
- **EBLMMaxSizeLength** nagłówka **EBML** musi zawierać się w przedziale od 1 do 8 (włącznie).

Wszystkie elementy najwyższego poziomu są zakodowane w 4 oktetach.

- Kody języków: Matroska (wersje od 1 do 3) używała kodów języków, które mogą być albo 3-literowym formularzem bibliograficznym ISO-639-2 (jak „fre” dla francuskiego), albo dodatkowym kodem kraju, takim jak „fre-ca " dla francuskiego francuskiego. Począwszy od Matroski w wersji 4, dla kodów języków MOŻE być używany ISO 639-2 lub BCP 47, chociaż zaleca się BCP 47.
- Typy fizyczne: mają różne znaczenie zarówno dla plików audio, jak i wideo. Na przykład ChapterPhysicalEquiv = 60 oznacza (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) dla audio i (DVD / VHS / LASERDISC) dla wideo.
- Struktura bloku - Nagłówek bloku: Nagłówek bloku zawiera informacje dotyczące numeru utworu, znaczników czasu, rodzaju sznurowania itp.
- Sznurowanie: Jest to mechanizm oszczędzania miejsca podczas przechowywania danych, który jest zwykle używany do małych bloków danych (ramek). Istnieją 3 rodzaje sznurowania:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock Structure: Jest inspirowana **Strukturą blokową**, z główną różnicą polegającą na dodaniu flag **Keyframe** i **Discardable**. Poza tym wszystko jest takie samo.

## Struktura Matroski ##

Dokument Matroska musi składać się z co najmniej jednego **Dokumentu EBML** przy użyciu **Typu dokumentu Matroska**. Każdy **Dokument EBML** musi zaczynać się od **Nagłówka EBML**, po którym następuje **Element główny EBML**, który jest zdefiniowany jako Segment. Matroska definiuje kilka elementów najwyższego poziomu, które mogą wystąpić w **segmencie**.

EBML używa systemu elementów do tworzenia dokumentu EBML. Poniżej znajduje się lista elementów najwyższego poziomu w pliku Matroska:

- **Dokument EBML**: Opakowanie dla całego pliku.
- **Nagłówek EBML**: zawiera informacje o nagłówku pliku, takie jak DocType.
- **Segment**: górny element zawierający wszystkie pozostałe elementy najwyższego poziomu.
- **SeekHead**: Zawiera pozycję segmentów innych elementów najwyższego poziomu.
- **Informacje**: Zawiera ogólne informacje o Segmencie.
- **Utwory**: najwyższy poziom informacji z wieloma opisami utworów.
- **Rozdziały**: Służy do definiowania podstawowych menu i danych partycji.
- **Klaster**: Element najwyższego poziomu zawierający strukturę bloku.
- **Wskazówki**: element najwyższego poziomu, który zawiera wszystkie wpisy lokalne w segmencie, które przyspieszają wyszukiwanie dostępu.
- **Załączniki**: Zawiera załączone pliki.
- **Tagi**: Ten element zawiera metadane opisujące Utwory, Wydania, Rozdziały, Załączniki lub Segment jako całość.

Poniższa tabela przedstawia strukturę dokumentu Matroska z większością elementów wyświetlanych w hierarchii:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Nagłówek EBML | | | |
| Segment | szukajgłowy| Szukaj | Identyfikator wyszukiwania |
| | | | Pozycja wyszukiwania |
| | Informacje | identyfikator segmentu | |
| | | SegmentNazwaPliku | |
| | | PoprzedniUID | |
| | | PoprzedniNazwa pliku | |
| | | NastępnyUID | |
| | | NastępnyNazwa pliku | |
| | | SegmentRodzina | |
| | | RozdziałPrzetłumacz | |
| | | Skala znacznika czasu | |
| | | Czas trwania | |
| | | DataUTC | |
| | | Tytuł | |
| | | Aplikacja Muxing | |
| | | Aplikacja do pisania | |
| | tory | Wpis śladu | Numer utworu |
| | | | TrackUID |
| | | | Typ toru |
| | | | Imię |
| | | | Język |
| | | | Identyfikator kodeka |
| | | | Kodek Prywatny |
| | | | Kodek-Nazwa |
| | | | wideo | Flaga z przeplotem |
| | | | | Kolejność pól |
| | | | | Tryb Stereo |
| | | | | Tryb alfa |
| | | | | Szerokość piksela |
| | | | | Wysokość piksela |
| | | | | Szerokość wyświetlacza |
| | | | | Wyświetl wysokość |
| | | | | Typ współczynnika proporcji |
| | | | | Kolor |
| | | | dźwięk | częstotliwość próbkowania |
| | | | | kanały |
| | | | | Głębokość bitowa |
| | Rozdziały | EdycjaWpis | EditionUID |
| | | | EdycjaFlagaUkryta |
| | | | EditionFlagDefault |
| | | | EdycjaFlagaZamówione |
| | | | RozdziałAtom | RozdziałUID |
| | | | | RozdziałStringUID |
| | | | | RozdziałCzasPoczątek |
| | | | | RozdziałCzasKoniec |
| | | | | RozdziałFlagaUkryta |
| | | | | Wyświetlanie rozdziału | RozdziałCiąg |
| | | | | | ChapJęzyk |
| | Klaster | Znacznik czasu |
| | | SilentTracks |
| | | Pozycja |
| | | PoprzedniRozmiar |
| | | prosty blok |
| | | Grupa bloków |
| | | Zaszyfrowany blok |
| | Wskazówki | Punkt kontrolny | Czas Cue |
| | | | Pozycje CueTrack |
| | Załączniki | Załączony plik | Opis pliku |
| | | | NazwaPliku |
| | | | FileMimeTyp |
| | | | Identyfikator pliku |
| | | | Odesłanie do pliku |
| | | | PlikUżytyCzasRozpoczęcia |
| | | | PlikUżytyCzasKoniec |
| | Tagi | Oznacz | Cele | TypDocelowyWartość |
| | | | | Typ celu |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | identyfikator rozdziału tagu |
| | | | | Identyfikator tagu załącznika |
| | | | ProstyTag | Nazwa Tagu |
| | | | | TagJęzyk |
| | | | | Znacznik domyślny |
| | | | | Ciąg tagów |
| | | | | Tagbinarny |
| | | | | ProstyTag |


### Korzystanie z kodeków ###

Jeśli nie chcesz nowego odtwarzacza multimedialnego i wolisz używać istniejącego odtwarzacza, będziesz musiał zainstalować kilka kodeków (skrót od kompresji/dekompresji). Mimo że pobieranie kodeków jest prawidłową opcją, należy uważać na źródło, ponieważ mogą one zawierać złośliwe oprogramowanie.

## Bibliografia ##

- [Matroska z Wikipedii](https://en.wikipedia.org/wiki/Matroska)

