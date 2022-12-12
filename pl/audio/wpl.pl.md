{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "plik wpl", "rozszerzenie", "format", "co to jest plik wpl", "muzyka", "format pliku wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku WPL i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki WPL.",
  "title" :"WPL — plik listy odtwarzania programu Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Czym jest plik WPL?

Plik z rozszerzeniem .wpl zawiera listę odtwarzania utworów do uruchomienia w programie Microsoft Windows Media Player. Pliki te są zwykle tworzone przez użytkowników do ich kolekcji wideo i audio. Treść zapisana w pliku WPL to tylko ścieżki do katalogów lub lokalizacje plików multimedialnych wybranych przez twórcę pliku .wpl, dzięki czemu aplikacja odtwarzacza multimediów może szybko znaleźć i odtworzyć zawartość multimedialną z ich lokalizacji w katalogu.

## Format pliku WPL

WPL (Windows Media Player Playlist) to zastrzeżony format plików używany w programie Microsoft Windows Media Player w wersji 9 lub nowszej. Jest to format pliku komputerowego, który przechowuje multimedialne listy odtwarzania. Domyślnie lista odtwarzania jest zapisywana z rozszerzeniem .wpl (Windows Media Player Playlist). Zamiast tego możesz użyć rozszerzenia [.m3u](/pl/audio/m3u), jeśli chcesz odtwarzać płyty z danymi w urządzeniu, które nie obsługuje tego rozszerzenia. Elementy pliku WPL są reprezentowane w formacie XML.

Element najwyższego poziomu „smil” określa, że elementy pliku są zgodne ze strukturą Synchronized Multimedia Integration Language (SMIL). Plik jest tworzony i zapisywany z rozszerzeniem .wpl, a jego typem MIME jest application/vnd.ms-wpl.

### Przykład WPL

Oto przykład pliku wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Bibliografia ##

* [MPEG-1 Audio Layer II – Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

