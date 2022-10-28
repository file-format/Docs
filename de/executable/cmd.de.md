{
  "date" : "2021-07-12",
  "keywords" :[ "cmd-Datei", "was ist eine cmd-Datei", "Datei", "cmd-Beispiel", "cmd-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das CMD-Dateiformat und APIs, die CMD-Dateien erstellen und öffnen können.",
  "title" :"CMD - Windows-Befehlsdateiformat",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Was ist eine CMD-Datei?
Eine CMD-Datei besteht aus einem Skript, das einen oder mehrere Befehle in Form von Klartext enthält, die ausgeführt werden, um verschiedene Aufgaben auszuführen. Sie ähnelt einer [BAT](/de/executable/bat/)-Datei, die im Allgemeinen auch zum Speichern einer Reihe ausführbarer Befehle verwendet wird. Die CMD-Dateien werden häufig im Microsoft Windows-Betriebssystem verwendet. Diese Dateien wurden fast in den 90er Jahren eingeführt, aber immer noch im neuesten Windows-Betriebssystem verwendet. Diese Dateien werden im Allgemeinen geschrieben, um mehr als einen Befehl in einer Sequenz auszuführen.

## CMD-Dateiformat
CMD ist ein Dateiformat, das von ausführbaren Programmen im CP/M-Stil verwendet wird. Es ist im Allgemeinen vergleichbar mit [COM](/de/executable/com/) in CP/M-80 und [EXE](/de/executable/exe/) in DOS. Eine CMD-Datei enthält 1 bis 8 Code- oder Datengruppen und einen 128-Byte-Header. Jede Gruppe kann bis zu 1 MB groß sein. CMD-Dateien können in späteren Versionen auch Umzugsinformationen und Resident System Extensions (RSXs) enthalten. Die CMD ist ein Neuling im Vergleich zur [BAT](/de/executable/bat/)-Datei; verwendet für MS-DOS vor der Veröffentlichung von Windows In MS-DOS. Obwohl Sie auch heute noch Dateien mit der Erweiterung .bat speichern können, verwenden viele Benutzer die Erweiterung .cmd, um ihre ausführbaren Skripts zu speichern.

### CMD-Formatspezifikation

Der Anfang des Headers enthält die Liste der in der Datei vorhandenen Gruppen zusammen mit ihren Typen. Jeder Typ kann höchstens einmal verwendet werden. Diese Typen sind:

- Code
- Daten
- Extra
- Stapel
- Benutzer 1
- Benutzer 2
- Benutzer 3
- Benutzer 4
- Gemeinsamer Code

Ebenso sind beim Programmsegmentpräfix in DOS die ersten 256 Bytes der Datengruppe Null. Sie werden von CP/M-86 mit der Nullseite gefüllt. Wenn keine Datengruppe vorhanden ist, werden stattdessen die ersten 256 Bytes der Codegruppe verwendet.
## Beispiel einer CMD-Datei
Im Folgenden finden Sie ein Beispiel für ein CMD-Skript zum Anzeigen von Systeminformationen.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Verweise

* [So schreiben Sie ein CMD-Skript] (https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD-Datei (CP/M) - von Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

