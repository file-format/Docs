{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "was ist eine cd-datei", "wie man eine cd-datei öffnet", "erweiterung", "datei", "cd-datei", "cd-dateiformat", "cd-dateierweiterung" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio-Klassendiagrammdatei",
  "description":"Erfahren Sie mehr über CD-Dateiformate und APIs, die CD-Dateien erstellen und öffnen können.",
  "linktitle" :"CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Was ist eine CD-Datei?

Eine Datei mit der Erweiterung .cd ist eine Visual Studio-Klassendiagrammdatei, die Informationen über die Struktur und Beziehung zwischen allen Klassen in der aktuellen Lösung bereitstellt. Eine Visual Studio-Projektmappe (dargestellt durch [.sln](/de/programming/sln/)) kann ein oder mehrere Projekte mit jeweils mehreren unterschiedlichen Klassen enthalten. Die Klassendiagrammdatei kann generiert werden, indem Sie mit der rechten Maustaste auf das Projekt klicken und die Option Klassendiagramm auswählen.

## Dateiformat für Klassendiagramme (.cd) – Weitere Informationen

Eine Klassendiagrammdatei wird im standardmäßigen XML-Dateiformat gespeichert, das Klassen in einem Projekt als XML-Knoten darstellt. Wenn Visual Studio nicht verfügbar ist, können diese Klassendiagrammdateien in jedem Anwendungsprogramm geöffnet werden, das das Öffnen von XML-Dateien unterstützt.

### So fügen Sie Klassendiagramme zu einem Visual Studio-Projekt hinzu

Öffnen Sie in Visual Studio die Lösung/das Projekt, für das Sie das Klassendiagramm hinzufügen möchten. Klicken Sie dann mit der rechten Maustaste auf den Projektknoten, und wählen Sie dann Hinzufügen > Neues Element aus. Oder drücken Sie STRG+UMSCHALT+A.

* Das Dialogfeld „Neues Element hinzufügen“ wird geöffnet.

* Erweitern Sie Gemeinsame Elemente > Allgemein und wählen Sie dann Klassendiagramm aus der Vorlagenliste aus. Suchen Sie bei Visual C++-Projekten in der Kategorie Hilfsprogramme nach der Vorlage Klassendiagramm.

### Klassendiagramme (CD) in Bilder exportieren

Visual Studio ermöglicht das Konvertieren/Exportieren von Klassendiagrammen in Bilder wie [PNG](/de/image/png/), [JPEG](/de/image/jpeg/) und [BMP](/de/image/bmp/). Diese exportierten Klassendiagrammdateien können für Dokumentations- und TDP-Aufzeichnungszwecke (Technische Datenpakete) verwendet werden. Um ein Klassendiagramm in ein Bild zu konvertieren, können die folgenden Schritte in Microsoft Visual Studio verwendet werden.

1. Öffnen Sie Ihre Klassendiagrammdatei (.cd).
1. Wählen Sie im Menü Klassendiagramm oder im Kontextmenü der Diagrammoberfläche die Option Diagramm als Bild exportieren.
1. Wählen Sie ein Diagramm aus.
1. Wählen Sie das gewünschte Format aus.
1. Wählen Sie Exportieren, um den Export abzuschließen.

## Verweise

* [Designklassen in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

