{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ-Dateiformat - Fritzing-Teiledatei",
  "description":"Erfahren Sie, was eine FZPZ-Datei und APIs sind, die FZPZ-Dateien erstellen und öffnen können.",
  "linktitle" :"FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Was ist eine FZPZ-Datei?

Eine FZPZ-Datei ist eine Komponente/ein Teil, das in einem elektronischen Schaltungsdesign verwendet wird, das mit der Schaltkreis-Prototyping- und Designanwendung **Fritzing** erstellt wurde. Es ist ein komprimiertes Archiv, das eine [FZP](/de/cad/fzp/)-Datei und vier [SVG](/de/image/svg/)-Bilder enthält, die den gesamten Teil in Fritzing beschreiben. Der Vorteil der Verwendung dieser Dateien besteht darin, dass Benutzer ihre FZPZ-Dateien aus Sicht der Wiederverwendbarkeit mit jedem teilen können. Die gemeinsame Nutzung von FZPZ-Teilen hilft bei der Integration von Schaltungsteilen, um schnell größere PCB-Designs zu erstellen.

## FZPZ-Dateiformat - Weitere Informationen

FZPZ-Dateien werden als komprimierte [ZIP](/de/compression/zip/)-Archive auf der Disc gespeichert. Sie können die Erweiterung von .fzpz in .zip umbenennen und jedes standardmäßige Dekomprimierungsprogramm wie WinZIP verwenden, um die Dateien aus dem Archiv zu extrahieren.

### Informationen zur FZPZ-Dateistruktur

Wie bereits erwähnt, ist eine FZPZ-Datei eine Archivdatei, die mehrere Dateien zur Darstellung eines auf einer Leiterplatte verwendeten Teils enthält. Das FZPZ enthält folgende Dateien:

* `Vier SVG-Dateien` - die Steckbrett-, Schaltplan-, PCB- und Symbolbilder des Teils darstellen
* „FZP-Datei“ – Eine XML-Datei, die Informationen über die Eigenschaften, Anschlüsse und Busse des Teils enthält

Die Dateien werden normalerweise wie folgt benannt.

* Teil.Datei.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematische.datei.svg

## Verweise ##

* [Neuteile mit fzpz-Erweiterung](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

