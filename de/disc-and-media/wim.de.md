{
  "date" : "2021-08-11",
  "keywords" :[ "WIM-Datei", "WIM-Dateiformat", "Was ist eine WIM-Datei", "Datei", "WIM-Beispiel", "WIM-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das WIM-Dateiformat und APIs, die WIM-Dateien erstellen und öffnen können.",
  "title" :"WIM - Windows-Imaging-Formatdatei",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Was ist eine WIM-Datei?
Die Dateien mit der Erweiterung .wim wurden zum ersten Mal in Windows Vista gesehen. Das WIM gehört zu einem dateibasierten Imaging-Format, das typischerweise in Microsoft Windows Vista eingeführt wurde. Es ermöglicht die Bereitstellung eines einzelnen Disk-Images auf verschiedenen Computerplattformen. WIM-Dateien werden verwendet, um Dateien wie Updates, Treiber und Komponenten zu verwalten, ohne das Betriebssystem-Image neu zu starten. Eine Q-WIM-Datei enthält eine Reihe von Dateien und zugehörigen Metadaten, die anderen Festplattendateiformaten sehr ähnlich sind.

## WIM-Dateiformate
Das WIM-Dateiformat ist nicht wie sektorbasierte Formate wie VHD oder IS, tatsächlich ist es dateibasiert, was bedeutet, dass die grundlegende Informationseinheit in einem WIM eine Datei ist. Der grundlegende Vorteil der Dateibasis besteht darin, dass eine Datei in einer einzelnen Instanz gespeichert wird, auf die im Dateisystembaum mehrfach verwiesen wird, und Hardwareunabhängigkeit. Dadurch wird der Aufwand für das Öffnen und Schließen verschiedener Dateien einzeln reduziert, da die Dateien in einem einzigen WIM gespeichert werden Datei. WIM-Dateien können mehrere Disk-Images speichern, auf die entweder durch ihren eindeutigen Namen oder durch ihren numerischen Index verwiesen wird.
### Unterstützung für Komprimierungsalgorithmen
WIM unterstützt die folgenden Familien von Komprimierungsalgorithmen in absteigender Geschwindigkeit und aufsteigendem Verhältnis:
-XPRESS
-LZX
-LZMS
- Feste Kompression.
Die ersten drei Familien basieren auf LZ77, während die Solid-Komprimierung zusammen mit LZMS in WIMGAPI Windows 8 und DISM Windows 8.1 eingeführt wurde.
### Tools für das WIM-Dateiformat
Die folgenden Tools unterstützen normalerweise das WIM-Dateiformat:

- **ImageX**: Ein Befehlszeilentool zum Bearbeiten, Erstellen und Bereitstellen von Windows-Festplattenabbildern im Windows-Imaging-Format. Zusammen mit der relevanten WIMGAPI wird es als Teil des kostenlosen Windows Automated Installation Kit verteilt. Ab Windows Vista verwendet Windows Setup die WAIK-API, um Windows zu installieren.
- **DISM**: Ein in Windows 7 und Windows Server 2008 R2 eingeführtes Tool, das dienstbezogene Aufgaben auf einem Windows-Installationsabbild ausführen kann, sei es ein Online-Abbild oder ein Offline-Abbild in einem Ordner oder einer WIM-Datei. Dieses Tool war in der Lage, Images zu mounten und zu unmounten, einem Offline-Image einen Gerätetreiber hinzuzufügen und installierte Gerätetreiber in einem Offline-Image abzufragen.
 




## Verweise


* [Windows Imaging Format – von Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


