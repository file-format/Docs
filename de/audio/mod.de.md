{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "file", "extension", "format", "was ist ein Mod-Dateiformat", "Musik", "mod-Dateiformat", "mod vs. MP3", "Mod-Dateiformatspezifikation "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das MOD-Dateiformat und APIs, die MOD-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"MOD - Musikmoduldatei",
  "linktitle" :"MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Was ist eine MOD-Datei?
Eine Datei mit der Erweiterung .mod ist eine Musikmoduldatei, die unter Verwendung des Standard-Musikmodulformats erstellt wurde, das auf dem **Amiga-Modulformat** basiert, das von Karsten Obarski entwickelt und mit der **Ultimate Soundtracker**-Software für den Commodore veröffentlicht wurde Amiga-System. Ähnlich wie eine [MIDI](/de/audio/mid/)-Datei besteht sie aus Notenmustern und Klangbeispielen, die verschiedene Instrumente darstellen, die entsprechend den Noten wiedergegeben werden. MOD-Dateien werden insbesondere in Videospielen als Hintergrundmusik und in der **Demosszene**-Subkultur der Computerkunst verwendet.
## MOD-Dateiformat
Das MOD ist ein Computerdateiformat, dessen grundlegende Funktion darin besteht, Musik darzustellen, und es war das erste Moduldateiformat. MOD-Dateien verwenden die Dateierweiterung .mod, außer auf dem **Amiga**, der den Header einer Datei liest, um den Dateityp zu bestimmen, also nicht auf Dateinamenerweiterungen angewiesen ist. Eine MOD-Datei besteht aus einer Reihe verschiedener Instrumente in Form von Samples, einer Reihe von Patterns, die angeben, wie und wann die Samples gespielt werden sollen, und einer Liste, welche Patterns in welcher Reihenfolge gespielt werden sollen.
### Spezifikation
Ein MOD-Dateimuster ist eigentlich in einer Sequenzer-Benutzeroberfläche als Tabelle mit einer Spalte pro Kanal entworfen, also hat diese Tabelle vier Spalten (eine für jeden Amiga-Hardware-Kanal. Jede Spalte hat 64 Zeilen).

Eine Zelle in der Tabelle kann eine der folgenden Aktionen auf dem Kanal ihrer Spalte auslösen, wenn die Zeit ihrer Zeile erreicht ist:

- Starten Sie ein Instrument, das in diesem Kanal eine neue Note mit einer bestimmten Lautstärke spielt, möglicherweise mit einem darauf angewendeten Spezialeffekt
- Ändern Sie die Lautstärke oder den Spezialeffekt, der auf die aktuelle Note angewendet wird
- Musterfluss ändern; zu einer bestimmten Song- oder Pattern-Position springen oder innerhalb eines Patterns loopen
- Nichts tun; jede vorhandene Note, die in diesem Kanal gespielt wird, wird weiterhin gespielt

Ein Instrument ist ein einzelnes Sample zusammen mit einer optionalen Spezifikation, welcher Teil des Samples wiederholt werden kann, um eine solide Note zu halten.
### Zeitliche Koordinierung
Der minimale Zeitrahmen betrug in der ursprünglichen MOD-Datei 0,02 Sekunden oder ein „vertikales Austastintervall“ (VSync), da die ursprüngliche Software das VSync-Timing des Monitors verwendete, der mit 50 Hz (für PAL) oder 60 Hz (für NTSC) lief. für Zeitmessung.

## Verweise

* [MOD (Dateiformat) - Von Wikipedia](https://en.wikipedia.org/wiki/MOD_(Dateiformat))


