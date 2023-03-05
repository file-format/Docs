{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S-Datei - Was ist eine M4S-Datei?",
  "description":"Erfahren Sie mehr über das M4S-Dateiformat und APIs, die M4S-Dateien erstellen und öffnen können.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Was ist eine M4S-Datei?

Eine M4S-Datei ist ein kleines Segment eines Videos, das mit der Streaming-Technik **MPEG-DASH** über das Internet gestreamt wird. Es enthält ein Videosegment in Form von Binärdaten. Die empfangende Anwendung (normalerweise ein Webbrowser oder Mediaplayer) spielt diese Segmente in der Reihenfolge ab, in der sie empfangen wurden. Das erste M4S-Segment wird durch die darin enthaltenen Initialisierungsdaten identifiziert. **Zusammenfassung**: M4S-Dateien sind kleine einzelne Mediensegmente einer vollständigen Datei.

## M4S-Dateiformat

M4S-Dateien basieren auf dem [ISO Base Media File (ISOBMFF)-Format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Diese kleinen Segmente einer großen Datei können unabhängig voneinander über HTTP heruntergeladen werden. Wenn Sie also eine große [MP4](/de/video/mp4/)-Filmdatei haben, kann diese mit der MPEG-DASH-Technik (Dynamic Adaptive Streaming over HTTP) gestreamt werden, indem sie als M4S-Segmentdateien segmentiert wird. Wenn diese große Filmdatei als M4S auf die Disc heruntergeladen wird, werden mehrere M4S-Dateien heruntergeladen. Wenn alle diese .m4s-Segmente verkettet werden, wird eine vollständige abspielbare Datei erstellt. Die Mediaplayer können die Datei nicht abspielen, es sei denn, das erste Initialisierungssegment ist auch mit der Datei verfügbar.

## Über MPEG-DASH-Streaming

MPEG-DASH verwendet eine Streaming-Technik mit adaptiver Bitrate, die es ermöglicht, Medieninhalte in hoher Qualität über das Internet zu streamen. Dazu wird der Inhalt in eine Folge kleiner Segmente aufgeteilt, die über HTTP gestreamt werden. Auf diese Weise können große Mediendateien wie Filme, Podcasts oder die Live-Übertragung eines Sportereignisses gestreamt werden. Diese Segmente werden mit unterschiedlichen Bitraten codiert. Die MPEG-DASH-fähigen Mediaplayer wählen automatisch das Segment mit der höchsten Bitrate mithilfe eines Bitraten-Anpassungsalgorithmus aus. Dies vermeidet das Blockieren oder Umpuffern von Ereignissen in der Wiedergabe.

### Open-Source-API für M4S-Dateien

Es sind Open-Source-APIs verfügbar, die zum Lesen und Konvertieren von M4S-Dateien verwendet werden können.

* [libdash](https://github.com/bitmovin/libdash) – .NET-API für M4S-Dateien
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) – Javascript-Client für M4S-Datei
* [Go-Bibliothek zum Erstellen von Dash-Dateien](https://github.com/zencoder/go-dash)

### Open-Source-API zum Konvertieren von M4S in MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Verweise ###

* [Format der ISO-Basismediendatei (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamisches adaptives Streaming über HTTP – MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

