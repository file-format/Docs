{
  "date" : "2019-10-11",
"Schlüsselwörter": [ "sln-Datei", "Wie man eine sln-Datei ausführt", "sln", "Erweiterung", "Format", "Was ist eine sln-Datei", "sln-Dateiformat", "Visual Studio Solution", "Visual Studio-Lösung VS-Projekt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Erfahren Sie mehr über das SLN-Dateiformat und APIs, die SLN-Dateien erstellen und öffnen können.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist SLN-Datei?
Eine Datei mit der Erweiterung .SLN stellt eine **Visual Studio-Lösungsdatei** dar, die Informationen über die Organisation von Projekten in einer Lösungsdatei enthält. Der Inhalt einer solchen Lösungsdatei wird im Klartext in die Datei geschrieben und kann angezeigt/bearbeitet werden, indem die Datei in einem beliebigen Texteditor geöffnet wird. Die in einer Lösungsdatei enthaltenen Informationen bleiben persistent und werden verwendet, um die mit der Lösung verknüpften Informationen wie [Projekte](/de/programming/csproj/) und alle anderen erforderlichen Informationen zu laden. Die Projektdateien, auf die von der Projektmappendatei verwiesen wird, enthalten zusätzliche Informationen, damit die Umgebung die Hierarchie mit den Elementen dieses Projekts füllen kann. In der .sln-Datei werden keine Daten gespeichert, obwohl Projektinformationen bei Bedarf in die .sln-Datei geschrieben werden können.

## **Geschichte der SLN-Versionen** ##

Die Version des Lösungsformats hat sich im Laufe der Zeit mit jeder Microsoft Visual Studio-Lösung weiterentwickelt. Die Details dazu sind wie folgt.


|Visual Studio-Version|Version des Lösungsformats
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Inhalt einer Lösungsdatei** ###

Eine Lösungsdatei besteht aus mehreren Abschnitten, die von der Umgebung gelesen werden, um das Projekt zu laden. Der Inhalt einer Beispiel-.sln-Datei ist unten dargestellt.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Projekterklärung** ###

Eine Lösungsdatei kann mehr als eine Projektdeklaration enthalten, und zwar auch von unterschiedlichen Projekttypen. Beispielsweise kann eine einzelne Lösungsdatei sowohl ein CSharp- als auch ein VB.NET-Projekt enthalten. Diese Typen werden in einer Lösung anhand der [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) unterschieden. Die obige Projekterklärung kann zum besseren Verständnis wie folgt verallgemeinert werden.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Die Project-Type-GUID ist für verschiedene Projekttypen eindeutig und wird vom Lösungsleser verwendet, um den Projekttyp zu identifizieren. In diesem Fall zeigt F184B08F-C81C-45F6-A57F-5ABD9991F28F, dass es sich um ein VB.NET-Projekt handelt.

„Projekt-GUID“: Die eindeutige GUID des Projekts, die es von anderen Projekten in der Lösung unterscheidet. Die eindeutige ID eines Projekts in der Lösung ermöglicht anderen Projekten in der Lösung den Zugriff darauf.

Basierend auf den im Projektabschnitt der .sln-Datei enthaltenen Informationen lädt die Umgebung jede Projektdatei. Das Projekt selbst ist dann dafür verantwortlich, die Projekthierarchie zu füllen und alle verschachtelten Projekte zu laden. Alle an der Lösung vorgenommenen Änderungen werden beim Speichern oder Schließen des Projekts wieder in der Lösungsdatei gespeichert.

## Visual Studio-Lösung VS-Projekt

**Projekt:** Wenn Sie beginnen, eine App oder Software mithilfe von Visual Studio zu erstellen, starten Sie logischerweise ein neues Projekt. Ein Projekt enthält alle notwendigen Dateien wie Quellcode, Symbole, Bilder, Datendateien und mehr, die zu einer ausführbaren App, Website oder Bibliothek kompiliert werden.

**Lösung:** Eine Lösung enthält ein oder mehrere Projekte. Die Lösung ist also wie ein Container für Visual Studio-Projekte. Logischerweise können wir sagen, dass jemand eine Komplettlösung für sein Unternehmen haben möchte, einschließlich einer Website, einer Desktop-App, einem erholsamen Service und einer mobilen App.

### **Verweise** ###

* [Lösungsdatei – von MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [Projekttyp-GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

