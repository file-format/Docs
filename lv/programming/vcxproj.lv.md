{
  "date": "2019-10-11",
  "keywords": [
"vcxproj",
"failu",
"pagarinājumu",
"faila formātā",
"Visual C++ projekts",
"Programmēšanas rokasgrāmata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "Uzziniet par VCXPROJ faila formātu un API, kas var izveidot un atvērt VCXPROJ failus.",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxpro-lvj"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir VCXPROJ fails?

Fails ar paplašinājumu .vcxproj ir Microsoft Visual C++ projekta fails, kurā tiek saglabāta [C++](/programming/cpp/) projekta informācija. Tajā ir informācija, ko MSBuild projektu sistēma izmanto, lai apkopotu un izveidotu gala rezultātu. Visual C++ projektu VCXPROJ ir tāds pats kā [CSPROJ](/programming/csproj/) .NET projektiem. VCXPROJ faili nesatur nekādu kodu, bet attiecas uz visām klasēm, mērķiem un rekvizītiem, kas definēti projektam, lai izveidotu projektu. Tos var atvērt vienkārša teksta redaktoros vai vēlams Microsoft Visual Studio IDE.


## VCXPROJ faila formāts — vairāk informācijas

VCXPROJ faili ir teksta faili, kas izveidoti [XML](/web/xml/) faila formātā. Tos var atvērt jebkurā teksta redaktorā, taču šo failu atvēršanai un rediģēšanai ir ļoti ieteicams izmantot Microsoft Visual Studio IDE. Tie nebija paredzēti manuālai rediģēšanai. Kļūdas var izraisīt IDE avāriju vai neparedzētas darbības.

VCXPROJ faila parauga saturs ir šāds.

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
### VCXPROJ faila elementi

Tipisks VCXPROJ fails satur vairākus elementus, kā redzams iepriekš minētajā XML piemērā. Microsoft [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) detalizēti izskaidro katru faila elementu, un to var atsaukties no izstrādātāja viedokļa.

#### Projekta elements

Šis ir VCXPROJ faila saknes mezgls. MSBuild izmanto šo elementu, lai lasītu būvējuma versiju un noklusējuma kompilācijas mērķi.

#### ProjectConfigurations ItemGroup Element

Tajā ir ietverta projekta konfigurācijas informācija, kas var ietvert veidošanas metodi (atkļūdošana vai izlaišana), 32 vai 64 bitu kompilāciju, optimizācijas opcijas un citas. Šīs grupas informāciju izmanto IDE, lai ielādētu projektu.

#### ProjectConfiguration Elements

ProjectConfiguration elementi VCXPROJ failā satur informāciju par būvējumu un platformu, kurai projekts tiek ielādēts. Tās nosaukumam ir jāatbilst formātam $(Configuration)|$(Platform).

#### Globals PropertyGroup elements

Šajā sadaļā ir iestatījumi, kas sniedz informāciju projekta līmenī, piemēram:

 * ProjectGuid
 * RootNamespace
 * ApplicationType vai ApplicationTypeRevision


## Atsauces

* [VCXPROJ struktūra — MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


