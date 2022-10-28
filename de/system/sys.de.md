{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "Erweiterung", "Datei", "Format", "System", "Treiber", "Systemdatei", "Programme", "Computer", "Anwendung" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Systemdateiformat",
  "description":"Erfahren Sie mehr über das SYS-Dateiformat und APIs, die SYS-Dateien erstellen und öffnen können.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Was ist eine SYS-Datei? ##

Die SYS-Dateien sind "Systemdateien", die in Windows-Betriebssystemen und MS-DOS-Anwendungen verwendet werden. Diese Dateien können nicht direkt geöffnet werden und bestehen aus dem Treiber und der Konfiguration des Geräts. Die SYS-Dateien sind dafür verantwortlich, Dateien mit Kernfunktionen des Betriebssystems zu enthalten. Diese gelten als kritische Dateien des Gerätetreibers und können auch verwendet werden, wenn ein Problem des Rennfahrers gelöst werden soll. Diese sind für das ordnungsgemäße Funktionieren eines Computersystems verantwortlich, und die .sys-Dateien müssen korrekt und vollständig sein.


## Technische Spezifikation ##

Die .sys-Dateien sind eigentlich die Teilmenge des [BMP](/de/image/bmp)-Formats, da es nur bestimmte Kombinationen zulässt. Das übliche Format dieser Dateien ist wie LOGOS.SYS, LOGOW.SYS und LOGO.SYS. Alle anderen Dateien haben dieses Format nicht.

Diese Dateien werden zum Zeitpunkt der Installation hauptsächlich im *C*-Verzeichnis von Windows verwendet. Die meisten Probleme im Zusammenhang mit Gerätetreibern werden durch die Aktualisierung des Windows-Betriebssystems behoben. Die Details und Informationen dieser Dateien können mit den integrierten Programmen des Windows-Betriebssystems angezeigt werden. Dazu gehören auch die Verweise auf verschiedene Module in einem Betriebssystem.
Einige der Beispiele für Systemdateien sind:

* IO.SYS (Diese speichern Gerätetreiber des Festplattenbetriebssystems)
* MSDOS.SYS (Diese enthalten den Kernel oder den Kerncode des Betriebssystems)
* CONFIG.SYS (Diese enthalten verschiedene Konfigurationsoptionen)
* KEYBOARD.SYS (Diese enthalten Informationen zum Tastaturlayout)
* COUNTRY.SYS (Diese enthalten Länder- und Codepage-bezogene Informationen)

## SYS-Dateiformat ##

Microsoft hat die Dateien mit der Erweiterung .sys entwickelt. Variablen und Funktionen sind in SYS-Dateien enthalten. Diese werden hauptsächlich vom Microsoft-Betriebssystem verwendet. Diese Dateien befinden sich hauptsächlich im Stammverzeichnis der Festplatte:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Einige häufige Warnungen zu SYS-Dateien lauten wie folgt:

* Die Namen dieser Dateien sollten nicht geändert werden, da diese Dateien für Kernfunktionen und Variablen des Betriebssystems verantwortlich sind
* Diese Dateien sollten nicht gelöscht werden, da das Fehlen dieser Dateien Fehler verursachen kann
* Die .sys-Dateien sollten nicht aus dem Internet heruntergeladen werden, bis Sie sich über die Legitimität der Quelle sicher sind
* Man sollte nicht mit diesen Dateien herumspielen, da das Verändern oder Herumspielen mit ihnen schwerwiegende Systemfehler verursacht
* Wenn diese Dateien durch Viren oder Malware beschädigt werden, sollten sie neu installiert werden

## SYS-Beispiel ##

Das Folgende ist ein Beispiel für eine einfache SYS-Systemkonfigurationsdatei:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
