{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "file", "extension", "file format", "VB Project File", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Erfahren Sie mehr über das VBPROJ-Dateiformat und APIs, die VBPROJ-Dateien erstellen und öffnen können.",
  "linktitle" :"VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine VBPROJ-Datei?

Eine Datei mit der Erweiterung .vbproj ist eine Microsoft Visual Basic-Projektdatei, die von der MSBuild-Engine von Microsoft verwendet wird, um die Projekte innerhalb einer Visual Studio-Projektmappe zu erstellen. Sie ähnelt der Datei [CSPROJ](/de/programming/csproj/) für .NET-Projekte, die in [C#](/de/programming/cs/) geschrieben wurden. Die MSBuild-Engine liest Informationen, die in verschiedenen Gruppen aus den VBPROJ-Dateien enthalten sind, und generiert die Ausgabedatei. Eine VBPROJ-Datei kann Informationen enthalten, die sich auf globale Bezeichner, Klassen und Eigenschaften beziehen, die das Projekt definieren. VBPROJ-Dateien können mit Microsoft Visual Studio und jedem gängigen Texteditor wie Notepad auf Windows- und MacOS-Betriebssystemen geöffnet und bearbeitet werden.

## VBPROJ-Dateiformat - Weitere Informationen

VBPROJ-Dateien sind Textdateien, die im Dateiformat [XML](/de/web/xml/) basierend auf dem [MSBuild XML Schema](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild- Projektdatei-Schemareferenz?view=vs-2019). Eine VBPROJ-Datei enthält Informationen in Form von XML-Tags, die Informationen zu dieser bestimmten Gruppe von Einstellungen definieren. Es wird dringend empfohlen, diese Einstellungsdateien in Microsoft Visual Studio IDE zu öffnen und zu bearbeiten.

### VBPROJ-Elemente

Die Bestandteile einer VB-Einstellungsdatei sind in der folgenden Abbildung dargestellt.

{{< figure src="../vbproj.png" alt="VBPROJ-Dateiformat" >}}

Die folgende Tabelle enthält eine kurze Beschreibung dieser Elemente.

|Element|Beschreibung|
---|---|
|Projekt| Root-Element jeder Projektdatei und kann Attribute enthalten, um die Einstiegspunkte für den Erstellungsprozess zusätzlich zum Identifizieren des XML-Schemas für die Projektdatei anzugeben |
|Eigenschaften und Konditionen| Eigenschaften bestehen aus Schlüssel-Wert-Paaren und werden innerhalb eines PropertyGroup-Elements definiert. Der Eigenschaftselementname stellt den Eigenschaftsschlüssel dar und der Inhalt des Elements definiert den Eigenschaftswert.|
|Items und ItemGroups|Items in einer Projektdatei sind Eingaben für den Build-Prozess, wie z. B. Dateien-Code-Dateien, Konfigurationsdateien, Befehlsdateien und andere, die als Teil des Build-Prozesses benötigt werden. Artikel sind und müssen innerhalb eines ItemGroup-Elements definiert werden.|
|Ziele und Aufgaben| Ein Task-Element repräsentiert eine einzelne Build-Anweisung (oder Task). MSBuild enthält eine Vielzahl vordefinierter Aufgaben wie Copy, CSC, VBC, Exec. Tasks müssen immer in einem „Target“-Element enthalten sein, das aus einer oder mehreren Tasks besteht, die nacheinander ausgeführt werden, und eine Projektdatei kann mehrere Targets enthalten.|

## Verweise

* [Die Projektdatei verstehen](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild-Schemaelemente](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

