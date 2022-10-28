{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC-Dateiformat - Was ist eine LRC-Datei?",
  "description":"Erfahren Sie mehr über die LRC Lyric-Datei und APIs, die LRC-Dateien erstellen und öffnen können.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Was ist eine LRC-Datei?

Eine LRC-Datei ist eine textbasierte Textdatei, die den Text eines Audio-Songs enthält. Wenn der Audiosong mit einem Musikplayer oder einer Audioplayer-Software auf einem Computer abgespielt wird, wird die LRC-Datei parallel gelesen und mit Zeit angezeigt. LRC-Dateien enthalten Cue-Punkte zum Anzeigen von Texten, wenn der Song abgespielt wird. Im Allgemeinen haben die LRC-Dateien denselben Namen wie die entsprechende Audiodatei, z. B. audio.mp3 und audio.lrc. LRC-Dateien ähneln Untertiteldateien wie [SRT](/de/video/srt/).

## LRC-Dateiformat - Weitere Informationen

Dateien im LRC-Textformat werden als einfache Textdateien gespeichert und können in einer Textdatei geöffnet und bearbeitet werden. Der Inhalt einer LRC-Datei enthält Farbinformationen für die Anzeige des Liedtextes.

## LRC-Formate

Es gibt mehrere Formate von LRC-Dateien, die im Laufe der Zeit entwickelt wurden. Diese

### Einfaches LRC-Format

Die Zeilenzeit-Tags haben das Format [mm:ss.xx], wobei mm für Minuten, ss für Sekunden und xx für Hundertstelsekunden steht.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Einfaches Format erweitert

Es beinhaltet die Möglichkeit, das Geschlecht des Textes zu ändern und anzugeben, indem M: Männlich, F: Weiblich, D: Duett verwendet wird.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Erweitertes LRC-Format

Das erweiterte LRC-Format ist eine erweiterte Version des einfachen LRC-Formats. Es fügt dem Format ein Word Time Tag hinzu<mm:ss.xx> am Ende des vorherigen Wortes.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Verweise

* [LRC Songtext-Dateiformat – Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

