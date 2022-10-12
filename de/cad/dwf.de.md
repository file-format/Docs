{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Dateiformat", "Öffnen", "Lesen", "Erstellen", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DWF-Dateiformat und APIs, die DWF-Dateien erstellen und öffnen können.",
  "title" :"DWF-Dateiformat",
  "linktitle" :"DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DWF-Datei?

Design Web Format (DWF) stellt 2D/3D-Zeichnungen in komprimiertem Format zum Anzeigen, Überprüfen oder Drucken von Designdateien dar. Es enthält Grafiken und Text als Teil der Designdaten und reduziert die Dateigröße aufgrund seines komprimierten Formats. Die reduzierte Dateigröße macht die Verteilung und Kommunikation umfangreicher Konstruktionsdaten effizient. DWF erfordert nicht, dass der Empfänger etwas über die Verwendung der CAD-Software weiß, mit der die Originalzeichnung erstellt wurde. Der Inhalt des DWF-Dateiformats kann einfach sein und nur ein einzelnes Blatt umfassen oder komplex genug sein, um Schriftarten, Farben und Bilder zu enthalten.

## Kurze Geschichte ##

Autodesk führte das DWF-Dateiformat 1995 als Teil des Netscape-Navigations-Plugins WHIP ein. Das Format entwickelte sich im Laufe der Zeit vom reinen 2D-Format hin zu 3D-Inhalten. Viele Anwendungen von Drittanbietern verwenden dieses Format ebenfalls.

## DWF-Dateiformat ##

DWF ist ein offenes, sicheres Format, das speziell für die gemeinsame Nutzung umfangreicher Konstruktionsdaten entwickelt wurde. Es ist unabhängig von der ursprünglichen Anwendungssoftware, Hardware und dem Betriebssystem, die zum Erstellen dieser Konstruktionsdaten verwendet werden. Dadurch können Teammitglieder, die keine CAD-Anwendungen verwenden, an den digitalen Prozessen teilnehmen, indem sie Gebäude-, GIS- oder Produktdesigns anzeigen. Ein DWF-Dateiarchiv besteht aus mehreren XML- und Binärdateien, die zusammen in einem komprimierten Archiv verpackt sind, das mit [ZIP](/de/compression/zip/)-Komprimierung erstellt wurde. Sie können eine DWF-Dateierweiterung in ZIP umbenennen und den Inhalt der Datei anzeigen. Das DWF-Paket kann viele Arten von Konstruktionsdaten wie 2D-Grafiken, 3D-Grafiken, Paket- und Schnittmetadaten und andere Ressourcendateien enthalten.

**DWF-Metadatendateien** – XML-Dateien, die Informationen zu Metadaten und Struktur (Autor, Titel, Erstellungszeit, Abschnittsabhängigkeiten, Abschnittsreihenfolge, Ressourcendateibeschreibungen, Rollen, Mimetypen usw.) und zum Abschnitt (page Informationen, Design-Metadaten usw.). Die strukturellen Metadaten werden verwendet, um logische Objekte (Sammlungen von Dateien zur Darstellung eines Teils oder einer Seite usw.) zu erstellen.

**Ressourcendateien** – Medien- oder andere Inhaltsdateien, die von den Paket-/Abschnittsmetadaten referenziert werden und normalerweise Präsentationen von Designdaten in verschiedenen Formaten sind (ZGL, W2D, [JPG](/de/image/jpeg/), [PNG] (/de/image/png/), AVI, XML, [TXT](/de/word-processing/txt/), [DOC](/de/word-processing/doc/), usw.)

### Details zum Dateiformat ###

DWF-Dateien sind wie unten gezeigt in drei Hauptabschnitte unterteilt.

* Header zur Dateiidentifikation
* Dateidatenblock
* Trailer zur Dateibeendigung

#### Datei-ID-Header ####

Der Dateikennungs-Header ermöglicht die Identifizierung von DWF-Dateien durch Anwendungen. Es gibt auch an, welche Version der DWF-Spezifikationen zum Codieren der Datei verwendet wurde. Es ist ein 12-Byte-Header, der wie folgt angeordnet ist:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Zeichen|(|D|W|F|(Leerzeichen)|V|0|0|.|3|0|)

Hier ist eine Zusammenfassung dieser Tabelle:

* Die ersten sechs Bytes des Headers repräsentieren immer ASCII-Zeichen "(DWF V"
* Die folgenden 5 Bytes enthalten Informationen über die Versionsnummer zB "00.30" mit dem Major- und Minor-Versionswert des Formats

Anwendungen, die eine DWF-Datei erstellen, sollten die niedrigstmögliche Versionsnummer angeben, die eine Reader-Anwendung unterstützen muss, um die Daten ordnungsgemäß zu verwenden.

#### Dateidatenblock ####

Der Dateidatenblock beginnt am 13. Byte einer DWF-Datei und besteht aus einer Reihe von Opcode- und Operandenpaaren, wie in der folgenden Tabelle dargestellt.

|Feld 1|Feld 2|Feld 3|Feld 4|Feld 5|Feld 5
--- | --- |--- | --- |--- | --- |
|Opcode|Operand|Opcode|Operand|Opcode|Operand

Eine DWF-Datei kann Opcode-Operanden-Paare als lesbaren ASCII-Code sowie als Code-Binärdatei oder eine Mischung aus beiden enthalten. Alle DWF-Operationen haben eine lesbare ASCII-Opcode/Operandenform, und die meisten Operationen haben auch eine codierte binäre Opcode/Operandenform. Opcodes sind in Einzelbytes und ermöglichen über 200 Operationen. Ausnahmefälle sind Extended ASCII und Extended Binary. Die Werte von Opcodes können mit einigen Ausnahmen zwischen 0 und 255 liegen. Abgesehen von den beiden speziellen Arten von Opcodes Extended ASCII und Extended Binary muss ein Dateileser wissen, wie die Operandenlänge zu berechnen ist.

##### Verbotene Opcodes #####

Die ASCII-Darstellungen für Folgendes können nicht als Opcodes verwendet werden:

Folgende ASCII-Darstellungen können nicht als Opcodes verwendet werden:

* Leerzeichen (0x20)
* Registerkarte (0x09)
* Bindestrich (0x2D)
* ASCII-Ziffern 0-9 (0x30 - 0x39)
* Wagenrücklauf (0x0D)
* Zeilenvorschub (0x0A)
* Einfaches Anführungszeichen (0x27)
* Doppeltes Anführungszeichen (0x22)
* Punkt (0x2E)
* Klammern (0x28 und 0x29)
* Geschweifte Klammern (0x7B und 0x7D)
* Eckige Klammern (0x5B und 0x5D)
* Backslash (0x5C)

#### Trailer zur Dateibeendigung ####

Der Dateibeendigungstrailer für DWF ist einfach ein spezieller Opcode, der das Ende der Datei anzeigt. Einige Anwendungen können Nicht-DWF-Daten nach dem Beendigungs-Opcode speichern. Der Trailer sieht wie folgt aus:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Zeichen|(|E|n|d|0|f|D|W|F|)

## Verweise ##

* [DWF – Von Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [WHIP-Datenformat](http://paulbourke.net/dataformats/whip/)
* [http://blogs.msdn.com/opc/archive/2009/05/18/adventures-in-packaging-episode-1.aspx](http://blogs.msdn.com/opc/archive/2009 /05/18/adventures-in-packaging-episode-1.aspx)

