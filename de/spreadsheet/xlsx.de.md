{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "Datei", "Erweiterung", "Dateiformat", "Excel", "Tabelle" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie, was eine XLSX-Datei und APIs sind, die XLSX-Dateien erstellen und öffnen können.",
  "title" :"XLSX-Dateiformat - Was ist eine XLSX-Datei?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Was ist eine XLSX-Datei?

**XLSX** ist ein bekanntes Format für Microsoft Excel-Dokumente, das von Microsoft mit der Veröffentlichung von Microsoft Office 2007 eingeführt wurde. Basierend auf einer Struktur, die gemäß den Open Packaging Conventions organisiert ist, wie in [Teil 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) des OOXML-Standards ECMA-376, ist das neue Format ein ZIP-Paket, das eine Reihe von XML-Dateien enthält. Die zugrunde liegende Struktur und Dateien können durch einfaches Entpacken der .xlsx-Datei untersucht werden.

## Kurze Geschichte des XLSX-Dateiformats

Das XLSX-Dateiformat wurde 2007 eingeführt und verwendet den Open XML-Standard, der bereits 2000 von Microsoft angepasst wurde. Vor XLSX war das übliche Dateiformat [XLS](/de/spreadsheet/xls/), das ein reines Binärdateiformat war. Der neue Dateityp hat zusätzliche Vorteile wie kleine Dateigrößen, weniger Änderungen durch Beschädigung und gut formatierte Bilddarstellung. Anfang des Jahres 2000 beschloss Microsoft, die Änderung vorzunehmen, um den Standard für **Office Open XML** aufzunehmen. 2007 wurde dieses neue Dateiformat Teil von Office 2007 und wird auch in den neuen Versionen von Microsoft Office weitergeführt.

## XLSX-Dateiformatspezifikationen

Die offiziellen [XLSX-Dateiformatspezifikationen](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) sind online bei Microsoft erhältlich. Um zu sehen, was sich in der XLSX-Datei befindet, benennen Sie sie einfach in [ZIP](/de/compression/zip/)-Datei um, indem Sie ihre Erweiterung ändern, und extrahieren Sie sie dann, um die konstituierenden Dateien dieser Excel-Arbeitsmappe anzuzeigen. Eine leere Arbeitsmappe enthält nach dem Extrahieren in ihre Dateien die folgenden Dateien und Ordner.

### [Content_Types].xml ###

Dies ist die einzige Datei, die beim Extrahieren der ZIP-Datei auf der Basisebene gefunden wird. Es listet die Inhaltstypen für Teile innerhalb des Pakets auf. Alle Verweise auf die im Paket enthaltenen XML-Dateien werden in dieser XML-Datei referenziert.

### \_rels (Ordner) ###

Dies ist der Ordner "Beziehungen", der eine einzelne XML-Datei enthält, in der die Beziehungen auf Paketebene gespeichert sind. Links zu den wichtigsten Teilen der Xlsx-Dateien sind in dieser Datei als URIs enthalten. Diese URIs identifizieren die Art der Beziehung jedes Schlüsselteils zum Paket. Dies umfasst die Beziehung zum primären Office-Dokument, das sich als xl/workbook.xml befindet, und andere Teile innerhalb von docProps als Kern- und erweiterte Eigenschaften.

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

## XLSX-Formatbeispiel ##


Für jedes in einer Arbeitsmappe enthaltene Excel-Arbeitsblatt gibt es eine XML-Datei. Sie finden diese XML-Dateien im Ordner xl/worksheets. Alle in einem Arbeitsblatt enthaltenen Informationen sind in verschiedenen Abschnitten in der XML-Datei organisiert. Sehen wir uns ein Beispielarbeitsblatt aus einer Arbeitsmappe an, die in der folgenden Abbildung dargestellt ist.

{{< figure src="../XLSX file format.png" alt="XLSX-Dateiformat" >}}

Wie zu sehen ist, enthält dieses Arbeitsblatt Inhalte in den Zellen A1 bis B2 und ein Bild. Darüber hinaus ist Zelle G13 derzeit die aktive Zelle im Arbeitsblatt. Sehen wir uns nun die Datei xl/worksheets/sheet1.xml an, um zu sehen, wie diese Informationen in der XML-Datei dargestellt werden. Der Inhalt dieser XML-Datei ist wie unten gezeigt.

{{< figure src="../XLSX File Format Details.png" alt="XPS-Dateiformat" >}}

1. Auf die Registerkarte wurde eine Designfarbe angewendet. Es wird in der XML-Datei mit Tag erwähnt<tabColor> nach der Themen-ID.
1. Der tabSelected-Wert wird auf 1 gesetzt, was anzeigt, dass dies das ausgewählte Blatt ist
1. Wie im ersten Bild oben zu sehen ist, ist die Zelle G13 im Arbeitsblatt eine aktive Zelle, die auch in der XML-Datei erwähnt wird.
1. Die Registerkarte Blattdaten stellt die im Arbeitsblatt enthaltenen Daten dar. Sie können jedoch sehen, dass sich der ursprüngliche Inhalt des Arbeitsblatts nirgendwo in diesem Abschnitt befindet. Dies liegt daran, dass auf den Text indirekt aus dem XML-Blatt „sharedStrings“ verwiesen wird. Durch diese Verlinkung wird sichergestellt, dass jeder Text nur einmal gespeichert wird und platzsparend wieder referenziert werden kann.
1. Das Bild, wie es zu sehen ist, wird durch die Referenz-ID „rId2“ referenziert.

## Beitragen

Müssen Sie etwas über XLSX- oder Spreadsheet-Dateiformate mitteilen? Sie können Ihre Ergebnisse im Abschnitt [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet) posten.

## Verweise

* [[MS-XLSX] - XLSX-Dateiformat](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

