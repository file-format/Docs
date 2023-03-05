{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "Datei", "Erweiterung", "Format", "Audio-Austausch-Dateiformat", "Musik" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das WAV-Dateiformat und APIs, die WAV-Dateien erstellen und öffnen können.",
  "title" :"WAV - Wellenform-Audiodateiformat",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Was ist eine WAV-Datei?

WAV, bekannt für WAVE (Waveform Audio File Format), ist eine Teilmenge der Resource Interchange File Format (RIFF)-Spezifikation von Microsoft zum Speichern digitaler Audiodateien. Das Format wendet keine Komprimierung auf den Bitstream an und speichert die Audioaufnahmen mit unterschiedlichen Abtastraten und Bitraten. Es war und ist eines der Standardformate für Audio-CDs. Wave-Dateien sind größer im Vergleich zu neuen Audiodateiformaten wie [MP3](/de/audio/mp3/), die eine verlustbehaftete Komprimierung verwenden, um die Dateigröße zu reduzieren, während die gleiche Audioqualität beibehalten wird. WAV-Dateien können jedoch mit Audio Compression Manager (ACM)-Codecs komprimiert werden. Es sind mehrere APIs und Anwendungen verfügbar, die WAV-Dateien in andere gängige Audiodateiformate konvertieren können.

**Hast Du gewusst?**
Sie können ein Mitwirkender bei FileFormat.com werden, um die Dateiformat-Community mit Ihren Erkenntnissen auf dem Laufenden zu halten. Wenn Sie etwas über WAV- oder Audiodateiformate mitteilen möchten, können Sie Ihre Ergebnisse im Abschnitt [Neuigkeiten zu Audiodateiformaten](https://news.fileformat.com/t/audio) veröffentlichen, damit die Leute auf dem Laufenden bleiben.

## WAV-Dateiformat ##

Das WAVE-Dateiformat, das eine Teilmenge der RIFF-Spezifikation von Microsoft ist, beginnt mit einem Dateiheader, gefolgt von einer Folge von Datenblöcken. Eine WAVE-Datei hat einen einzelnen „WAVE“-Block, der aus zwei Unterblöcken besteht:

* ein "fmt"-Stück - gibt das Datenformat an
* ein "Daten"-Chunk - enthält die eigentlichen Beispieldaten

### Kopfzeile der WAV-Datei ###

Der Header einer WAV (RIFF)-Datei ist 44 Bytes lang und hat folgendes Format:


|Positionen|Beispielwert|Beschreibung
---|---|---|
|1 - 4|"RIFF"|Markiert die Datei als Riff-Datei. Zeichen sind jeweils 1 Byte lang.
|5 - 8|Dateigröße (Ganzzahl)|Größe der gesamten Datei - 8 Byte, in Byte (32-Bit-Ganzzahl). Normalerweise würden Sie dies nach der Erstellung ausfüllen.
|9 -12|"WAVE"|Dateityp-Header. Für unsere Zwecke ist es immer gleich "WAVE".
|13-16|"fmt "|Chunk-Marker formatieren. Enthält nachgestellte Null
|17-20|16|Länge der Formatdaten wie oben aufgeführt
|21-22|1|Formattyp (1 ist PCM) – 2-Byte-Ganzzahl
|23-24|2|Anzahl der Kanäle – 2-Byte-Ganzzahl
|25-28|44100|Abtastrate - 32-Byte-Ganzzahl. Gängige Werte sind 44100 (CD), 48000 (DAT). Abtastrate = Anzahl der Abtastungen pro Sekunde oder Hertz.
|29-32|176400|(Abtastrate * BitsPerSample * Kanäle) / 8.
|33-34|4|(BitsPerSample * Kanäle) / 8.1 - 8-Bit-Mono2 - 8-Bit-Stereo/16-Bit-Mono4 - 16-Bit-Stereo
|35-36|16|Bits pro Abtastung
|37-40|"data"|"data" Chunk-Header. Markiert den Beginn des Datenabschnitts.
|41-44|Dateigröße (Daten)|Größe des Datenbereichs.
|Beispielwerte sind oben für eine 16-Bit-Stereoquelle angegeben.

## Verweise ##

* [WAV – von Wikipedia](https://en.wikipedia.org/wiki/WAV)

