{
"Datum": "2023-05-31",
  "keywords": [
"Desktop-Datei",
"Was ist eine Desktop-Datei",
"Was enthält die Desktop-Datei",
"Beispiel-Desktop-Datei",
"So öffnen Sie eine Desktop-Datei",
"Was ist das Format der Desktop-Datei?",
"Datei",
"Desktop-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "DESKTOP-Dateiformat – Desktop-Eintragsdatei",
  "description":"Erfahren Sie mehr über das DESKTOP-Format und die APIs, mit denen DESKTOP-Dateien erstellt und geöffnet werden können.",
"linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent": "settings"
}
},
"lastmod": "31.05.2023"
}

## Was ist eine DESKTOP-Datei?

Eine .desktop-Datei ist eine Konfigurationsdatei, die von Linux-Desktop-Umgebungen zum Definieren von Anwendungsverknüpfungen und Startprogrammen verwendet wird. Es stellt Metadaten zu einer Anwendung bereit, z. B. ihren Namen, ihr Symbol, den auszuführenden Befehl und andere Eigenschaften. Diese Dateien werden typischerweise zum Erstellen von Verknüpfungen in Anwendungsmenüs, Desktop-Startprogrammen oder Panels in Linux-basierten Systemen verwendet.

## Was enthält die DESKTOP-Datei?

Eine .desktop-Datei folgt einem bestimmten Format und enthält mehrere Schlüsselfelder:

- **[Desktop-Eintrag]:** Dies ist der Hauptabschnittsheader für die .desktop-Datei.
- **Name:** Gibt den Namen der Anwendung an.
- **Kommentar:** Bietet eine kurze Beschreibung oder einen Kommentar zur Anwendung.
- **Exec:** Definiert den Befehl, der beim Starten der Anwendung ausgeführt werden soll.
- **Symbol:** Gibt den Pfad zur mit der Anwendung verknüpften Symboldatei an.
- **Terminal:** Gibt an, ob die Anwendung in einem Terminalfenster ausgeführt werden soll.
- **Typ:** Gibt die Art des Eintrags an, z. B. "Anwendung" oder "Link".
- **Kategorien:** Gibt Kategorien oder Gruppen an, unter denen die Anwendung im Menü angezeigt werden soll.
- **StartupNotify:** Gibt an, ob in der Desktop-Umgebung eine Startbenachrichtigung für die Anwendung angezeigt werden soll.
- **NoDisplay:** Gibt an, ob die Anwendung aus Menüs ausgeblendet werden soll.
- **Aktionen:** Definiert zusätzliche Aktionen, die in der Anwendung ausgeführt werden können, z. B. das Öffnen einer bestimmten Datei.

## Beispiel-DESKTOP-Datei

Hier ist ein Beispiel einer .desktop-Datei für einen fiktiven Texteditor namens "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

In diesem Beispiel definiert die .desktop-Datei die Anwendung "MyTextEditor" mit den zugehörigen Eigenschaften. Es enthält außerdem zwei zusätzliche Aktionen, "Neues Fenster öffnen" und "Vorhandene Datei öffnen", auf die über das Kontextmenü des Anwendungsstarters zugegriffen werden kann.

Durch das Platzieren einer .desktop-Datei in bestimmten Verzeichnissen wie "/usr/share/applications" oder "~/.local/share/applications" erkennt die Desktop-Umgebung sie und zeigt die Anwendung entsprechend in Menüs an oder ermöglicht den Start von ihr Desktop.

## Wie öffne ich die DESKTOP-Datei?

Mehrere Softwareprogramme können .desktop-Dateien öffnen und verarbeiten. Bei diesen Programmen handelt es sich typischerweise um Dateimanager oder Desktop-Umgebungen auf Linux-basierten Systemen. Hier sind einige Beispiele:

- **Nautilus (Dateien):** Der Standarddateimanager für die GNOME-Desktopumgebung.
- **Nemo:** Der Dateimanager für die Cinnamon-Desktop-Umgebung.
- **Dolphin:** Der Standarddateimanager für die KDE Plasma-Desktopumgebung.
- **Thunar:** Der Standarddateimanager für die Xfce-Desktopumgebung.
- **KDE-Menü-Editor:** Ein spezielles Tool für die KDE Plasma-Desktopumgebung, mit dem Sie .desktop-Dateien anzeigen und bearbeiten können.

Diese Dateimanager und Desktop-Umgebungen bieten eine grafische Oberfläche zum Verwalten von .desktop-Dateien. Sie ermöglichen Ihnen, Eigenschaften von .desktop-Dateien anzuzeigen und zu bearbeiten, Anwendungsstarter zu erstellen und Verknüpfungen in Anwendungsmenüs oder auf dem Desktop zu organisieren.

Bei den .desktop-Dateien handelt es sich um reine Textdateien, sodass Sie sie auch mit einem Texteditor Ihrer Wahl öffnen und bearbeiten können. Klicken Sie einfach mit der rechten Maustaste auf die .desktop-Datei und wählen Sie "Öffnen mit" oder "Öffnen mit einer anderen Anwendung", um einen Texteditor aus der Liste der installierten Programme auszuwählen.

## Was ist das Format der DESKTOP-Datei?

Das .desktop-Dateiformat folgt einer bestimmten Struktur und einem bestimmten Format. Es handelt sich um eine reine Textdatei mit einer Reihe von Schlüssel-Wert-Paaren, die in Abschnitte unterteilt sind. Hier eine Übersicht über das Format:

- **Abschnittsüberschriften:** Jeder Abschnitt beginnt mit einer Überschrift in eckigen Klammern ([]). Der primäre Abschnitt heißt normalerweise [Desktop-Eintrag] und enthält die Hauptmetadaten für die Anwendung oder den Launcher.
- **Schlüssel-Wert-Paare:** In jedem Abschnitt definieren Sie Eigenschaften mithilfe von Schlüssel-Wert-Paaren. Das Format ist "Schlüssel=Wert". Der Schlüssel identifiziert die Eigenschaft und der Wert liefert entsprechende Daten.
- **Eigenschaftssyntax:** Die Eigenschaftswerte können von unterschiedlichem Typ sein, einschließlich Zeichenfolgen, booleschen Werten, Dateipfaden oder Listen. Das Format für jeden Eigenschaftswert hängt von seinem Typ ab.
- **Kommentare:** Sie können Kommentare in die .desktop-Datei einfügen, indem Sie das Symbol "#" verwenden. Alles, was in der Zeile auf "#" folgt, gilt als Kommentar und wird ignoriert.

## Verweise
* [Desktop-Eintragsdateien](https://www.baeldung.com/linux/desktop-entry-files)

