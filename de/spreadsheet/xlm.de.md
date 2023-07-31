{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "Datei", "Erweiterung", "Dateiformat", "Microsoft Excel-Makrodatei", "Tabellenkalkulation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformatleitfaden, um zu wissen, was eine XLM-Makrodatei und APIs sind, die XLM-Dateien erstellen und öffnen können.",
  "title" :"Was ist eine XLM-Datei?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Was ist eine XLM-Datei?

XLM, für Excel-Makro, ist eine Art Tabellenkalkulationsdatei, die zum Speichern von Makros verwendet wird. Aus Anwendungssicht ist ein Makro eine Reihe von Anweisungen, die zur Automatisierung von Prozessen verwendet werden. Ein Makro wird verwendet, um die Schritte aufzuzeichnen, die wiederholt für das Dateiformat [XLS](/de/spreadsheet/xls/) ausgeführt werden, und erleichtert das Ausführen der Aktionen durch erneutes Ausführen des Makros. Makros werden mit Microsofts Visual Basic for Applications (VBA) innerhalb der Excel-Arbeitsmappe mit dem Visual Basic-Editor programmiert und können direkt von dort aus ausgeführt/debuggt werden.

## Kurze Geschichte ##

Microsoft Excel unterstützte die Programmierung von Makros seit seiner ersten öffentlichen Einführung. Die Funktionen von Makros blieben in den nachfolgenden Versionen von Excel mit der Erweiterung gemäß den neuen Funktionen gleich. XLM war die Standardmakrosprache für Excel bis Excel 4.0. Excel 5.0 zeichnete Makros standardmäßig in VBA auf, aber mit Version 5.0 war die XLM-Aufzeichnung weiterhin als Option erlaubt. Nach Version 5.0 wurde diese Option eingestellt. Alle Versionen von Excel, einschließlich Excel 2010, können ein XLM-Makro ausführen, obwohl Microsoft von ihrer Verwendung abrät.

## Aufzeichnen eines Makros in XLM ##

Excel bietet benutzerfreundliche Schritte zum Aufzeichnen eines Makros. Es erfordert, dass Sie Entwicklertools installiert haben, um mit Makros arbeiten zu können. Sobald eine Makroaufzeichnung in Bearbeitung ist, zeichnet sie jede Benutzeraktion auf, die später abgespielt werden soll. Die Makroaufzeichnung umfasst eigentlich alle Schritte, die ein Benutzer nach Beginn der Aufzeichnung ausführt. Wenn Sie also den Inhalt einer Zelle fett, kursiv und ihre Textausrichtung einstellen, nachdem eine Makroaufzeichnung gestartet wurde, werden alle diese Befehle aufgezeichnet. Jedem aufgezeichneten Makro kann auch ein Shortcut für die spätere schnelle Wiedergabe zugewiesen werden. Die Makroaufzeichnung generiert VBA-Code in Form eines Makros, das mit dem Visual Basic Editor (VBE) bearbeitet werden kann.

## Excel-Objektmodell ##

Makros verwenden hinter sich VBA-Routinen und folgen zu diesem Zweck dem [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model). Dieses Modell identifiziert die Objekte einer Tabellenkalkulation für die Interaktion mit der Tabellenkalkulation durch benutzerdefinierte Befehlssymbolleisten, Befehlsleisten oder Meldungsfelder. Der Zugriff auf die Eigenschaften der Arbeitsmappe wird beispielsweise mit dem Workbook-Objekt gewährt. In ähnlicher Weise gibt es im Modell ein Arbeitsblattobjekt, um programmgesteuert mit den Arbeitsblättern der Arbeitsmappe zu arbeiten.

## Makros und Sicherheit ##

VBA ermöglicht den Zugriff auf alle Anwendungsbereiche sowie das Dateisystem und kann auch gefährlich sein. Dies wirft Bedenken auf, wenn die Arbeitsmappe mit jemandem geteilt wird, der die Datei an seinem Ende ausführen kann. Das heißt, Microsoft Excel warnt vor dem Öffnen einer solchen Datei. Makros können mit einer digitalen Signatur zertifiziert werden, damit andere Benutzer überprüfen können, ob diese vertrauenswürdig sind. Somit können Makros nach Überprüfung ihrer Quelle aktiviert werden.

## Verweise ##

* [[MS-XLS] - Struktur des Excel-Binärdateiformats](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Makroprogrammierung](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

