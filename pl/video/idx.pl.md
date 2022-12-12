{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX – kodek wideo o wysokiej wydajności",
  "description":"Dowiedz się o formacie pliku IDX i interfejsach API, które mogą tworzyć i otwierać pliki IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Czym jest plik IDX?

Plik IDX to plik indeksu napisów, który wskazuje listę metadanych napisów w pliku .sub (VobSub Subtitles). Jest tworzony i używany przez aplikację VobSub, która pozwala użytkownikom wyodrębnić napisy z płyt DVD i zrzucić je do pliku SUB. Pliki IDX zawierają znaczniki czasu i przesunięcia bajtów używane do wskazywania każdego pojedynczego napisu. VobSub zawsze tworzy plik IDX wraz z odpowiednim plikiem SUB.

## Format pliku IDX — więcej informacji

Pliki IDX są generowane i zapisywane jako zwykłe pliki tekstowe, które można otworzyć w dowolnym edytorze tekstu. Plik IDX zawiera informacje odczytywane przez odtwarzacze multimedialne w celu odczytania parametrów, takich jak kolor tekstu napisów do wyświetlenia na ekranie, położenie tekstu napisów na ekranie.

### Ustawienia napisów IDX

Typowy plik IDX przechowuje te informacje o metadanych na początku pliku. Ustawienia napisów zaczynają się od **#**. Sygnatury czasowe i odniesienia do obrazów są dodawane po wszystkich tych ustawieniach napisów i zaczynają się od **znacznik czasu:**.

## Przykład formatu pliku IDX

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## Jak korzystać z pliku IDX?

Jeśli masz pliki Sub i IDX dla filmu, możesz odtwarzać te napisy wraz z filmem, dla którego zostały utworzone. Wiele aplikacji, takich jak VLC, GOM Player, PotPlayer lub PowerDVD, ma możliwość ładowania tych plików SUB i IDX i odtwarzania ich razem z filmem. Aplikacje mogą również osadzać pliki napisów SUB i IDX w plikach [.mkv](/pl/video/mkv/).

## Konwertuj IDX na SRT

[SRT](/pl/video/srt/) (format pliku SubRip) to prosty plik z napisami zapisany w formacie pliku SubRip. Jest częściej używany w porównaniu z formatem pliku VobSub. Tak więc, jeśli chcesz przekonwertować pliki SUB/IDX do formatu pliku SRT, dostępne są narzędzia innych firm, których można użyć do osiągnięcia tego celu. Konwerter SUB/IDX na SRT, dostępny na SubtitleTools.com, jest jednym z takich narzędzi, które pobiera pliki SUB i IDX jako dane wejściowe i konwertuje te napisy VobSub na pliki SRT.

## Bibliografia

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub – Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

