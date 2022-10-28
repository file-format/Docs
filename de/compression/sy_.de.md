{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_-Dateiformat - Komprimierte SYS-Datei",
  "description":"Erfahren Sie mehr über das SY_-Dateiformat und APIs, die SY_-Dateien erstellen und öffnen können.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Was ist eine SY_-Datei?

Eine SY_-Datei ist eine komprimierte .sys-Datei, die von Softwareinstallationsprogrammen verwendet wird, um die Größe der Installationsdateien zu reduzieren, die im Installationsprogramm verpackt sind. Dies reduziert die Gesamtgröße des Installers. SY_-Dateien können mit dem Microsoft Expand-Befehlszeilendienstprogramm erweitert werden, das eine oder mehrere komprimierte Dateien erweitert.

## SY_-Dateiformat - Weitere Informationen

SY_-Dateien werden als komprimierte Binärdateien auf der Disc gespeichert. Ihr internes Dateiformat ist jedoch nicht öffentlich verfügbar. Das Befehlszeilendienstprogramm Microsoft Expand kann SY_-Dateien mithilfe einer der folgenden Befehlszeilen erweitern.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Beim Erweitern werden die SY_-Dateien in die Datei [SYS](https://docs.fileformat.com/system/sys/) konvertiert.

SY_-Dateien ähneln EX_- und DL_-Dateien.

## Verweise

* [StuffIt – Von Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

