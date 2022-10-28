{
  "date" : "2019-10-11",
"Schlüsselwörter": [ "csproj-Datei", "csproj", "Erweiterung", "Format", "Was ist eine csproj-Datei", "csproj-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Erfahren Sie mehr über das CSPROJ-Dateiformat und APIs, die CSPROJ-Dateien erstellen und öffnen können.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Was ist eine CSProj-Datei?
Dateien mit der Erweiterung CSPROJ stellen eine C#-Projektdatei dar, die die Liste der in einem Projekt enthaltenen Dateien zusammen mit den Verweisen auf Systemassemblys enthält. Wenn ein neues Projekt in Microsoft VIiual Studio initiiert wird, erhalten Sie eine .csproj-Datei zusammen mit der Hauptlösungsdatei ([.sln](/de/programming/sln/)). Wenn es mehr als eine Assembly in einem Projekt gibt, gibt es auch die gleiche Anzahl von Projektdateien, wobei die .sln-Datei sie alle als Teil des Projekts zusammenbindet. Der Inhalt dieser Datei definiert alle Anforderungen, die zum Erstellen des Projekts erforderlich sind, z. B. einzuschließende Inhalte, Plattformanforderungen, Versionsinformationen, Webserver- oder Datenbankservereinstellungen und die auszuführenden Aufgaben. Der Inhalt einer Projektdatei ist im XML-Dateiformat angeordnet und kann in jedem Texteditor zum Bearbeiten und Anzeigen geöffnet werden. Es bietet auch eine logische Ansicht der Projektdateien für die richtige Anordnung.

## CSPROJ-Dateiformat #

Entwickler können Projektdateien auch selbst erstellen und dabei das [MSBuild-XML-Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx) berücksichtigen. Die offene und transparente Struktur von Projektdateien ermöglicht Anwendungsentwicklern eine ausgefeilte und feinkörnige Kontrolle darüber, wie die Projekte erstellt und bereitgestellt werden. Die Inhalte einer solchen Projektdatei stehen untereinander in einem sehr klaren Zusammenhang. Die folgende Abbildung zeigt Schlüsselelemente und die Beziehung zwischen diesen für eine solche Projektdatei.

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

In den folgenden Abschnitten werden die Dateiformatelemente für eine Projektdatei erläutert.

### Projektelement ###

Das Element [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) ist das Stammelement jeder Projektdatei. Es identifiziert das XML-Schema für die Projektdatei und kann Attribute enthalten, um die Einstiegspunkte für den Erstellungsprozess anzugeben.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Eigenschaften und Bedingungen

Eigenschaften stellen die notwendigen Informationen dar, die zum Erstellen eines Projekts erforderlich sind. Solche Eigenschaften werden in einem [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx)-Element definiert. Diese Eigenschaften bestehen aus Schlüssel-Wert-Paaren, wobei der Name des Eigenschaftselements den Eigenschaftsschlüssel und der Inhalt des Elements den Eigenschaftswert definiert. Beispielsweise könnten Sie Eigenschaften namens ServerName und ConnectionString definieren, um einen statischen Servernamen und eine Verbindungszeichenfolge zu speichern.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Über Elemente können Bedingungen angegeben werden, um die Kriterien für die Bewertung des Elements festzulegen. Dies wird durch das Bedingungswort angegeben, während die Eigenschaft wie unten gezeigt definiert wird:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Wenn MSBuild diese Eigenschaftsdefinition verarbeitet, prüft es zunächst, ob ein **$(OutputRoot)**-Eigenschaftswert verfügbar ist. Wenn der Eigenschaftswert leer ist – mit anderen Worten, der Benutzer hat keinen Wert für diese Eigenschaft angegeben – ergibt die Bedingung **true** und der Eigenschaftswert wird auf **..\Publish\Out.** gesetzt.

### Artikel und Artikelgruppen

Eine Projektdatei definiert Eingaben für den Erstellungsprozess, bei denen es sich tatsächlich um unterschiedliche Dateitypen handelt. In der MSBuild-Nomenklatur werden diese Eingaben durch Item-Elemente dargestellt und in einem [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx)-Element definiert. Genau wie **Property**-Elemente können Sie ein **Item**-Element beliebig benennen. Sie müssen jedoch ein **Include**-Attribut angeben, um die Datei oder den Platzhalter zu identifizieren, die das Element darstellt.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Ziele und Aufgaben

Ein [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx)-Element stellt eine einzelne Build-Anweisung (oder Aufgabe) dar. MSBuild enthält eine Vielzahl vordefinierter Aufgaben. Zum Beispiel:

* Die Aufgabe **Kopieren** kopiert Dateien an einen neuen Speicherort.
* Die Aufgabe **Csc** ruft den Visual C#-Compiler auf.
* Die Aufgabe **Vbc** ruft den Visual Basic-Compiler auf.
* Die Task **Exec** führt ein bestimmtes Programm aus.
* Die Task **Message** schreibt eine Nachricht an einen Logger.

Aufgaben müssen immer in [Target](https://msdn.microsoft.com/library/t50z2hka.aspx)-Elementen enthalten sein. Ein **Target**-Element ist ein Satz aus einer oder mehreren Aufgaben, die nacheinander ausgeführt werden, und eine Projektdatei kann mehrere Ziele enthalten.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Verweise

* [Die Projektdatei verstehen – MSDN](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- Datei)

