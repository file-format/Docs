{
  "date" : "2021-08-13",
  "keywords" :[ "sdi-Datei", "sdi-Dateiformat", "was ist eine sdi-Datei", "Datei", "sdi-Beispiel", "sdi-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das SDI-Dateiformat und APIs, die SDI-Dateien erstellen und öffnen können.",
  "title" :"SDI - Windows-Systembereitstellungs-Image-Datei",
  "linktitle" :"SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Was ist eine SDI-Datei?
Die Datei mit der Erweiterung .sdi enthält einen Lade-Blob, einen Boot-Blob und einen Teil-Blob; Wird häufig von Windows Embedded Studio verwendet, um RAM-Disketten oder Boot-Disketten zum Laden und Installieren von Windows zu erstellen. Das SDI wird für System Deployment Image abgekürzt. Das Windows Embedded Studio ist ein Programm zum Erstellen von Disk-Images für Windows. Tatsächlich enthält dieses Programm das SDI File Manager-Programm und ein Befehlszeilentool namens **sdimgr.exe**, die beide zum Bereitstellen, Erstellen und Bearbeiten von SDI-Images verwendet werden können.

## SDI-Dateiformat
Das SDI-Dateiformat wird häufig verwendet, um die Verwendung einer virtuellen Festplatte zum Booten eines Systems zu ermöglichen. Einige Versionen von Microsoft Windows ermöglichen **RAM-Booten**, was wichtig ist, um eine SDI-Datei in den Speicher zu laden und dann von dort zu booten. Das SDI-Dateiformat aktiviert sich auch für das Booten über das Netzwerk, indem es PXE (Preboot Execution Environment) verwendet. Es wird auch für Festplatten-Imaging verwendet.
### SDI-Dateiabschnitte
Die SDI-Datei selbst kann in die folgenden Abschnitte unterteilt werden:
- **Boot BLOB**: Enthält das eigentliche Bootprogramm, STARTROM.COM. Dies ist eine Analogie zum Bootsektor einer Festplatte.
- **Load BLOB**: Dies enthält normalerweise NTLDR und wird vom Boot-BLOB gestartet.
- **Part BLOB**: Enthält die eigentliche Boot-Laufzeit; enthält auch die Dateien boot.ini und ntdetect.com, die sich im Stammverzeichnis der Laufzeitumgebung befinden sollten.
- **Festplatten-BLOB**: Dies ist ein flaches HDD-Image, das mit einem MBR beginnt. Es wird für das Festplatten-Imaging anstelle des Bootens verwendet. Außerdem können nur Festplatten-BLOBs mit den Dienstprogrammen von Microsoft gemountet werden.


## Verweise

* [Systembereitstellungsbild – von Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


