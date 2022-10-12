{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformat-Leitfaden, um zu wissen, was eine _XLSX-Datei und APIs sind, die _XLSX-Dateien erstellen und öffnen können.",
  "title" :"Was ist eine _XLSX-Datei?",
  "linktitle" :"_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Was ist eine _XLSX-Datei?

Eine Datei mit der Erweiterung .\_xlsx ist eigentlich eine [XLSX](/de/spreadsheet/xlsx/)-Datei, die von einer anderen Anwendung umbenannt wird. Dies kann in bestimmten Fällen passieren, wenn der Dateiname eine . am Ende des Dateinamens. Die \_XLSX-Dateien können in Microsoft Excel ähnlich wie die XLSX-Dateien geöffnet werden, indem diese wieder in die Erweiterung .xlsx umbenannt werden.

## _XLSX-Dateiformat - Weitere Informationen

Die _XLSX-Dateien unterscheiden sich nicht von den XLSX-Dateien und verwenden den von Microsoft im Jahr 2000 übernommenen Open XML-Standard. Vor XLSX war [XLS](/de/spreadsheet/xls/) das primäre Dateiformat, das für die Arbeit mit Excel-Tabellen zum Speichern von Dokumenten verwendet wurde im Binärformat. Dieses neue XML-basierte Dateiformat hatte Vorteile wie kleine Dateigrößen, Widerstandsfähigkeit gegen Dateibeschädigung und gut formatierte Bilddarstellung. Dieses neue XML-basierte Dateiformat wurde Bestandteil von Office 2007 und wird auch in den neuen Versionen von Microsoft ausgeführt.

## \_XLSX-Dateiformatspezifikationen

Da eine \_XLSX-Datei in eine XLSX-Datei umbenannt wird, hat sie die gleichen Spezifikationen wie die Originaldatei. Es ist nur eine Archivdatei, die auf dem Archivdateiformat [ZIP](/de/compression/zip/) basiert. Wenn Sie den Inhalt dieses Archivs sehen möchten, benennen Sie die Datei einfach in die Erweiterung .zip um und extrahieren Sie sie, um die Bestandteile dieser Excel-Arbeitsmappe anzuzeigen. Eine leere Arbeitsmappe enthält nach dem Extrahieren in ihre Dateien die folgenden Dateien und Ordner.

### [Content_Types].xml

Dies ist die einzige Datei, die beim Extrahieren der ZIP-Datei auf der Basisebene gefunden wird. Es listet die Inhaltstypen für Teile innerhalb des Pakets auf. Alle Verweise auf die im Paket enthaltenen XML-Dateien werden in dieser XML-Datei referenziert.

### \_rels (Ordner)

Dies ist der Ordner "Beziehungen", der eine einzelne XML-Datei enthält, in der die Beziehungen auf Paketebene gespeichert sind. Links zu den wichtigsten Teilen der Xlsx-Dateien sind in dieser Datei als URIs enthalten. Diese URIs identifizieren die Art der Beziehung jedes Schlüsselteils zum Paket. Dies umfasst die Beziehung zum primären Office-Dokument, das sich als xl/workbook.xml befindet, und andere Teile innerhalb von docProps als Kern- und erweiterte Eigenschaften.

### docProps

Dieser Ordner enthält die allgemeinen Dokumenteigenschaften. Dazu gehören eine Reihe von Kerneigenschaften, eine Reihe von erweiterten oder anwendungsspezifischen Eigenschaften und eine Miniaturvorschau des Dokuments. Eine leere Arbeitsmappe enthält zwei Dateien in diesem Ordner, nämlich app.xml und core.xml. Die core.xml enthält Informationen wie Autor, Erstellungs- und Speicherdatum sowie Änderungsdatum. App.xml enthält Informationen zum Inhalt der Datei.

### xl (Ordner)

Dies ist der Hauptordner, der alle Details zum Inhalt der Arbeitsmappe enthält. Standardmäßig hat es folgende Ordner:

* \_rels
* Thema
* Arbeitsblätter

und folgende XML-Dateien:

* Stile.xml
* Arbeitsmappe.xml

## Verweise

* [MS-XLSX - .xlsx-Dateiformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

