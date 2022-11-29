{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "fil", "tillägg", "filformat", "Visual C++ Project", "Programmeringsguide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Läs mer om VCXPROJ-filformat och API:er som kan skapa och öppna VCXPROJ-filer.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är en VCXPROJ fil?

En fil med tillägget .vcxproj är en Microsoft Visual C++-projektfil som lagrar projektinformationen [C++](/sv/programming/cpp/). Den innehåller information som används av MSBuild-projektsystemet för att kompilera och bygga slutresultatet. VCXPROJ för Visual C++-projekt är samma som för [CSPROJ](/sv/programming/csproj/) för .NET-projekt. VCXPROJ-filer innehåller ingen kod utan hänvisar till alla klasser, mål och egenskaper som definierats för projektet för att bygga projektet. Dessa kan öppnas i vanlig textredigerare eller helst i Microsoft Visual Studio IDE.


## VCXPROJ-filformat - Mer information

VCXPROJ-filer är textfiler som skapas i filformat [XML](/sv/web/xml/). Dessa kan öppnas i vilken textredigerare som helst, men det rekommenderas starkt att använda Microsoft Visual Studio IDE för att öppna och redigera dessa filer. Dessa var inte designade för manuell redigering. Misstag kan göra att IDE kraschar eller beter sig på oväntade sätt.

Innehållet i en VCXPROJ-exempelfil är som följer.

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
### VCXPROJ-filelement

En typisk VCXPROJ-fil innehåller ett antal element som kan ses i exemplet XML ovan. [VCXPROJ-strukturen](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) från Microsoft förklarar varje filelement i detalj och kan hänvisas till ur utvecklarens perspektiv.

#### Projektelement

Detta är rotnoden för VCXPROJ-filen. MSBuild använder detta element för att läsa byggversionen och standardmålet för kompilering.

#### ProjectConfigurations ItemGroup Element

Den innehåller projektkonfigurationsinformation som kan inkludera byggmetoden (debug eller release), 32 eller 64-bitars kompilering, optimeringsalternativ och annat. Informationen i denna grupp används av IDE för att ladda projektet.

#### ProjectConfiguration Elements

ProjectConfiguration-elementen i en VCXPROJ-fil innehåller information om bygget och plattformen för vilken projektet laddas. Dess namn bör följa formatet `$(Configuration)|$(Platform)`.

#### Globals PropertyGroup Element

Det här avsnittet innehåller inställningar som ger information för projektnivå som:

* ProjectGuid
* RootNamespace
* ApplicationType eller ApplicationTypeRevision


## Referenser

* [VCXPROJ-struktur - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ Project Files](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

