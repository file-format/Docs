{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "file", "extension", "file format", "Visual C++ Project", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"További információ a VCXPROJ fájlformátumról és az API-król, amelyek VCXPROJ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az a VCXPROJ fájl?

A .vcxproj kiterjesztésű fájl egy Microsoft Visual C++ projektfájl, amely a [C++](/hu/programming/cpp/) projektinformációkat tárolja. Olyan információkat tartalmaz, amelyeket az MSBuild projektrendszer a végső kimenet összeállításához és felépítéséhez használ. A Visual C++ projektek VCXPROJ-ja megegyezik a .NET-projektek [CSPROJ](/hu/programming/csproj/) verziójával. A VCXPROJ fájlok nem tartalmaznak kódot, de hivatkoznak a projekthez a projekthez meghatározott összes osztályra, célra és tulajdonságra. Ezeket egyszerű szövegszerkesztőkkel vagy lehetőleg Microsoft Visual Studio IDE-ben lehet megnyitni.


## VCXPROJ fájlformátum – További információ

A VCXPROJ fájlok olyan szöveges fájlok, amelyek [XML](/hu/web/xml/) fájlformátumban jönnek létre. Ezek bármelyik szövegszerkesztőben megnyithatók, de erősen ajánlott a Microsoft Visual Studio IDE használata a fájlok megnyitásához és szerkesztéséhez. Ezeket nem kézi szerkesztésre tervezték. A hibák az IDE összeomlását vagy váratlan viselkedést okozhatnak.

A VCXPROJ mintafájl tartalma a következő.

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
### VCXPROJ fájlelemek

Egy tipikus VCXPROJ fájl számos elemet tartalmaz, amint az a fenti XML példában látható. A Microsoft [VCXPROJ szerkezete](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) részletesen elmagyarázza az egyes fájlelemeket, és hivatkozni is lehet rá. a fejlesztő szemszögéből.

#### Projektelem

Ez a VCXPROJ fájl gyökércsomópontja. Az MSBuild ezt az elemet használja a build verziójának és az alapértelmezett fordítási cél olvasásához.

#### ProjectConfigurations ItemGroup Element

Tartalmazza a projekt konfigurációs adatait, amelyek magukban foglalhatják a felépítési módszert (Debug vagy Release), a 32 vagy 64 bites fordítást, az optimalizálási beállításokat és egyebeket. Az ebben a csoportban található információkat az IDE használja a projekt betöltéséhez.

#### Projektkonfigurációs elemek

A VCXPROJ fájl ProjectConfiguration elemei információkat tartalmaznak arról a buildről és platformról, amelyre a projekt betöltve van. A nevének a következő formátumot kell követnie: `$(Configuration)|$(Platform)`.

#### Globals PropertyGroup Element

Ez a szakasz olyan beállításokat tartalmaz, amelyek projektszintű információkat tartalmaznak, például:

* ProjectGuid
* RootNamespace
* ApplicationType vagy ApplicationTypeRevision


## Hivatkozások

* [VCXPROJ Structure – MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

