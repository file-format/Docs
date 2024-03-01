{
  "date": "2019-10-11",
  "keywords": [
"vcxproj",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Visuaalinen C++-projekti",
"Ohjelmointiopas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "Opi VCXPROJ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VCXPROJ-tiedostoja.",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxpro-fij"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on VCXPROJ-tiedosto?

Tiedosto, jonka laajennus on .vcxproj, on Microsoft Visual C++ -projektitiedosto, joka tallentaa [C++](/programming/cpp/)-projektin tiedot. Se sisältää tietoja, joita MSBuild-projektijärjestelmä käyttää lopputuloksen kokoamiseen ja rakentamiseen. Visual C++ -projektien VCXPROJ on sama kuin .NET-projektien [CSPROJ](/programming/csproj/). VCXPROJ-tiedostot eivät sisällä mitään koodia, mutta viittaavat kaikkiin luokkiin, kohteisiin ja ominaisuuksiin, jotka on määritetty projektille projektin rakentamiseksi. Ne voidaan avata pelkillä tekstieditoreilla tai mielellään Microsoft Visual Studio IDE:ssä.


## VCXPROJ-tiedostomuoto – lisätietoja

VCXPROJ-tiedostot ovat tekstitiedostoja, jotka on luotu [XML](/web/xml/)-tiedostomuodossa. Nämä voidaan avata missä tahansa tekstieditorissa, mutta on erittäin suositeltavaa käyttää Microsoft Visual Studio IDE:tä näiden tiedostojen avaamiseen ja muokkaamiseen. Näitä ei ole suunniteltu manuaaliseen muokkaukseen. Virheet voivat aiheuttaa IDE:n kaatumisen tai käyttäytymisen odottamattomilla tavoilla.

Esimerkki VCXPROJ-tiedoston sisällöstä on seuraava.

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
### VCXPROJ-tiedostoelementit

Tyypillinen VCXPROJ-tiedosto sisältää useita elementtejä, kuten yllä olevasta XML-esimerkistä näkyy. Microsoftin [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) selittää jokaisen tiedostoelementin yksityiskohtaisesti, ja siihen voidaan viitata kehittäjän näkökulmasta.

#### Projektielementti

Tämä on VCXPROJ-tiedoston juurisolmu. MSBuild käyttää tätä elementtiä koontiversion ja käännöksen oletuskohteen lukemiseen.

#### ProjectConfigurations ItemGroup Element

Se sisältää projektin kokoonpanotiedot, jotka voivat sisältää koontimenetelmän (Debug tai Release), 32- tai 64-bittisen käännöksen, optimointivaihtoehdot ja muut. IDE käyttää tämän ryhmän tietoja projektin lataamiseen.

#### ProjectConfiguration Elements

VCXPROJ-tiedoston ProjectConfiguration-elementit sisältävät tietoja koontiversiosta ja alustasta, jolle projekti ladataan. Sen nimen tulee noudattaa muotoa `$(Configuration)|$(Platform)`.

#### Globals PropertyGroup Element

Tämä osio sisältää asetukset, jotka tarjoavat tietoa projektitasosta, kuten:

 * ProjectGuid
 * RootNamespace
 * ApplicationType tai ApplicationTypeRevision


## Viitteet

* [VCXPROJ-rakenne – MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


