{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl-Datei", "Erweiterung", "Format", "was ist eine wpl-Datei", "Musik", "wpl-Dateiformat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das WPL-Dateiformat und APIs, die WPL-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"WPL - Windows Media Player-Wiedergabelistendatei",
  "linktitle" :"WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Was ist eine WPL-Datei?
Eine Datei mit der Erweiterung .wpl enthält die Playlist der Songs, die auf dem Microsoft Windows Media Player abgespielt werden sollen. Diese Dateien werden normalerweise von Benutzern für ihre Video- und Audiosammlungen erstellt. Die in eine WPL-Datei geschriebenen Inhalte sind nur Verzeichnispfade oder Speicherorte für die Multimediadateien, die vom Ersteller der WPL-Datei ausgewählt wurden, sodass die Media-Player-Anwendung die Multimediainhalte von ihren Verzeichnisspeicherorten sofort finden und wiedergeben kann.

## WPL-Dateiformat
WPL (Windows Media Player Playlist) ist ein proprietäres Dateiformat, das in Microsoft Windows Media Player Version 9 oder höher verwendet wird. Es ist ein Computerdateiformat, das Multimedia-Wiedergabelisten speichert. Standardmäßig wird die Playlist mit der Erweiterung .wpl (Windows Media Player Playlist) gespeichert. Sie können stattdessen die Erweiterung [.m3u](/de/audio/m3u) verwenden, wenn Sie Ihre Daten-Discs auf einem Gerät abspielen möchten, das diese Erweiterung nicht unterstützt. Die Elemente einer WPL-Datei werden im XML-Format dargestellt. Das Top-Level-Element "smil" gibt an, dass die Elemente der Datei der Struktur der Synchronized Multimedia Integration Language (SMIL) folgen. Die Datei wird mit der Erweiterung .wpl erstellt und gespeichert und ihr MIME-Typ ist application/vnd.ms-wpl.

### WPL-Beispiel
Hier ist ein Beispiel für eine wpl-Datei:
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




## Verweise ##

* [MPEG-1 Audio Layer II – Von Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


