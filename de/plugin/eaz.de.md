{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ-Datei – Was ist eine EAZ-Datei und wie öffnet man sie?",
  "description":"EAZ-Datei – Was ist eine EAZ-Datei und wie öffnet man sie?",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-eaz"
}
},
  "lastmod" : "2023-12-23"
}

## Was ist eine EAZ-Datei?

Die EAZ-Datei ist eine Add-In-Datei, die von ArcGIS Explorer verwendet wird, einer kostenlosen Anwendung, die von ESRI zur Kartenerkundung, Visualisierung und Freigabe entwickelt wurde. Es enthält ein komprimiertes Dateiarchiv, das einen [XML file](/web/xml/), kompilierten Code und unterstützende Dateien enthält, die für das Add-In erforderlich sind. Diese Dateien werden verwendet, um die Basisfunktionalität der Software durch die Integration neuer Schaltflächen, andockbarer Fenster und anderer Erweiterungen zu erweitern.

## EAZ-Dateiformat – Weitere Informationen

EAZ-Dateien werden mithilfe des ArcGIS Explorer SDK erstellt, einem Entwicklungskit zum Erstellen benutzerdefinierter Funktionen in ArcGIS Explorer. Diese Dateien nutzen die Komprimierung [ZIP](/compression/zip/), um ihren Inhalt effizient zu verpacken. Im Kern des Archivs befindet sich die Datei **Addins.xml** im Stammverzeichnis und dient als wichtige Komponente, die die verschiedenen in der EAZ-Datei eingebetteten Anpassungen beschreibt und detailliert beschreibt.

Die Datei Addins.xml fungiert im Wesentlichen als Roadmap und bietet Einblicke in die spezifischen Verbesserungen, Änderungen und Erweiterungen, die die EAZ-Datei in ArcGIS Explorer einführt. Durch diese umfassende Struktur können Entwickler neue Funktionen, Schaltflächen und andockbare Fenster kapseln und nahtlos integrieren und so die Gesamtfunktionalität und Benutzererfahrung der ArcGIS Explorer-Anwendung verbessern.

## Verweise

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
