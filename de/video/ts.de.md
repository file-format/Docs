{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TS-Dateiformat - Video-Transport-Stream-Datei",
  "keywords" :[ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"Erfahren Sie, was eine TS-Datei und APIs sind, die TS-Dateien erstellen und öffnen können.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
"identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Was ist eine TS-Datei?

Eine Datei mit der Erweiterung .ts ist ein Videostream, der die Daten auf DVDs speichert. Es verwendet den Komprimierungsalgorithmus MPEG-2 ([.mpeg](/de/video/mpg/)), um maximale Effizienz und Kompatibilität über verschiedene Medientypen wie Internet-Streaming und -Rundfunk zu erreichen. Das TS-Dateiformat wurde erstellt, damit es auf Geräten mit schlechter Internetverbindung, wie z. B. Smart TV, abgespielt werden kann.

## TS-Dateiformat – Weitere Informationen

Daten in einer TS-Datei ähneln [MP4](/de/video/mp4/)-Dateien, sind jedoch in winzige Teile unterteilt. Jeder Chunk besteht aus einem winzigen Videostück, gefolgt von einem kleinen Audiostück und einer optionalen Beschriftung. Eine einzelne TS-Datei besteht aus vielen solcher Chunks. Zusätzlich zu Video, Audio und Untertiteln umfasst jeder Chunk auch einige zusätzliche Daten zum Erkennen von Fehlern im Chunk. Aus diesem Grund sind TS-Dateien etwas größer.

### Warum das TS-Dateiformat verwenden?

Wenn also TS-Dateien etwas groß sind, welchen Vorteil bietet es, sie anstelle anderer Dateiformate zu verwenden? Nun, beim Rundfunk können die winzigen Video- und Audiostücke in Echtzeit über die Kommunikationsmedien (Kabel oder Funk) gesendet werden. Die zusätzlichen Daten in den Chunks werden vom Empfänger verwendet, um die fehleranfälligen Chunks zu überspringen.

Außerdem werden TS-Dateien verwendet, da das Sendesystem nicht den gesamten Stream zum Abspielen benötigt. Die Übertragung kann abgeholt und in Echtzeit genutzt werden, indem Audio und Video zusammengesetzt werden.

## Wie spielt man TS-Dateien ab?

Nun, TS-Dateien können im beliebten [VideoLAN VLC Media Player] (https://www.videolan.org/vlc/features.html) geöffnet und abgespielt werden, der kostenlos zum Download zur Verfügung steht.

## Verweise ##

* [MPEG-Transportstrom – Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

