{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "file", "extension", "format", "audio interchange file format", "music", "aiff file format", "aiff to mp3", "aiff vs wav", "convert aiff to mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das AIFF-Dateiformat und APIs, die AIFF-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"AIFF - Audio Interchange File Format",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Was ist eine AIFF-Datei?
Das AIFF (Audio Interchange File Format) ist ein unkomprimiertes Audiodateiformat, das 1998 von Apple entwickelt wurde, aber auf **EA IFF 85** (Standard for Interchange Format Files, entwickelt von Electronic Arts) basiert, einem Wrapper-Format, das auf Amiga-Systemen verwendet wird . Dieses Dateiformat bietet einen Standard zum Speichern von gesampelten Sounds. Das Format ist ausreichend flexibel und ermöglicht die Speicherung von Mono- oder Mehrkanal-Sample-Sounds mit verschiedenen Sample-Raten und Sample-Breiten. Da die AIFF-Dateien unkomprimiert sind, werden sie dadurch größer als andere verlustbehaftete Formate wie [MP3](/audio/mp3/). Diese Dateien bestehen aus 2 Kanälen mit unkomprimiertem Stereo-Audio mit 16-Bit-Samplegröße, aufgenommen mit 44,1 kHz. Aufgrund der hohen Audioqualität kann ein 5-minütiges Audio bis zu 50 MB Speicherplatz beanspruchen, was dem Dateiformat [WAV](/audio/wav/) ähnelt.

## AIFF gegen WAV
AIFF und WAV sind qualitativ fast gleich. Beide verwenden die gleiche PCM-Codierung (Pulse-Code-Modulation), wodurch sie im Vergleich zu anderen verlustbehafteten Formaten wie [MP3](/audio/mp3/) größer werden. [M4A](/audio/m4a/). Einige der allgemeinen Unterschiede sind in der folgenden Tabelle aufgeführt:

|AIFF|WAV|
---|---|
|Wird hauptsächlich für MAC verwendet|Wird hauptsächlich für PCs verwendet|
|Erlaubt Metadeta| Erlaubt keine Metadeta|

## Dateistruktur
Das **EA IFF 85** legt eine allgemeine Struktur zum Speichern von Daten in Dateien fest. Eine **EA IFF 85**-Datei besteht aus mehreren Datenblöcken. Ein Chunk ist ein Gebäudeblock einer AIFF-Datei, der aus einigen Header-Informationen gefolgt von Daten besteht:
{{< figure src="../chunk.png" alt="AIFF-Stück" >}}

Eine AIFF-Datei ist eine Sammlung verschiedener Chunk-Typen. Es gibt zwei allgemeine Arten von Chunks, die wichtig sind, um einen AIFF-Datei-Chunk zu bilden:
- **Common Chunk**: Enthält wichtige Parameter, die den gesampelten Sound beschreiben, wie Länge und Samplerate.
- **Sound Data Chunk**: Enthält die eigentlichen Audio-Samples.
Es gibt viele andere optionale Chunks, die Instrumentenparameter auflisten, Marker definieren, anwendungsspezifische Informationen speichern usw.
 

### Lokale Chunk-Typen

Die Chunk-Typen zum Bilden von AIFF sind in der folgenden Tabelle angegeben:

|Chunk-Typ| Beschreibung|
---|---|
|Common Chunk|Der Common Chunk beschreibt grundlegende Parameter des gesampelten Sounds|
|Sound Data Chunk|Der Sound Data Chunk enthält die eigentlichen Sample-Frames|
|Marker Chunk|Der Marker Chunk enthält Marker, die auf Positionen in den Sounddaten zeigen|
|Instrument Chunk|Der Instrument Chunk definiert grundlegende Parameter, die ein Instrument, z. B. ein Sampler, verwenden könnte, um die Klangdaten wiederzugeben|
|MIDI Data Chunk|Der MIDI Data Chunk kann zum Speichern von MIDI-Daten verwendet werden|
|Audio Recording Chunk|Der Audio Recording Chunk enthält relevante Informationen zu Audioaufnahmegeräten|
|Anwendungsspezifischer Chunk|Der anwendungsspezifische Chunk kann von Herstellern von Anwendungen für beliebige Zwecke verwendet werden|
|Comments Chunk|Der Comment Chunk dient zum Speichern von Kommentaren im FORM AIFF|
|Textblöcke - Name, Autor, Copyright, Anmerkung| Alle sind Textstücke|

## Verweise ##

* [Audio Interchange File Format – Von Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

