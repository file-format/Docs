{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "file", "extension", "file format", "Visual C++ Project", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Erfahren Sie mehr über das VCXPROJ-Dateiformat und APIs, die VCXPROJ-Dateien erstellen und öffnen können.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine VCXPROJ-Datei?

Eine Datei mit der Erweiterung .vcxproj ist eine Microsoft Visual C++-Projektdatei, die die [C++](/de/programming/cpp/)-Projektinformationen speichert. Es enthält Informationen, die vom MSBuild-Projektsystem zum Kompilieren und Erstellen der endgültigen Ausgabe verwendet werden. VCXPROJ von Visual C++-Projekten ist dasselbe wie das von [CSPROJ](/de/programming/csproj/) für .NET-Projekte. VCXPROJ-Dateien enthalten keinen Code, sondern beziehen sich auf alle Klassen, Ziele und Eigenschaften, die für das Projekt definiert sind, um das Projekt zu erstellen. Diese können in einfachen Texteditoren oder vorzugsweise in Microsoft Visual Studio IDE geöffnet werden.


## VCXPROJ-Dateiformat - Weitere Informationen

VCXPROJ-Dateien sind Textdateien, die im Dateiformat [XML](/de/web/xml/) erstellt wurden. Diese können in jedem Texteditor geöffnet werden, es wird jedoch dringend empfohlen, Microsoft Visual Studio IDE zum Öffnen und Bearbeiten dieser Dateien zu verwenden. Diese wurden nicht für die manuelle Bearbeitung entwickelt. Fehler können dazu führen, dass die IDE abstürzt oder sich unerwartet verhält.

Der Inhalt einer Beispiel-VCXPROJ-Datei ist wie folgt.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ-Dateielemente

Eine typische VCXPROJ-Datei enthält eine Reihe von Elementen, wie im obigen XML-Beispiel zu sehen ist. Die [VCXPROJ-Struktur](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) von Microsoft erklärt jedes Dateielement im Detail und kann referenziert werden aus Entwicklersicht.

#### Projektelement

Dies ist der Stammknoten der VCXPROJ-Datei. MSBuild verwendet dieses Element, um die Buildversion und das Standardziel für die Kompilierung zu lesen.

#### ProjectConfigurations ItemGroup-Element

Es enthält die Projektkonfigurationsinformationen, die die Erstellungsmethode (Debug oder Release), 32- oder 64-Bit-Kompilierung, Optimierungsoptionen und andere enthalten können. Die Informationen in dieser Gruppe werden von der IDE zum Laden des Projekts verwendet.

#### Projektkonfigurationselemente

Die ProjectConfiguration-Elemente in einer VCXPROJ-Datei enthalten Informationen über den Build und die Plattform, für die das Projekt geladen wird. Sein Name sollte dem Format „$(Configuration)|$(Platform)“ folgen.

#### Globales PropertyGroup-Element

Dieser Abschnitt enthält Einstellungen, die Informationen für die Projektebene bereitstellen, z. B.:

* ProjectGuide
* RootNamespace
* ApplicationType oder ApplicationTypeRevision


## Verweise

* [VCXPROJ-Struktur – MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++-Projektdateien](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

