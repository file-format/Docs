{
  "date" : "2021-04-23",
"Schlüsselwörter": [ "RES-Datei", "wie man eine res-Datei öffnet", "was ist eine res-Datei", "Erweiterung", "format", "RES-Dateiformat" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ kompiliertes Ressourcenskript",
  "description":"Erfahren Sie mehr über das RES-Dateiformat mit RES-Beispiel und APIs, die RES-Dateien erstellen und öffnen können.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Was ist eine RES-Datei?
Die Datei mit dem Suffix oder der Erweiterung .res kann zu vielen Dateiformatkategorien gehören. Hier diskutieren wir das RES-Dateiformat, das ein C++-kompiliertes Ressourcenskript ist; eine vom Microsoft Resource Compiler (rc) erstellte Binärdatei, die Ressourcendaten enthält; basierend auf dem Inhalt der Ressourcendefinitionsdatei; relevant für das übergeordnete Softwareprojekt. Die RES-Datei wird normalerweise in eine Ressourcenobjektdatei umformatiert, um sie mit der ausführbaren Datei einer Anwendung zu verknüpfen.

## RES-Dateiformat
Das RES-Dateiformat gehört zum Microsoft Resource Compiler (rc). Der Ressourcencompiler ist ein Tool, das Ressourcen wie Cursor, Symbole, Menüs und Dialogfelder kompiliert, die Ihre Anwendung verwendet. Die Ressourcendateien haben normalerweise die Erweiterung .res; enthält Ressourcen wie Cursor, Bilder und Versionsinformationen. Eine RES-Datei kann eine 16- oder 32-Bit-Ressourcendatei sein.
## Struktur der Ressourcendatei
Eine Ressourcendatei enthält eine Reihe verschiedener Ressourceneinträge. Jeder Eintrag enthält einen Ressourcenkopf und relevante Daten. Ein Ressourcen-Header ist in der Datei normalerweise DWORD-ausgerichtet und enthält Folgendes:

- Ein **DWORD**, um die Größe des Ressourcenheaders anzugeben
- Ein **DWORD**, um die Größe der Ressourcendaten anzugeben
- Der Ressourcentyp
- Der Ressourcenname
- Zusätzliche Ressourceninformationen

Die Ressourcenkopfstruktur definiert das Format der RES-Datei. Die Daten für die Ressource folgen dem Ressourcenheader. Einige Ressourcen fügen auch ein ressourcenspezifisches Gruppenkopfmuster hinzu, um Informationen über eine Gruppe von Ressourcen bereitzustellen. Im Folgenden sind einige der Ressourceneintragstypen und ihre Beschreibung aufgeführt:

### Accelerator-Tabellenressourcen
Eine Beschleunigertabelle ist ein Ressourceneintrag in einer RES-Datei ohne Gruppenheader. Das Muster **ACCELTABLEENTRY** definiert jeden Eintrag in der Beschleunigertabelle. Eine RES-Datei kann mehrere Beschleunigertabellen haben.

### Cursor- und Icon-Ressourcen
Obwohl das System jedes Symbol und jeden Cursor als eine einzelne Datei betrachtet, werden diese jedoch in RES-Dateien als eine Gruppe von Symbolressourcen oder eine Gruppe von Cursorressourcen gespeichert. Die Dateiformate von Icon- und Cursor-Ressourcen sind gleich. Ein Ressourcengruppenheader folgt allen einzelnen Symbol- oder Cursorgruppenkomponenten in der RES-Datei.

### Dialogfeldressourcen
Auch ein Dialogfenster wird als Ressourceneintrag in der RES-Datei realisiert. Es enthält ein **DLGTEMPLATE**-Kopfzeilenmuster für Dialogfelder und ein **DLGITEMTEMPLATE**-Muster für jedes spezifische Steuerelement im Dialogfeld. Die Muster **DLGTEMPLATEEX** und **DLGITEMTEMPLATEEX** erläutern das Format von erweiterten Dialogfeldressourcen.

### Font-Ressourcen
Eine Menüressource enthält ein **MENUHEADER**-Muster, gefolgt von einem oder mehreren **NORMALMENUITEM**- oder **POPUPMENUITEM**-Mustern, eines für jeden Menüpunkt in der Menüvorlage. Die Muster **MENUEX_TEMPLATE_HEADER** und **MENUEX_TEMPLATE_ITEM** erläutern das Format der erweiterten Menüressourcen.

### Nachrichtentabellen-Ressourcen
Eine Meldungstabelle besteht aus formatiertem Text zur Anzeige als Fehlermeldung oder in einem Meldungsfeld. Das Hauptmuster in einer Nachrichtentabellenressource ist die **MESSAGE_RESOURCE_DATA**-Struktur.

### Versionsressourcen
Das Hauptmuster in einer Versionsressource ist **VS_FIXEDFILEINFO**. Zusätzliche Muster umfassen **VarFileInfo** zum Speichern von sprachbezogenen Daten und **StringFileInfo** für benutzerdefinierte Zeichenfolgeninformationen.




## Verweise

* [Ressourcendateiformate](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



