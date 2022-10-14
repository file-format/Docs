{
  "date" : "2021-06-09",
  "keywords" :[ "Cue", "Datei", "Erweiterung", "Format", "Was ist eine Cue-Datei", "Musik", "Cue-Dateiformat", "Cue-Dateiformatspezifikation", "Cue-Sheet", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das CUE-Dateiformat und APIs, die CUE-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"CUE - Cue-Sheet-Datei",
  "linktitle" :"CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Was ist eine CUE-Datei?

Eine Datei mit der Erweiterung .cue, auch Cue-Sheet-Datei genannt, ist eine Metadatendatei, die Informationen über das Layout von Tracks auf einer CD oder DVD enthält. Diese werden von Mediaplayern und Authoring-Anwendungen für optische Discs unterstützt. Die auf der CD gespeicherten Hauptaudiodaten werden von der Cue-Datei referenziert, zusammen mit den Spezifikationen von Titellängen, Disc-Titeln und Interpreten. Wenn also eine einzelne Audiodatei mehrere Tracks enthält, kann die Cue-Datei verwendet werden, um das Audio in mehrere Dateien aufzuteilen oder auf verschiedene Tracks zu verweisen.

## CUE-Dateiformat

CUE- oder Cue-Sheet-Dateien werden im Klartextformat gespeichert, das für Menschen lesbar ist. Informationen in einer Cue-Datei sind Befehle mit einem oder mehreren Parametern. Diese Befehle gelten je nach Befehl und Kontext entweder für die gesamte Datei oder für eine einzelne Spur. Das CDRWIN-Benutzerhandbuch beschreibt die Spezifikationen für die Cue-Sheet-Syntax und -Semantik.

## Wichtige CUE-Sheet-Befehle

|Befehl|Beschreibung|
---|---|
|DATEI| Bezieht sich auf die Datei, die die Daten und ihr Format enthält, wie z. B. [MP3](/de/audio/mp3/), [WAV](/de/audio/wav/) oder einfaches binäres Disc-Image)|
|SPUR| Definiert die Spurkontextinformationen wie Nummer und Typ oder Modus.|
|INDEX| Repräsentiert die Position als Index innerhalb der DATEI. Das Format ist mm:ss:ff (Minuten-Sekunden-Frame).|
|PREGAP und POSTGAP|Dies zeigt den Pregap oder Postgap eines Tracks an, der in keiner Datendatei gespeichert ist. Die Länge wird im gleichen Minuten-Sekunden-Frame-Format wie bei INDEX.| angegeben

### CUE-Sheet-Beispiel

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Verweise

* [.cda-Datei – von Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

