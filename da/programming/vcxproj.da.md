{
  "date": "2019-10-11",
  "keywords": [
"vcxproj",
"fil",
"udvidelse",
"filformat",
"Visual C++ projekt",
"Programmeringsvejledning"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "Lær om VCXPROJ filformat og API'er, der kan oprette og åbne VCXPROJ filer.",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxpro-daj"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en VCXPROJ fil?

En fil med filtypenavnet .vcxproj er en Microsoft Visual C++-projektfil, der gemmer [C++](/programming/cpp/)-projektoplysningerne. Den indeholder information, der bruges af MSBuild-projektsystemet til at kompilere og bygge det endelige output. VCXPROJ af Visual C++-projekter er den samme som for [CSPROJ](/programming/csproj/) for .NET-projekter. VCXPROJ-filer indeholder ingen kode, men henviser til alle klasser, mål og egenskaber, der er defineret for projektet for at bygge projektet. Disse kan åbnes i almindelige teksteditorer eller helst i Microsoft Visual Studio IDE.


## VCXPROJ-filformat - flere oplysninger

VCXPROJ-filer er tekstfiler, der er oprettet i filformatet [XML](/web/xml/). Disse kan åbnes i enhver teksteditor, men det anbefales stærkt at bruge Microsoft Visual Studio IDE til at åbne og redigere disse filer. Disse var ikke designet til manuel redigering. Fejl kan få IDE til at gå ned eller opføre sig på uventede måder.

Indholdet af en eksempel-VCXPROJ-fil er som følger.

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
### VCXPROJ-filelementer

En typisk VCXPROJ-fil indeholder en række elementer, som kan ses i eksemplet XML ovenfor. [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) fra Microsoft forklarer hvert filelement i detaljer og kan henvises fra udviklerens perspektiv.

#### Projektelement

Dette er rodknudepunktet for VCXPROJ-filen. MSBuild bruger dette element til at læse buildversionen og standardmålet for kompilering.

#### ProjectConfigurations ItemGroup Element

Den indeholder projektkonfigurationsoplysninger, der kan omfatte byggemetoden (fejlretning eller udgivelse), 32 eller 64-bit kompilering, optimeringsmuligheder og andre. Information i denne gruppe bruges af IDE til at indlæse projektet.

#### ProjectConfiguration Elements

ProjectConfiguration-elementerne i en VCXPROJ-fil indeholder information om den build og platform, som projektet er indlæst til. Dens navn skal følge formatet `$(Configuration)|$(Platform)`.

#### Globals PropertyGroup Element

Dette afsnit indeholder indstillinger, der giver oplysninger for projektniveau, såsom:

 * ProjektGuid
 * RootNamespace
 * ApplicationType eller ApplicationTypeRevision


## Referencer

* [VCXPROJ-struktur - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


