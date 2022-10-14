{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "Erweiterung", "Datei", "Format", "System", "Initiierung", "Verzeichniserweiterung", "Programme", "Computer", "Anwendung" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Initialisierungsdateiformat",
  "description":"Erfahren Sie mehr über das INI-Dateiformat und APIs, die INI-Dateien erstellen und öffnen können.",
  "linktitle" :"INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Was ist eine INI-Datei? ##

Eine INI-Datei ist ein Nachrichtenkonfigurationsdokument für Computerprogramme, die öffentliche Schlüssel für Merkmale und Abschnitte enthalten, die die Attribute in einem Rahmenwerk und einer Grammatik organisieren. Diese Konfigurationsdokumente für das Systemdateiformat erhalten ihren Namen von der Verzeichniserweiterung INI des MS-DOS-Betriebssystems, die für Initiierung steht. Es hat diese Form des Software-Setups populär gemacht. Viele Programme in anderen Softwareanwendungen verwenden verschiedene Dateinamenzusätze, wie CONF und [CFG](/de/system/cfg), obwohl das Format in vielen Konfigurationssituationen einen inoffiziellen Standard etabliert hat.

## Kurze Geschichte der INI-Dateien##

Anfänglich war die Hauptprogrammkonfigurationstechnik von Windows ein Textdateiformat, das aus Textzeilen mit einem entscheidenden Paar pro Zeile bestand, die in Abschnitte unterteilt waren. Gerätetreiber, Schriftarten und Startprogramme wurden alle in diesem Format gespeichert. Individuelle Einstellungen wurden auch häufig von Apps in INI-Dateien gespeichert.
Bis Windows 3.1x wurde das Format auf 16-Bit-Microsoft Windows-Plattformen unterstützt. Beginnend mit Windows 95 begann Microsoft, Entwickler zu ermutigen, die Windows-Registrierung anstelle von INI-Dateien für die Konfiguration zu verwenden.

## INI-Datei - Dateiformatspezifikationen

### Schlüssel/Eigenschaften ###

Der Schlüssel/die Eigenschaft ist das grundlegendste Element einer INI-Datei. Ein Gleichheitszeichen (=) trennt den Namen und den Wert jedes Schlüssels. Links vom Gleichheitszeichen wird der Name angezeigt. Das Gleichheitszeichen und das Semikolon sind diskrete Buchstaben im Windows-System und können daher nicht im Schlüssel verwendet werden. Im Wert können beliebige Zeichen verwendet werden.

```
name=value
```

### Abschnitte ###

Der Abschnittskommentar steht in eckigen Klammern ([]) in einer eigenen Zeile. Nach der Abschnittsdefinition sind alle Schlüssel mit diesem Abschnitt verknüpft. Abschnitte enden mit der nächsten Abschnittsbezeichnung oder dem Ende des Dokuments; Es gibt kein spezielles Trennzeichen für das „Ende des Abschnitts“. Abschnitte können nicht gestapelt werden; sie können nur einmal benannt werden und müssen nicht verknüpft werden.

```
[section]
a=a
b=b
```

### Funktionen ändern ###

Das INI-Dateiformat hat keine global akzeptierte Definition. Viele Computeranwendungen umfassen Funktionen zusätzlich zu den bereits erwähnten. Die folgende Liste enthält einige gemeinsame Merkmale, die in jedem einzelnen Programm enthalten sein können oder nicht.

* Kommentare
* Escapezeichen
* Doppelte Namen


## INI-Beispiel ##

Die Beispiel-INI-Datei sieht wie folgt aus:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Bezug ##

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

