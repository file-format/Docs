{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "mp2-Datei", "Erweiterung", "Format", "was ist eine mp2-Datei", "Musik", "mp2-Dateiformat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das MP2-Dateiformat und APIs, die MP2-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"MP2 - MPEG Layer 2 Audiodateiformat",
  "linktitle" :"MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Was ist eine MP2-Datei?
Eine MP2-Datei, die auch als MPA-Datei bezeichnet wird, ist eine mit Layer II von MPEG-1 oder MPEG-2 komprimierte Audiodatei; ein verlustbehaftetes Audiokomprimierungsformat, das von ISO/IEC 11172-3 zusammen mit MPEG-1 Audio Layer I und MPEG-1 Audio Layer III ([MP3](/de/audio/mp3/)) definiert wird, um die Audiodateigröße zu reduzieren. Dagegen ist MP3 aufgrund seiner geringeren Größe und Verfügbarkeit über das Internet beliebter als MP2. Daher ist MP2 immer noch ein wichtiger Standard für die Audioübertragung.

## MP2-Dateiformat
MPEG Audio Layer II (MP2) ist der Kernalgorithmus der MP3-Standards. Die MPEG-1-Audio-Layer-2-Codierung wurde vom MUSICAM-Audio-Codec erhalten. Es begann als Digital Audio Broadcast (DAB)-Projekt in Deutschland als Teil des EUREKA-Forschungsprogramms. Die Eureka 147 enthielt drei Hauptelemente: Transmission Coding & Multiplexing, COFDM Modulation und MUSICAM Audio Coding (Masking Pattern Universal Sub-Band Integrated Coding And Multiplexing). Die MUSICAM war eine der wenigen Kodierungen, die eine hohe Audioqualität bei Bitraten im Bereich von 64 bis 192 kbit/s pro Monokanal erreichen konnte. Ziel war es, geringe Verzögerung, geringe Komplexität, Fehlerrobustheit, kurze Zugriffseinheiten bereitzustellen und die technischen Anforderungen von Rundfunk, Telekommunikation und Aufzeichnung auf digitalen Speichermedien zu erfüllen.

MP2 ist ein Subband-Audiocodierer, der im Zeitbereich mit einer Filterbank mit geringer Verzögerung komprimiert werden kann, die 32 Frequenzbereichskomponenten erzeugt. Im Vergleich dazu ist MP3 ein Transformations-Audio-Encoder mit hybrider Filterbank, was bedeutet, dass die Kompression im Frequenzbereich nach einer hybriden Transformation aus dem Zeitbereich angewendet wird. Der MP2-Codierer kann Redundanzen zwischen Kanälen ausnutzen, indem er eine optionale "gemeinsame Stereo"-Intensitätscodierung verwendet.

### Spezifikation des MP2-Dateiformats
Das MP2-Dateiformat basiert auf aufeinanderfolgenden digitalen Frames mit 1152 Abtastintervallen mit vier möglichen Formaten:

- Monoformat
- Stereoformat
- intensitätscodiertes gemeinsames Stereoformat (Stereoirrelevanz)
- Zweikanalformat (unkorreliert).
Einige wichtige technische Spezifikationen von MP2 sind in der folgenden Tabelle aufgeführt:

|Spezifikation| Beschreibung|
---|---|
|**Abtastraten**| 32, 44,1 und 48 kHz|
|**Bitraten**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 und 384 kbit/s|
|**Zusätzliche Abtastraten**|16, 22,05 und 24 kHz|
|**Weitere Bitraten**|8, 16, 24, 40 und 144 kbit/s|
|**Mehrkanalunterstützung**|Bis zu 5 Vollbereichs-Audiokanäle und ein LFE-Kanal (Low Frequency Enhancement Channel)|




## Verweise ##

* [MPEG-1 Audio Layer II – Von Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


