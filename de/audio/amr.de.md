{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "Datei", "Erweiterung", "Format", "was ist eine amr-Datei", "Musik", "amr-Dateiformat", "amr-Datei", "amr-Datei konvertieren in mp3", "amr-Datei abspielen" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das AMR-Dateiformat und APIs, die AMR-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"AMR - Adaptive Multi-Rate-Codec-Datei",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Was ist eine AMR-Datei?
Die Datei mit der Erweiterung .amr ist ein Audiodatenformat, das für den Audio-Codec **Adaptive Multi-Rate** relevant ist; besteht aus einem Schmalband-Sprachcodec mit mehreren Raten, der Schmalbandsignale mit einer Bitrate von 4,75 bis 12,2 kbit/s codiert, wobei die Sprache in Mautqualität bei 7,4 kbit/s beginnt; verwendet eine Verbindungsanpassung, um aus einer von acht verschiedenen Bitraten auszuwählen.

## AMR-Dateiformat
Das AMR-Dateiformat verwendet viele Codierungstechniken, der ACELP-Algorithmus (Algebraic Code Excited Linear Prediction) ist eine der besten Techniken; entwickelt, um von Menschen gesprochenes Audio effizienter zu komprimieren. AMR wurde 1999 von 3GPP als standardmäßiger Sprach- oder Sprachcodec festgelegt. Das AMR-Dateiformat wird auch zum Speichern des gesprochenen Audios verwendet, indem der Audiocodec **Adaptive Multi-Rate** verwendet wird, der von vielen Smartphones zum Speichern von Aufzeichnungen verwendet wird Reden.

### Struktur des Dateiformats
AMR (Adaptive Multi-Rate) ist ein Audioformat; weit verbreitet in verschiedenen mobilen Anwendungen und Geräten, typischerweise in Audio-Player/Recorder oder in VoIP-Anwendungen. AMR kann weiter klassifiziert werden als:

1. AMR-NB (Schmalband)
2. AMR-WB (Breitband)

Normalerweise bezieht sich AMR auf AMR-NB. Das AMR-Dateiformat hat die folgende Struktur:

Jede AMR-Datei enthält einen 6-Byte-Header, der die Datei als AMR-Audio erkennt. Dieser Header ist immer eingestellt auf:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Dies ist normalerweise bei allen AMR-NB-Dateien ähnlich. Wenn der Header einem Standard entspricht, ist die Datei wahrscheinlich beschädigt und sollte nicht verwendet werden. Die AMR-Datei besteht aus einer ganzen Anzahl gepackter Audioframes. Diese Frames bestehen jeweils aus 20 ms Audio. Jeder Rahmen kann mit einem der gültigen AMR-NB-Modi (0-7, 8 SID im DTX-Modus) codiert werden. Da die Frames mit unterschiedlichen Bitraten codiert werden können, wird dieses typische Verfahren als Adaptive Multi-Rate (AMR) bezeichnet.
#### AMR-Modi
Im Folgenden sind die verschiedenen AMR-Modi und ihre entsprechenden Bitraten aufgeführt:

|MODUS| BITRATEN|
---|---|
|0| AMR 4.75 – Kodiert mit 4,75 kbit/s|
|1 | AMR 5.15 – Kodiert mit 5,15 kbit/s|
|2 | AMR 5.9 – Kodiert mit 5,9 kbit/s|
|3 | AMR 6.7 – Kodiert mit 6,7 kbit/s|
|4 | AMR 7.4 – Kodiert mit 7,4 kbit/s|
|5 | AMR 7.95 – Codiert mit 7,95 kbit/s|
|6 | AMR 10.2 – Codiert mit 10,2 kbit/s|
|7 | AMR 12.2 – Codiert mit 12,2 kbit/s|

Die Rahmengröße der AMR-Modi in Bytes (einschließlich des Header-Bytes) ist unten angegeben:

|CMR |MODUS |FRAME SIZE( in Bytes )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5,9 |16|
|3 |AMR 6,7 |18|
|4 |AMR 7,4 |20|
|5 |AMR 7,95 |21|

## Verweise ##

* [Adaptive Multi-Rate Audiocodec – von Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [RTP-Payload-Format und Dateispeicherformat für AMR- und AMR-WB-Audio-Codecs](https://tools.ietf.org/html/rfc4867#page-35)

