{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "soubor", "rozšíření", "formát souboru", "Projekt Visual C++", "Průvodce programováním" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Další informace o formátu souboru VCXPROJ a rozhraních API, která mohou vytvářet a otevírat soubory VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor VCXPROJ?

Soubor s příponou .vcxproj je soubor projektu Microsoft Visual C++, který ukládá informace o projektu [C++](/cs/programming/cpp/). Obsahuje informace, které používá systém projektu MSBuild ke kompilaci a sestavení konečného výstupu. VCXPROJ projektů Visual C++ je stejný jako [CSPROJ](/cs/programming/csproj/) pro projekty .NET. Soubory VCXPROJ neobsahují žádný kód, ale odkazují na všechny třídy, cíle a vlastnosti definované pro projekt k sestavení projektu. Ty lze otevřít v editorech prostého textu nebo nejlépe v Microsoft Visual Studio IDE.


## Formát souboru VCXPROJ - Další informace

Soubory VCXPROJ jsou textové soubory, které jsou vytvořeny ve formátu souboru [XML](/cs/web/xml/). Tyto soubory lze otevřít v libovolném textovém editoru, ale pro otevírání a úpravy těchto souborů se důrazně doporučuje použít Microsoft Visual Studio IDE. Tyto nebyly navrženy pro ruční úpravy. Chyby mohou způsobit selhání IDE nebo se chovat neočekávaným způsobem.

Obsah ukázkového souboru VCXPROJ je následující.

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
### Prvky souboru VCXPROJ

Typický soubor VCXPROJ obsahuje řadu prvků, jak je vidět na příkladu XML výše. [Struktura VCXPROJ](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) od společnosti Microsoft podrobně vysvětluje každý prvek souboru a lze na ni odkazovat z pohledu vývojáře.

#### Prvek projektu

Toto je kořenový uzel souboru VCXPROJ. MSBuild používá tento prvek ke čtení verze sestavení a výchozího cíle pro kompilaci.

#### Prvek ProjectConfigurations ItemGroup

Obsahuje informace o konfiguraci projektu, které mohou zahrnovat metodu sestavení (Debug nebo Release), 32 nebo 64bitovou kompilaci, možnosti optimalizace a další. Informace v této skupině používá IDE k načtení projektu.

#### Prvky konfigurace projektu

Prvky ProjectConfiguration v souboru VCXPROJ obsahují informace o sestavení a platformě, pro kterou je projekt načten. Jeho název by měl být ve formátu `$(Konfigurace)|$(Platforma)`.

#### Prvek Globals PropertyGroup

Tato část obsahuje nastavení, která poskytují informace pro úroveň projektu, jako jsou:

* ProjectGuid
* Kořenový jmenný prostor
* ApplicationType nebo ApplicationTypeRevision


## Reference

* [Struktura VCXPROJ – MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

