{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "Datei", "Erweiterung", "Dateiformat", "Excel Open XML", "Tabellenkalkulation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformat-Leitfaden, um zu wissen, was eine XLTX-Datei und APIs sind, die sie erstellen und öffnen können.",
  "title" :"Was ist eine XLTX-Datei?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Was ist eine XLTX-Datei?

Dateien mit der Erweiterung .xltx stellen Microsoft Excel-Vorlagendateien dar, die auf den Office OpenXML-Dateiformatspezifikationen basieren. Es wird verwendet, um eine Standardvorlagendatei zu erstellen, die zum Generieren von [XLSX](/de/spreadsheet/xlsx/)-Dateien verwendet werden kann, die dieselben Einstellungen wie in der XLTX-Datei angegeben aufweisen.

## Kurze Geschichte

Anfang des Jahres 2000 beschloss Microsoft, die Änderung vorzunehmen, um den Standard für **Office Open XML** aufzunehmen. Dokumente verschiedener Typen unter diesem neuen Standard wurden durch das Anhängen von „X“ in ihren Erweiterungen identifiziert, wobei „X“ für XML steht. 2007 wurde dieses neue Dateiformat Teil von Office 2007 und wird auch in den neuen Versionen von Microsoft Office weitergeführt. Der neue Dateityp hat zusätzliche Vorteile von kleinen Dateigrößen, weniger Änderungen durch Beschädigung und gut formatierter Bilddarstellung.

## XLTX-Dateiformatspezifikationen

XLTX-Dateien basieren auf dem Office OpenXML-Dateiformat und verwenden XML und [ZIP](/de/compression/zip/), um die Dateigröße zu reduzieren. Es wurde mit der Veröffentlichung von Microsoft Office 2007 erstellt, um das binäre XLT-Dateiformat zu ersetzen. Ähnlich wie XLTX kann das XLT-Dateiformat verwendet werden, um [XLS](/de/spreadsheet/xls/)-Dateien mit Microsoft Excel 2003 und 2007 zu erstellen. Diese können mit Microsoft Excel durch Doppelklicken auf die Datei geöffnet werden. Die Dateiorganisation in einem XLTX-Dateiformat kann beobachtet werden, indem Sie die Datei in ZIP umbenennen und dann ihren Inhalt auf die Disc extrahieren.

### [Content_Types].xml ###

Dies ist die einzige Datei, die beim Extrahieren der ZIP-Datei auf der Basisebene gefunden wird. Es listet die Inhaltstypen für Teile innerhalb des Pakets auf. Alle Verweise auf die im Paket enthaltenen XML-Dateien werden in dieser XML-Datei referenziert.

### \_rels (Ordner) ###

Dies ist der Ordner "Beziehungen", der eine einzelne XML-Datei enthält, in der die Beziehungen auf Paketebene gespeichert sind. Links zu den wichtigsten Teilen der Xltx-Dateien sind in dieser Datei als URIs enthalten. Diese URIs identifizieren die Art der Beziehung jedes Schlüsselteils zum Paket. Dies umfasst die Beziehung zum primären Office-Dokument, das sich als xl/workbook.xml befindet, und andere Teile innerhalb von docProps als Kern- und erweiterte Eigenschaften.

### docProps ###

Dieser Ordner enthält die allgemeinen Dokumenteigenschaften. Dazu gehören eine Reihe von Kerneigenschaften, eine Reihe von erweiterten oder anwendungsspezifischen Eigenschaften und eine Miniaturvorschau des Dokuments. Eine leere Arbeitsmappe enthält zwei Dateien in diesem Ordner, nämlich app.xml und core.xml. Die core.xml enthält Informationen wie Autor, Erstellungs- und Speicherdatum sowie Änderungsdatum. App.xml enthält Informationen zum Inhalt der Datei.

### xl (Ordner) ###

Dies ist der Hauptordner, der alle Details zum Inhalt der Arbeitsmappe enthält. Standardmäßig hat es folgende Ordner:

* \_rels
* Thema
* Arbeitsblätter

und folgende XML-Dateien:

* Stile.xml
* Arbeitsmappe.xml

## Verweise ##

* [[MS-XLSX] - .Xlsx-Dateiformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

