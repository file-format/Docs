{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPG-Dateiformat",
  "keywords" :[ "MPG", "Datei", "Erweiterung", "Format", "Videoformat", "Was ist ein MPG-Dateiformat", "MPG-Dateiformat", "MPG-Dateiplayer", "MPEG-Komprimierung", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Erfahren Sie mehr über das MPG-Dateiformat und APIs, die erstellt und gezeigt werden können, wie MPG-Dateien geöffnet werden.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Was ist ein MPG-Dateiformat? ##

Die Datei mit der Erweiterung .mpg gehört zur Gruppe der Dateierweiterungen für MPEG-1- oder MPEG-2-Audio- und Videokomprimierung. MPEG-1 Teil 2-Video ist nicht leicht verfügbar, und diese Erweiterung (MPG-Dateiformat) verweist normalerweise auf einen MPEG-Programmstrom, der in MPEG-1 und MPEG-2 definiert ist, oder auf einen MPEG-Transportstrom, der in MPEG-2 definiert ist . Es gibt auch andere Erweiterungen wie .m2ts, die den genauen Container angeben, in diesem Fall MPEG-2 TS, aber dies hat wenig Relevanz für MPEG-1-Medien. [.mp3](/audio/mp3/) ist die häufigste Erweiterung für Dateien, die MP3-Audio enthalten. Eine MP3-Datei ist ein typischer Stream von Rohaudio; Die herkömmliche Art, MP3-Dateien zu taggen, besteht darin, Stream-Daten in "Müll"-Segmente jedes Frames zu schreiben, die die Medieninformationen speichern, aber vom **MPG-Dateiplayer** verworfen werden. Dies ist eine ähnliche Technik, die zum Taggen der AAC-Dateien verwendet wird, aber heutzutage weniger unterstützt wird.

## MPEG-Komprimierung ##

Der Name MPEG steht für Moving Pictures Experts Group. MPEG ist ein Tool zur Videokomprimierung, das die Komprimierung von Bildern und Tönen sowie die Synchronisierung der beiden beinhaltet.
Derzeit gibt es mehrere MPEG-Standards.

- MPEG-1 wird für mittlere Datenraten in der Größenordnung von 1,5 Mbit/s vorgeschlagen.
- MPEG-2 wird für hohe Datenraten von mindestens 10 Mbit/sec vorgeschlagen.
- MPEG-3 wurde für die HDTV-Komprimierung vorgeschlagen, wurde jedoch als überflüssig befunden und mit MPEG-2 zusammengeführt.
- MPEG-4 wird für sehr niedrige Datenraten von weniger als 64 Kbit/sec vorgeschlagen.


## Programmstream im MPG-Dateiformat ##

Der Programmstream ist ein Container zum Multiplexen von digitalem Audio, Video und mehr. Das Program Stream-Format ist im 1. Teil von MPEG-1 (ISO/IEC 11172-1) und im 1. Teil von MPEG-2, Systems (ISO/IEC-Standard 13818-1/ITU-T H.222.0) spezifiziert. Der MPEG-2-Programmstrom ist analogbasiert und ähnlich der ISO/IEC 11172-Systemschicht und aufwärtskompatibel.

### Kodierungsdetails ###

Hier sind die Codierungsdetails des partiellen MPEG-2 Program Stream Pack-Header-Formats:

| Name | Anzahl der Bits | Beschreibung |
---|---|---|
| Sync-Bytes | 32 | 0x000001BA |
| Markierungsbits | 2 | 01b für die MPEG-2-Version. Die Markierungsbits für die MPEG-1-Version sind 4 Bits mit dem Wert 0010b. |
| Systemuhr [32..30] | 3 | System Clock Reference (SCR) Bits 32 bis 30 |
| Markierungsbit | 1 | 1 Bit immer gesetzt. |
| Systemuhr [29..15] | 15 | Systemtaktbits 29 bis 15 |
| Markierungsbit | 1 | 1 Bit immer gesetzt. |
| Systemuhr [14..0] | 15 | Systemtaktbits 14 auf 0 |
| Markierungsbit | 1 | 1 Bit immer gesetzt. |
| SCR-Erweiterung | 9 | |
| Markierungsbit | 1 | 1 Bit immer gesetzt. |
| Bitrate | 22 | In Einheiten von 50 Byte pro Sekunde. |
| Markierungsbits | 2 | 11 Bits immer gesetzt. |
| reserviert | 5 | reserviert für zukünftige Verwendung |
| Fülllänge | 3 | |
| Füllbytes | 8 * Fülllänge | |
| Systemheader (optional) | 0 oder mehr | wenn der Startcode des Systemheaders folgt: 0x000001BB |

Die folgende Tabelle zeigt das partielle System-Header-Format:

| Name | Anzahl Bytes | Beschreibung |
---|---|---|
| Sync-Bytes | 4 | 0x000001BB |
| Kopfzeilenlänge | 2 | |
| ratengebundene und Markierungsbits | 3 | |
| Audio gebunden und Flags | 1 | |
| Flags, Markierungsbit und Videobindung | 1 | |
| Paketratenbeschränkung und reserviertes Byte | 1 | |


## Verweise ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



