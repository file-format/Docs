{
  "date" : "2019-10-11",
  "keywords" :[ "plik mov", "format pliku mov", "co to jest plik mov", "plik", "przykład mov", "rozszerzenie pliku mov", "rozszerzenie", "format", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik MOV — format pliku filmowego Apple QuickTime",
  "description":"Poznaj format pliku MOV i interfejsy API, które mogą tworzyć i otwierać pliki MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Czym jest plik MOV?

Plik MOV to typ pliku wideo opracowany przez firmę Apple Inc., który zawiera jedną lub więcej ścieżek. Każda ścieżka przechowuje film, audio, klipy filmowe i napisy. Jest to kontener multimedialny, który może przechowywać różnego rodzaju elementy multimedialne. Format wideo MOV jest zgodny zarówno z systemami Windows, jak i Macintosh. Wykorzystuje kodowanie MPEG-4 do kompresji, a ścieżki są utrzymywane w obiektach zwanych atomami, które są umieszczone w hierarchicznej strukturze danych.

## Krótka historia formatu pliku MOV

Format plików MPEG-4 wyewoluował ze specyfikacji QuickTime File Format (**QTFF**) w 2001 roku. Międzynarodowa Organizacja Normalizacyjna zatwierdziła ten format, a specyfikacje systemów MPEG-4 część 1 zostały opublikowane w 1999 roku. W 2001 roku plik z poprawkami format [MP4](/pl/video/mp4/) został opublikowany.

Pierwsza wersja MP4 została poprawiona w 2003 roku jako MPEG-4 Part 14 (ISO/IEC 14496-14:2003). W 2004 roku MP4 został uogólniony w celu zdefiniowania ogólnej struktury wszystkich plików multimedialnych opartych na czasie. Dlatego teraz jest używany jako podstawa dla różnych innych formatów plików multimedialnych.

## Format pliku QuickTime (QTFF) — więcej informacji

Aby pracować z cyfrowymi multimediami, QTFF może przechowywać wiele rodzajów danych. Jest to pomysł na format wymiany mediów cyfrowych, ponieważ format ten określa standardy opisu wszelkiego rodzaju struktur medialnych. Format pliku składa się z elastycznej kolekcji obiektów zorientowanych obiektowo. Do przechowywania filmów na dyskach QuickTime wykorzystuje dwie struktury tj. `atomy` i `atom QT`.

### Atomy

Atom to podstawowa jednostka pliku QuickTime. Istnieją dwa główne pola w każdym atomie przed jakimkolwiek innym polem: pola rozmiaru i typu. Pole rozmiaru pokazuje rozmiar atomu, podczas gdy pole typu wskazuje typ danych przechowywanych w atomie. Z natury atomy są hierarchiczne, co oznacza, że jeden atom może zawierać inne atomy, które nadal mogą zawierać inne. Układ przykładowego atomu pokazano na poniższym obrazku.

Każdy atom ma dwie części, „nagłówek” i „dane”. Nagłówek zawiera pola rozmiaru i typu, a część danych zawiera rzeczywiste dane. Ponadto każde pole jest wyjaśnione poniżej:

### Rozmiar atomu

Nagłówek i zawartość atomu są wskazywane przez 32-bitową liczbę całkowitą znaną jako rozmiar atomu. Pole rozmiaru zawiera rozmiar atomu w bajtach, wyrażony w 32-bitowej liczbie całkowitej bez znaku.

### Typ atomu

Typ atomu jest również pokazywany przez 32-bitową liczbę całkowitą, która jest najczęściej traktowana jako czteroznakowe pole o wartości knemonicznej, takie jak „moov” (0x6D6F6F76) dla atomu filmowego lub „trak” (0x7472616B) dla atom śladu. Poznanie typu atomu umożliwia interpretację jego danych.

### Atomy QT i pojemniki na atomy

Atomy QT zapewniają format przechowywania ogólnego przeznaczenia i mają rozszerzony nagłówek składający się z pól Rozmiar, Typ, Identyfikator atomu i Liczba atomów potomnych. Atomy QT są opakowane w kontener atomów, unikalną strukturę danych mającą nagłówek z liczbą blokad. W każdym pojemniku na atomy znajduje się jeden atom główny, który jest atomem QT. Układ atomu QT pokazano na poniższym rysunku.

Nagłówek kontenera atomu QT zawiera następujące dane:

Zarezerwowany: 10-bajtowy element o wartości 0.

Lock Count: 16-bitowa liczba całkowita o wartości 0.

Nagłówki atomów QT zawierają następujące dane:

**Rozmiar -** Nagłówek i zawartość atomu QT są wskazywane w bajtach przez 32-bitową liczbę całkowitą. W przypadku atomu liścia pole to zawiera wielkość pojedynczego atomu.

**Typ -** Typ atomu jest wskazywany przez 32-bitową liczbę całkowitą. W przypadku, gdy jest to atom główny, wartość jest ustawiona na „sean”.

**Atom ID -** Jest to 32-bitowa liczba całkowita, która pokazuje identyfikator atomu i musi być unikalna dla wszystkich rodzeństwa. Atom główny zawsze ma wartość identyfikatora atomu równą 1.

**Zarezerwowane -** 16-bitowa liczba całkowita, która musi być ustawiona na 0.

**Liczba dzieci -** 16-bitowa liczba całkowita wskazująca liczbę atomów dzieci w atomie.

**Zarezerwowane -** 32-bitowa liczba całkowita, która musi być ustawiona na 0.

## Struktura plików MOV

Pliki MOV składają się z następujących po sobie fragmentów. Każdy fragment ma 8-bajtowy nagłówek: 4-bajtowy rozmiar fragmentu (big-endian, najpierw wysoki bajt) i 4-bajtowy typ fragmentu - jeden z predefiniowanych podpisów: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", „clip”, „crgn”, „sync”, „chap”, „tmcd”, „scpt”, „ssrc”, „PICT”. Pierwsza porcja jest typu „ftype” i ma podtyp o przesunięciu 8. MOV zdefiniowany przez podtyp, który musi być „qt”. Aby skomponować plik MOV, potrzebne są iteracyjne fragmenty, dopóki nie zostanie wykryty nieznany typ.

Oto `przykładowy przykład`: po sprawdzeniu danych binarnych przykładowego pliku MOV widać, że zaczyna się on od podpisu **ftyp** (szesnastkowo: 66 74 79 70) z przesunięciem 4, które definiuje typ pliku kontenera QuickTime. Podtyp pliku to **qt~_~_** (hex: 71 74 20 20), co wskazuje na typ pliku MOV. Pierwszy blok ma rozmiar 32 (heks: 00 00 00 20, big-endian, najpierw wysoki bajt), rozmiar znajduje się przy przesunięciu 0. Przy przesunięciu 32 (heks: 20) znajduje się drugi fragment, który ma rozmiar 8 i wpisz **mdat** (szesnastkowo: 6D 64 61 74).

Następna porcja znajduje się pod offsetem 32+8#40 (hex: 28) i ma rozmiar 3 263 028 (hex: 00 31 CA 34) i wpisz **mdat** (hex: 6D 64 61 74) z offsetem 44 (hex : 2C). Następny fragment znajduje się pod offsetem 40 + 3 263 028#3 263 068 (hex: 00 31 CA 5C) i ma rozmiar 21 189 (hex: 00 00 52 C5) i typ **moov** (hex: 6D 6F 6F 76) z offsetem 1 836 019 574 (szesnastkowo: 00 31 CA 60). To jest ostatnia porcja, więc całkowity rozmiar pliku wynosi 3 263 068+21 189#3 284 257 bajtów.

## Jak przekonwertować plik MOV?

Dostępnych jest wiele odtwarzaczy multimedialnych i programowych edytorów wideo do konwersji plików MOV na inne popularne formaty plików wideo. Niektóre z odtwarzaczy multimedialnych, które mogą konwertować pliki MOV do innych formatów, obejmują:

* Odtwarzacz multimedialny VideoLAN VLC
* Odtwarzacz Eltima Elmedia

Kilka odtwarzaczy multimedialnych i edytorów wideo, w tym odtwarzacz multimedialny VideoLAN VLC i Eltima Elmedia Player, może konwertować pliki MOV do innych formatów. To oprogramowanie może konwertować pliki MOV do następujących formatów wideo.

* Wideo MPEG-4 — [MP4](/pl/wideo/mp4/)
* Wideo WebM – [WEBM](/pl/video/webm/)
* Transmisja strumienia wideo – [TS](/pl/video/ts/)
* Format systemów zaawansowanych – [ASF](/pl/video/ts/)
* Ogg Vorbis Audio – [OGG](/pl/audio/ogg/)
* Dźwięk MP3 — [MP3](/pl/audio/mp3/)
* Darmowy bezstratny kodek audio — [FLAC](/pl/audio/flac/)
* WAVE Audio – [WAV](/pl/audio/wav/)

## Open Source API dla plików MOV

* [React Native API do konwersji MOV na MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [API Pythona do naprawy plików MOV](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API do konwersji MOV na GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Bibliografia

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

