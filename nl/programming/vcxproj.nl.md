{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "bestand", "extensie", "bestandsindeling", "Visual C++ Project", "Programmeergids" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Meer informatie over de VCXPROJ-bestandsindeling en API's die VCXPROJ-bestanden kunnen maken en openen.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een VCXPROJ-bestand?

Een bestand met de extensie .vcxproj is een Microsoft Visual C++-projectbestand waarin de projectinformatie [C++](/nl/programming/cpp/) is opgeslagen. Het bevat informatie die door het MSBuild-projectsysteem wordt gebruikt om de uiteindelijke uitvoer te compileren en te bouwen. VCXPROJ van Visual C++-projecten is hetzelfde als die van [CSPROJ](/nl/programming/csproj/) voor .NET-projecten. VCXPROJ-bestanden bevatten geen code, maar verwijzen naar alle klassen, doelen en eigenschappen die zijn gedefinieerd voor het project om het project te bouwen. Deze kunnen worden geopend in platte teksteditors of bij voorkeur in Microsoft Visual Studio IDE.


## VCXPROJ-bestandsindeling - Meer informatie

VCXPROJ-bestanden zijn tekstbestanden die zijn gemaakt in de bestandsindeling [XML](/nl/web/xml/). Deze kunnen in elke teksteditor worden geopend, maar het wordt ten zeerste aanbevolen om Microsoft Visual Studio IDE te gebruiken voor het openen en bewerken van deze bestanden. Deze zijn niet ontworpen voor handmatige bewerking. Fouten kunnen ervoor zorgen dat de IDE crasht of zich op onverwachte manieren gedraagt.

De inhoud van een voorbeeld VCXPROJ-bestand is als volgt.

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
### VCXPROJ-bestandselementen

Een typisch VCXPROJ-bestand bevat een aantal elementen zoals te zien is in het voorbeeld-XML hierboven. De [VCXPROJ-structuur](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) van Microsoft legt elk bestandselement in detail uit en er kan naar worden verwezen vanuit het perspectief van de ontwikkelaar.

#### Projectelement

Dit is het hoofdknooppunt van het VCXPROJ-bestand. MSBuild gebruikt dit element om de buildversie en het standaarddoel voor compilatie te lezen.

#### ProjectConfiguraties ItemGroup Element

Het bevat de projectconfiguratie-informatie die de buildmethode (Debug of Release), 32- of 64-bits compilatie, optimalisatie-opties en andere kan bevatten. De informatie in deze groep wordt door IDE gebruikt om het project te laden.

#### Projectconfiguratie-elementen

De ProjectConfiguration-elementen in een VCXPROJ-bestand bevatten informatie over de build en het platform waarvoor het project is geladen. De naam moet het formaat `$(Configuration)|$(Platform)` volgen.

#### Globals PropertyGroup Element

Dit gedeelte bevat instellingen die informatie geven op projectniveau, zoals:

* ProjectGids
* Rootnaamruimte
* ApplicationType of ApplicationTypeRevision


## Referenties

* [VCXPROJ-structuur - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++-projectbestanden](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

