{
  "date": "2019-10-11",
  "keywords": [
"vcxproj",
"failą",
"pratęsimas",
"Dokumento formatas",
"Visual C++ projektas",
"Programavimo vadovas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "Sužinokite apie VCXPROJ failo formatą ir API, kurios gali kurti ir atidaryti VCXPROJ failus.",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxpro-ltj"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra VCXPROJ failas?

Failas su plėtiniu .vcxproj yra Microsoft Visual C++ projekto failas, kuriame saugoma [C++](/programming/cpp/) projekto informacija. Jame yra informacija, kurią MSBuild projekto sistema naudoja galutiniam išėjimui sudaryti ir sukurti. Visual C++ projektų VCXPROJ yra toks pat kaip [CSPROJ](/programming/csproj/), skirtas .NET projektams. VCXPROJ failuose nėra jokio kodo, bet jie nurodo visas klases, tikslus ir ypatybes, apibrėžtas projektui sukurti. Juos galima atidaryti paprasto teksto rengyklėse arba, pageidautina, Microsoft Visual Studio IDE.


## VCXPROJ failo formatas – daugiau informacijos

VCXPROJ failai yra tekstiniai failai, sukurti [XML](/web/xml/) failo formatu. Juos galima atidaryti bet kuriame teksto rengyklėje, tačiau labai rekomenduojama naudoti Microsoft Visual Studio IDE šiems failams atidaryti ir redaguoti. Jie nebuvo skirti redaguoti rankiniu būdu. Dėl klaidų IDE gali sugesti arba veikti netikėtai.

Pavyzdinio VCXPROJ failo turinys yra toks.

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
### VCXPROJ failo elementai

Įprastame VCXPROJ faile yra daug elementų, kaip matyti anksčiau pateiktame XML pavyzdyje. Microsoft [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) išsamiai paaiškina kiekvieną failo elementą ir gali būti nurodyta kūrėjo požiūriu.

#### Projekto elementas

Tai yra VCXPROJ failo šakninis mazgas. MSBuild naudoja šį elementą, kad nuskaitytų kūrimo versiją ir numatytąjį kompiliavimo tikslą.

#### ProjectConfigurations ItemGroup Element

Jame yra projekto konfigūracijos informacija, kuri gali apimti kūrimo metodą (derinimo arba išleidimo), 32 arba 64 bitų kompiliavimą, optimizavimo parinktis ir kt. Šios grupės informaciją naudoja IDE projektui įkelti.

#### Projekto konfigūracijos elementai

ProjectConfiguration elementuose VCXPROJ faile yra informacijos apie kūrimą ir platformą, kuriai įkeliamas projektas. Jos pavadinimas turi atitikti formatą $(Configuration)|$(Platform).

#### Globals PropertyGroup Element

Šiame skyriuje pateikiami nustatymai, kuriuose pateikiama projekto lygio informacija, pvz.:

 * ProjectGuid
 * RootNamespace
 * ApplicationType arba ApplicationTypeRevision


## Nuorodos

* [VCXPROJ struktūra – MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


